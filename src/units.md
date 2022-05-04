---
layout: page
title: Units
paginate:
  collection: units
  per_page: 2
---

<ul>
<% paginator.resources.each do |course| %>
  <li>
      <a href="<%= course.relative_url %>"><%= course.data.name %></a>
  </li>
<% end %>
</ul>
<div>
<% if paginator.total_pages > 1 %>
    <% if paginator.previous_page %>
      <a href="<%= paginator.previous_page_path %>">Previous Page</a>
    <% end %>
    <% if paginator.next_page %>
      <a href="<%= paginator.next_page_path %>">Next Page</a>
    <% end %>
<% end %>
</div>