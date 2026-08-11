<%
function safeUrl(value) {
  const url = String(value || "").trim();
  return /^(https?:|mailto:)/i.test(url) ? url : "";
}

function sortName(item) {
  const name = item.name;
  if (Array.isArray(name) && name.length) {
    return String(name[0].label || name[0].name || "").toLowerCase();
  }
  return String(name || "").toLowerCase();
}

const sortedItems = [...items].sort((a, b) =>
  sortName(a).localeCompare(sortName(b))
);
%>

<div class="qmc-software-table-wrap">
<table class="qmc-software-table">
<caption class="visually-hidden">Community-maintained directory of quasi-Monte Carlo software</caption>
<thead>
<tr>
<th scope="col">Software</th>
<th scope="col">Language</th>
<th scope="col">Development status</th>
<th scope="col">Contact</th>
</tr>
</thead>
<tbody>
<% for (const item of sortedItems) { %>
<tr>
<td data-label="Software"><% if (Array.isArray(item.name)) { %><% for (let index = 0; index < item.name.length; index += 1) { const entry = item.name[index]; %><% if (index) { %> / <% } %><a href="<%= safeUrl(entry.url) %>"><%= entry.label || entry.name %></a><% } %><% } else { %><a href="<%= safeUrl(item.url) %>"><%= item.name %></a><% } %><% if (item.related && item.related.length) { %><span class="software-related">Related: <% for (let index = 0; index < item.related.length; index += 1) { const related = item.related[index]; %><% if (index) { %>, <% } %><a href="<%= safeUrl(related.url) %>"><%= related.name %></a><% } %></span><% } %><span class="software-description"><%= item.description %></span></td>
<td data-label="Language"><%= item.language %></td>
<td data-label="Development status"><% for (const status of String(item.status || "").split(", ")) { %><span class="software-status"><%= status %></span><% } %></td>
<td data-label="Contact"><% if (item.contact && item.contact.length) { %><% for (const contact of item.contact) { %><% if (typeof contact === "object" && contact.url) { %><a href="<%= safeUrl(contact.url) %>"><%= contact.name %></a><% } else { %><span><%= typeof contact === "object" ? contact.name : contact %></span><% } %><% } %><% } else { %><span aria-label="No contact listed">—</span><% } %></td>
</tr>
<% } %>
</tbody>
</table>
</div>
