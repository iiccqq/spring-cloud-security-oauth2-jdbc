# spring-cloud-security-oauth2-jdbc
使用spring-cloud-security-oauth2来实现oauth server和resource server，oauth Server和resource Server分开，resource Server实现了两种方式，一种是当用token调用受保护资源时，使用RemoteTokenServices来去oauth server去校验。另一种是共享数据库，然后资源服务器自己通过数据库进行校验。



get:
http://localhost:8080/uaa/oauth/authorize?client_id=acme&state=state&response_type=code&redirect_uri=http://localhost:8081

post:
http://localhost:8080/uaa/oauth/token?client_id=acme&state=state&response_type=code&redirect_uri=http://localhost:8081&grant_type=authorization_code&code=YTZuAz

get:
http://localhost:8081/hello


