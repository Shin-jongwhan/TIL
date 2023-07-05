# ajax
### <br/><br/><br/>

-----------------------------------------------------

## ajax 란
### 아래 블로그를 참고하였다.
#### https://codong.tistory.com/29
### Ajax(Asynchornous Javascript And XML)
#### AJAX란, JavaScript의 라이브러리중 하나이며 Asynchronous Javascript And Xml(비동기식 자바스크립트와 xml)의 약자이다. 
#### 브라우저가 가지고있는 XMLHttpRequest 객체를 이용해서 `전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법` 이며 JavaScript를 사용한 비동기 통신, 클라이언트와 서버간에 XML 데이터를 주고받는 기술이다.
### <br/><br/><br/>

## ajax 구현 방법
### html 부분에 ajax 코드를 작성한다.
```
<!-- ajax test -->
	<script type="text/javascript">
		$('#table-body').on('click', function(e) {
			data = $('#text').val();
			data = "test";
			$.ajax({
				type:'POST',
				url:'dashboard',
				data:JSON.stringify(data),
				headers: { "X-CSRFToken": '{{csrf_token}}' },
				success:function(json){
					console.log("data pass success",data);
				},
				error : function(xhr,errmsg,err) {
					console.log(xhr.status + ": " + xhr.responseText); 
				}
			});
			console.log(data);
		});
	</script>
```
### <br/>

### views.py 부분에는 POST method 가 호출되면 data 를 받을 수 있도록 작성한다.
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/59fd30cc-6149-4cb8-8b32-94930ed9b12e)
### <br/>

### 확인
### console 에 log 가 잘 찍힌다.
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/73f28b4a-a5c6-4770-b52b-27298a6c6489)
### django 서버 로그에도 잘 찍힌다. 
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/844d01db-0127-4d59-af25-57c699d63fb6)
### <br/><br/><br/>




