<table class="table table-striped" style="width: 100%;">
{% for w in site.data.amy  %}
    {% for wt in w.tags %}
    {% if wt['name'] == "SWC" or wt['name'] == "DC" or wt['name'] == "LC" %}
    <tr>
    <td>
        <img src="{{site.url}}/assets/img/logos/{{ wt['name'] | downcase}}.png" title="{{ wt['name'] }} workshop" alt="{{ wt['name']}} logo" width="24" height="24"/>
    </td>
    <td>
      <img src="{{site.url}}/assets/img/flags/{{site.flag_size}}/{{w.country | downcase}}.png" title="{{w.country | replace: '-', ' '}}" alt="{{w.country | replace: '-', ' ' | downcase}}" />
      <a href="{{w.url}}">{{w.venue}}</a>
	</td>
	<td>
		{{w.humandate}}
	</td>
	</tr>
    {% endif %}
    {% endfor %}
{% endfor %}
</table>
