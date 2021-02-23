set_password란 명령어를 이용해서 패스워드를 암호화할 수 있다.



기본 pagination
<div>

    <span>
        {% if page_obj.has_previous %}

        <a href="?page={{page_obj.previous_page_number}}">이전</a>
        {% endif %}

        페이지 {{ page_obj.number }} / {{ page_obj.paginator.num_pages}}

        {% if page_obj.has_next %}
        <a href="?page={{page_obj.next_page_number}}">다음</a>
        |
        <a href="?page={{page_obj.paginator.num_pages}}">맨 뒤로</a>
        {% endif %}

    </span>
</div>




숫자 pagination


    {# First Previous #}
    {% if page_obj.has_previous %}
    <span>
        <ul class="pagination">
            <ul class="pagination justify-content-center" style="margin:20px 0">
                <li class="page-item"></li>
            </ul>
            <a class="page-link" href="?page=1">Previous</a></li>
        <li class="page-item active">
            <a class="page-link" href="?page={{page_obj.number}}">1</a></li>
        <li class="page-item"><a class="page-link" href="?page=2">2</a></li>
        <li class="page-item"><a class="page-link" href="?page=3">3</a></li>
        <li class="page-item"><a class="page-link" href="?page={{page_obj.next_page_number}}">Next</a></li>
        </ul>
    </span>

    {% endif %}

    {# current of all #}
    <span>
        <li class="page-item active">
            <li class="page-item"><a class="page-link" href="page=1">맨 앞으로</a>           
        |
        <li class="page-item"><a class="page-link" href="?page={{page_obj.previous_page_number">이전</a></li>
        <li class="page-item"><a class="page-link" href="?page={{page_obj.previous_page_number}}">{{page_obj.previous_page_number}}</a></li>>
        <li class="page-item disabled"><a class="page-link" href="?page={{page_obj.number}}">{{page_obj.number}}</a>
        <li class="page-item"><a class="page-link" href="?page={{page_obj.next_page_number}}">{{page_obj.next_page_number}}</a></li>
        <li class="page-item"><a class="page-link" href="?page={{page_obj.next_page_number}}">다음</a></li>
        |
        <li class="page-item"><a class="page-link" href="?page={{page_obj.paginator.num_pages}}">맨 뒤로</a>
    </ul>
    </span>

    {# Next Last #}
    {% if page_obj.has_next %}
    <span>
        <li class="page-item active">
            <li class="page-item"><a class="page-link" href="page=1">맨 앞으로</a>           
        |
        <li class="page-item"><a class="page-link" href="?page={{page_obj.previous_page_number">이전</a></li>
        <li class="page-item"><a class="page-link" href="?page={{page_obj.previous_page_number}}">{{page_obj.previous_page_number}}</a></li>>
        <li class="page-item disabled"><a class="page-link" href="?page={{page_obj.number}}">{{page_obj.number}}</a>
        <li class="page-item disabled"><a class="page-link" href="?page={{page_obj.next_page_number}}">다음</a></li>
        |
        <li class="page-item"><a class="page-link" href="?page={{page_obj.paginator.num_pages}}">맨 뒤로</a>
    </ul>
    </span>
    {% endif %}

