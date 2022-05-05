---
layout: page
title: Units
paginate:
  collection: units
  per_page: 2
---

<ul>
  <% paginator.resources.each do |unit| %>
    <li>
        <a href="<%= unit.relative_url %>"><%= unit.data.name %></a>
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
<div>
  <h3>Without pagination:</h3>
  <ul>
    <% collections.units.resources.each do |unit| %>
      <li>
          <a href="<%= unit.relative_url %>"><%= unit.data.name %></a>
      </li>
    <% end %>
  </ul>
</div>