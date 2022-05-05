---
# Feel free to add content and custom Front Matter to this file.

layout: default
paginate:
    collection: courses
    per_page: 1
---

# Main page

<h3>With pagination:</h3>
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

<div>
  <h3>Without pagination:</h3>
  <ul>
    <% collections.courses.resources.each do |course| %>
      <li>
          <a href="<%= course.relative_url %>"><%= course.data.name %></a>
      </li>
    <% end %>
  </ul>
</div>

