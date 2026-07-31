::: {.publication-catalog}

<% let currentYear = null; %>
<% for (const item of items) { %>

<% if (item.year !== currentYear) { currentYear = item.year; %>
### <%= item.year %>
<% } %>

::: {.publication-item}

#### <%= item.title %>

**<%= item.authors.join(", ") %>**

*<%= item.venue %>*<% if (item.series) { %>, <%= item.series %><% } %><% if (item.volume) { %>, volume <%= item.volume %><% } %><% if (item.pages) { %>, pages <%= item.pages %><% } %>, <%= item.year %>.

<% if (item.doi_url || item.publisher_url || item.arxiv_url) { %>
:::{.project-links}
<% if (item.doi_url) { %>[DOI](<%= item.doi_url %>){.btn .btn-primary}<% } %>
<% if (item.publisher_url) { %>[Publisher](<%= item.publisher_url %>){.btn .btn-outline-primary}<% } %>
<% if (item.arxiv_url) { %>[arXiv](<%= item.arxiv_url %>){.btn .btn-outline-primary}<% } %>
:::
<% } %>

<%= item.description %>

<% if (item.tags && item.tags.length) { %>
**Tags:** <%= item.tags.join(", ") %>
<% } %>

<% if (item.related_projects && item.related_projects.length) { %>
**Related projects:** <%= item.related_projects.join(", ") %>
<% } %>

:::

<% } %>

:::
