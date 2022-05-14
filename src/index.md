---
# Feel free to add content and custom Front Matter to this file.

layout: default
paginate:
    collection: courses
    per_page: 1
---

<div class="columns">
    <div class="column is-four-fifth">
        Список курсов
    </div>
    <div class="column is-one-fifth">
        <div class="buttons is-right">
            <button class="button is-success">
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
                    <div class="column">
                        <a class="is-size-3 columns is-four-fifths" href="<%= course.relative_url %>"><%= course.data.name %></a>
                        <p class="columns is-four-fifths"><%= course.data.description %></p>
                    </div>
                    <p class="column has-text-right"><b><%= course.data.volume %></b></p>
            </div>

        </div>
    <% end %>
  
</div>

