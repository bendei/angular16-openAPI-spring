# Java (Spring Boot) and Angular basic showcase
THis project conatains 3 module: a parent one, a backend and frontend.
We build here a Spring fat jar, that contains the backend and the frontend.
We can start frontend and backend separately too.

### Frontend:
Angular app uses port 4200, java backend 8081.
The heavy lifting is done by the plugin https://github.com/eirslett/frontend-maven-plugin. This plugin downloads and installs node, install the libraries and build the project by running npm install.
C:\Users\36309\.m2\repository\com\github\eirslett\node\20.5.1\node-20.5.1-win-x64.exe
(com.github.eirslett mint a kvs projectben)
The result is a jar file that contains the Angular application compiled.

### Buildelés:
A. java-angular-example: mvn clean, install
B. vagy csak a forntend/backend külön 

This is a quick starter for projects using Spring Boot as backend and Angular as frontend.

### Backend
Wir haben das Frontend Module in das Backend module importiert, wir haben maven-dependency-plugin verwendet, welches den Frontend-Inhalt auspakt und kopiert es im /classes/static Verzeichnis von Backend.
Pacjaking von Backend was als war File, und wir haben es in einer der Wildfly Servers eingespielt.
Az (backend) app futtatása:
1. mvn clean; mvn package
2. cd bacend/target
3. mvn java -jar backend-0.1-SNAPSHOT.jar

vagy: Application RUn configból futtatjuk a Application osztályt.

### Frontend futtatása:
1. cd frontend
2. ng serve
3. ng testű

### OpenAPI ( Swagger ) for defining and documenting REST API
-- we generate typescript and java fiels from OpenAPI definition file: API first approach. OpenAPI spec is one of the spec formats.
// https://blog.mimacom.com/using-the-openapi-generator-for-spring-boot/
// https://www.stefanwille.com/2021/05/2021-05-30-openapi-code-generator-for-typescript
// defintion file tutorial
// https://support.smartbear.com/swaggerhub/docs/tutorials/openapi-3-tutorial.html


To the basic example I added some 'showcases' extra features:
- Test with MockMvc
- Test with RestTemplateTest
- OpenApi using Spring Doc (code first). Swagger-ui is accessible here: http://localhost:8080/swagger-ui

### making subsequent commits locally and than pushing it all as one with one commit message:
1. Go to Git pane in the IDE down below -> stand with coursor with Remote-origin-master: click "compare with master"
2. In the window in the middle "Commits that exists in master but dont exist in origin/master" -> jobb erér click -> squash commits : write a new message
3. Now check the squased message apperas  in the pane where you can find commits (and #1 #2 commits disappear)
4. Push

## java version news:
    https://www.marcobehler.com/guides/a-guide-to-java-versions-and-features