::: {.publication-catalog}

<% for (const item of items) { %>

::: {.publication-item}

### <%= item.title %>

**<%= item.authors.join(", ") %>**

*<%= item.venue %>*<% if (item.series) { %>, <%= item.series %><% } %><% if (item.volume) { %>, volume <%= item.volume %><% } %><% if (item.issue) { %>, issue <%= item.issue %><% } %><% if (item.pages) { %>, pages <%= item.pages %><% } %><% if (item.article_number) { %>, article <%= item.article_number %><% } %>, <%= item.year %>.

<% if (item.doi_url || item.publisher_url || item.arxiv_url || item.status_url) { %>
:::{.project-links}
<% if (item.doi_url) { %>[DOI](<%= item.doi_url %>){.btn .btn-primary}<% } %>
<% if (item.publisher_url) { %>[<%= item.publication_status === "historical-report" ? "Historical workshop link" : "Publisher" %>](<%= item.publisher_url %>){.btn .btn-outline-primary}<% } %>
<% if (item.status_url) { %>[Publication status](<%= item.status_url %>){.btn .btn-outline-primary}<% } %>
<% if (item.arxiv_url && !item.doi_url && !item.publisher_url) { %>[<%= item.type === "phdthesis" ? "Thesis text" : "arXiv preprint" %>](<%= item.arxiv_url %>){.btn .btn-outline-primary}<% } %>
:::
<% } %>

<%= item.description %>

<% if (item.publication_status === "historical-report") { %>
Historical workshop reference; the original link has not been independently reverified.
<% } %>

<% if (item.related_projects && item.related_projects.length) { %>
**Related projects:** <%= item.related_projects.join(", ") %>
<% } %>

:::

<% } %>

:::
