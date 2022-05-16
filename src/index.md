---
# Feel free to add content and custom Front Matter to this file.

layout: default
paginate:
    collection: courses
    per_page: 1
---

<div class="columns">
    <div class="column is-four-fifth">
        <h1 class="has-text-left mb-2 mt-0"> Список курсов </h1>
    </div>
    <div class="column is-one-fifth">
        <div class="buttons is-right">
            <button class="button is-success mt-3">
                + Новый курс
            </button>
        </div>
    </div>
</div>
<hr class="mt-3">  



<div class="courses blocks">

    <% collections.courses.resources.each do |course| %>
        <div class="block">
      
            <div class="columns">
                    <div class="column is-four-fifths">
                        <p class="columns">Объем <%= course.data.volume %></p>
                        <a class="is-size-5 columns" href="<%= course.relative_url %>"><%= course.data.name %></a>
                    </div>
                    <p class="column has-text-right is-size-5"><b><%= course.data.price_USD %> $</b></p>
            </div>

        </div>
    <% end %>
  
</div>
<style>
.column a {
    text-decoration: none;
}
</style>

