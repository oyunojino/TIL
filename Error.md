# Error

## # DB 관련

### 1. 데이터베이스 생성 안됨

<details open>
  <summary>에러 메시지</summary>
<pre>
***************************
APPLICATION FAILED TO START
***************************

Description:

Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured.

Reason: Failed to determine a suitable driver class

Action:

Consider the following:
If you want an embedded database (H2, HSQL or Derby), please put it on the classpath.
If you have database settings to be loaded from a particular profile you may need to activate it (no profiles are currently active).

</pre>
</details>

<details>
  <summary>해결방법</summary>
<pre>

#### database 연결관련 정보를 입력해주지 않았기 때문

// application.properties

// # mysql 설정
spring.datasource.url=jdbc:mysql://localhost:3306/(database명)?characterEncoding=utf8
spring.datasource.username=(mysql 접속 username)
spring.datasource.password=(mysql 접속 password)
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

</pre>
</details>

---

---

<!-- ///////////////////////////////// -->

### Template

<details open>
  <summary>에러 메시지</summary>
<pre>
내용 1
내용 2
내용 3
</pre>
</details>
<details open>
  <summary>해결방법</summary>
<pre>
내용 1
내용 2
내용 3
</pre>
</details>

---

---

<!-- ///////////////////////////////// -->
