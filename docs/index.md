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
        {% endfor %}
        </tr>
        <tr>
            <a href="{{ mydata.Insides}}">{{mydata.Weight}} :: Outlink / {{ mydata.Descriptor}}</a>
        </tr>
    {% endfor %}
    </tbody>
</table>
