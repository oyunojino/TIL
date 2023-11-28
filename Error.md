# Error

## # DB 관련

<!-- ///////////////////////////////// -->

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
<!-- ///////////////////////////////// -->

### 2. SQLIntegrityConstraintViolationException

<details open>
  <summary>에러 메시지</summary>
<pre>
2023-11-24T14:53:44.474+09:00  WARN 4752 --- [nio-8080-exec-2] o.h.engine.jdbc.spi.SqlExceptionHelper   : SQL Error: 1048, SQLState: 23000
2023-11-24T14:53:44.474+09:00 ERROR 4752 --- [nio-8080-exec-2] o.h.engine.jdbc.spi.SqlExceptionHelper   : Column 'item_status' cannot be null
2023-11-24T14:53:44.553+09:00 ERROR 4752 --- [nio-8080-exec-2] o.a.c.c.C.[.[.[/].[dispatcherServlet]    : Servlet.service() for servlet [dispatcherServlet] in context with path [] threw exception [Request processing failed: org.springframework.dao.DataIntegrityViolationException: could not execute statement [Column 'item_status' cannot be null] [update items set bid_id=?,category_id=?,created_at=?,description=?,image_url=?,is_biding=?,item_status=?,title=?,updated_at=?,user_id=? where item_id=?]; SQL [update items set bid_id=?,category_id=?,created_at=?,description=?,image_url=?,is_biding=?,item_status=?,title=?,updated_at=?,user_id=? where item_id=?]; constraint [null]] with root cause

java.sql.SQLIntegrityConstraintViolationException: Column 'item_status' cannot be null
at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:118) ~[mysql-connector-j-8.0.33.jar:8.0.33]

</pre>
</details>
<details>
  <summary>해결방법</summary>
<pre>

#### 수정 시 dto에 포함된 모든 값이 변경되지않아 null로 출력됨

</pre>
</details>

---

---

<!-- ///////////////////////////////// -->
<!-- ///////////////////////////////// -->

### 3. Template

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
