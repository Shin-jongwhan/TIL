## cloudtables
### https://cloudtables.com/
### 테이블 만드는 데에 꽤 잘 꾸며주길래 한 번 예시로 사용해보았다.
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/43e51cc1-340d-446a-a295-94cda64d1d89)
### <br/>

### 코드
### django web server 에서 테스트하였다.
```
{% extends 'html/home.html' %}
{% load static %}
{% load bootstrap5 %}

{% block static %}
<script src="{% static 'js/jquery-3.7.0.min.js' %}"></script>
<link href="{% static 'css/dashboard.css' %}" rel="stylesheet" type="text/css" />
<!-- datatables -->
<link rel="stylesheet" href="https://cdn.datatables.net/1.13.6/css/jquery.dataTables.css" />
<script src="https://cdn.datatables.net/1.13.6/js/jquery.dataTables.js"></script>

<title>분석 작업</title>
<script type="text/javascript">
    var setpointpage = "{% url 'todolist_dashboard' %}";
    console.log(setpointpage);
</script>

<!-- external js 에 django variant 할당해주기 위한 variant 선언 -->
<script>
    var scrf_token = "{{csrf_token}}";
</script>
{% endblock %}

{% block content %}
    <table id="myTable" class="display">
        <thead>
            <tr>
                <th>Column 1</th>
                <th>Column 2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Row 1 Data 1</td>
                <td>Row 1 Data 2</td>
            </tr>
            <tr>
                <td>Row 2 Data 1</td>
                <td>Row 2 Data 2</td>
            </tr>
            ...
        </tbody>
    </table>

    <script>
        $(document).ready( function () {
            $('#myTable').DataTable();
        } );
    </script>

{% endblock content %}
```
### <br/>


### 예시로 따라해본 것
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/4c79a6f2-2123-4837-a17f-13e4fcb499ba)
### <br/><br/><br/>


