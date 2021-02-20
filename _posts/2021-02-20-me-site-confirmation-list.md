---
layout: post
title:  "Updated M&E Site Confirmation List"
date:   2021-02-20 9:00:00 +0800
categories: jekyll update
---
<table style="width:55vw">
  <tr>
    <th>S/N</th>
    <th>SC Ref. No.</th>
    <th>Decription</th>
	<th>Date Issued</th>	
  </tr>
{% assign counter = 0 %}
{% for scme in site.data.scme %}
<tr>	
	<td>{{ counter | plus: 1}}</td>
	<td>{{ scme.scme_no }}</td>
	<td><a href="{{ scme.url }}" target="_blank"> {{ scme.title }}</a></td>
	<td>{{ scme.issued_date }}</td>
	{% assign counter = counter | plus: 1 %}	
</tr>
{% endfor %}