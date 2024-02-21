---
layout: layouts/ficheLecture.html
title: /Fiches_de_lecture
tags: memoire
category: [ all, danse, archivage]
previous: /Mémoire
wantedCategory: all
---

<div class="fiches_filter">
<button id="dansebtn" onclick="displayDanse('visible','yellow'); displayAll('hidden', 'white')">danse</button>
<button id="allbtn" onclick="displayDanse('hidden', 'white');displayAll('visible', 'yellow')">all</button>
</div>



<div class="fiches_liste">
<div id="all">
{% for fiches in collections.fiches %}
<a href="{{fiches.url}}">{{fiches.data.bookTitle}}</a>
{% endfor %}
</div>

<div id="danse">
{% for fiches in collections.fiches %}
{% if fiches.data.category == "danse" %}
<a href="{{fiches.url}}">{{fiches.data.bookTitle}}</a>
{% endif %}
{% endfor %}
</div>   
</div>

<script>
function displayDanse(newValue, newColor) {
  var danse = document.getElementById("danse");
  var dansebtn = document.getElementById("dansebtn")
danse.style.visibility = newValue;
dansebtn.style.backgroundColor = newColor;
}
function displayAll(newValue, newColor){
    var all = document.getElementById("all");
    all.style.visibility = newValue;
    var allbtn = document.getElementById("allbtn")
    allbtn.style.backgroundColor = newColor;
}
</script>

<!-- <script>
    var danse = "danse";
    var wantedCategory = "all";

    function selectCategory(){
        return wantedCategory;
    }
    
    console.log(wantedCategory);

</script>

<div class="fiches_filter">
    {% for category in category %}
    <button onclick="selectCategory({{category}})">{{category}}</button>
    {% endfor %}
</div> 

{% for fiches in collections.fiches %}
    {% if fiches.data.category == "all" %}
    <li>{{fiches.data.title}}</li>
    {% endif %}
{% endfor %} -->


