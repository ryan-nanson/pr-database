---

layout: home
include_scripts: [
  "https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js",
  "https://d3js.org/d3.v5.min.js",
  "/assets/js/search.js"
]
---
<h2>List of Prose Romances</h2>

<input type="text" id="search" placeholder="Type to search">
<table id="table">
  {% for book in site.data.books %}
   <tr>
      <td><a href="{{ book.title | datapage_url: 'all-books' }}">{{book.title}}</a></td>
      <td>{{ book.year }}</td>
      <td style="display:none;">{{ book.author }}</td>
   </tr>
   {% endfor %}
</table>

