{% assign mydata=site.data.networks %}

<table>
    <caption>Network Table</caption>
    <thead>
    {% for column in mydata[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in mydata %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
            <tr><td>
            <a href="{{ mydata.Insides }}">{{ mydata.Weight }} :: Outlink / {{ mydata.Descriptor }}</a>
        </td><td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>
