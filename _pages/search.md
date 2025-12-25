---
layout: page
title: Search
permalink: /search/
---

<div id="search-container">
    <input type="text" id="search-input" placeholder="Search posts..." autocomplete="off">
    <ul id="results-container"></ul>
</div>

<style>
  #results-container {
    list-style: none;
    padding: 0;
    margin-top: 1.5rem;
  }
  
  #results-container li {
    margin-bottom: 0;
  }
  
  .search-result {
    display: block;
    padding: 1.25rem;
    background: #1a1a1a;
    border-radius: 8px;
    margin-bottom: 1rem;
    border: 1px solid #2a2a2a;
    transition: all 0.2s ease;
  }
  
  .search-result:hover {
    border-color: #6366f1;
    transform: translateY(-2px);
  }
  
  .search-result h2 {
    font-size: 1.1rem;
    margin: 0 0 0.5rem;
    color: #e8e8e8;
  }
  
  .search-result .date {
    font-size: 0.85rem;
    color: #555;
  }
</style>

<script src="{{ site.baseurl }}/assets/simple-jekyll-search.min.js" type="text/javascript"></script>

<script>
    SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    searchResultTemplate: '<li><a href="{url}" class="search-result"><h2>{title}</h2><span class="date">{date}</span></a></li>',
    noResultsText: '<li style="text-align: center; color: #555; padding: 2rem;">No results found</li>',
    json: '{{ site.baseurl }}/search.json'
    });
</script>