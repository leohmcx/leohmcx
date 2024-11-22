# Leonardo Cornachione

routes.get('/recentSVG', (request, result) =>
{
    sql.getRecentPosts(4).then((sqlData)=>
    {  
        result.writeHead(200, {'Content-Type': 'image/svg+xml',
            'Cache-Control': 'no-cache',
            'Vary': 'Accept-Encoding'});
        var res = `
        <svg width="400" height="200" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
            <g>
                <title>background</title>
                <rect x="-1" y="-1" width="808" height="202" id="canvas_background" fill="#fff"/>
                    <g id="canvasGrid" display="none">
                <rect id="svg_1" width="100%" height="100%" x="0" y="0" stroke-width="0" fill="url(#gridpattern)"/>
                </g>
            </g>
            <g>
                <title>Jrtechs</title>
                <a xlink:href="https://jrtechs.net">
                    <text fill="#498FBE" stroke="#000" stroke-width="0" stroke-opacity="null" x="36.5" y="40.5" id="svg_6" font-size="24" font-family="Oswald, sans-serif" text-anchor="start" xml:space="preserve" font-weight="bold">Recent Blog Posts</text>
                </a>
                <a xlink:href="${getURL(sqlData[0])}">
                    <text fill="#000000" stroke="#000" stroke-width="0" stroke-opacity="null" x="65.5" y="73.5" id="svg_7" font-size="20" font-family="Oswald, sans-serif" text-anchor="start" xml:space="preserve" font-weight="normal">- ${sqlData[0].name}</text>
                </a>
                <a xlink:href="${getURL(sqlData[1])}">  
                    <text fill="#000000" stroke="#000" stroke-width="0" stroke-opacity="null" x="65.5" y="106.5" id="svg_7" font-size="20" font-family="Oswald, sans-serif" text-anchor="start" xml:space="preserve" font-weight="normal">- ${sqlData[1].name}</text>
                </a>
                <a xlink:href="${getURL(sqlData[2])}">
                    <text fill="#000000" stroke="#000" stroke-width="0" stroke-opacity="null" x="65.5" y="139.5" id="svg_7" font-size="20" font-family="Oswald, sans-serif" text-anchor="start" xml:space="preserve" font-weight="normal">- ${sqlData[2].name}</text>
                </a>
                <a xlink:href="${getURL(sqlData[3])}">   
                    <text fill="#000000" stroke="#000" stroke-width="0" stroke-opacity="null" x="65.5" y="172.5" id="svg_7" font-size="20" font-family="Oswald, sans-serif" text-anchor="start" xml:space="preserve" font-weight="normal">- ${sqlData[3].name}</text>
                </a>
            </g>
        </svg>`;
        result.write(res);
        result.end();
    }).catch((err)=>
    {
        result.status(404).json({error: 404}).end();
    })
});

[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/leohmcx)](https://github.com/leohmcx)
<!--[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/leohmcx/)](https://www.linkedin.com/in/leohmcx/)-->

<p>
  <img src="https://img.shields.io/badge/Backend-Java-informational?style=flat&logo=java&logoColor=red&color=05122A" />
  <img src="https://img.shields.io/badge/Backend-Kotlin-informational?style=flat&logo=kotlin&color=05122A" />
  <img src="https://img.shields.io/badge/Cloud&nbsp;Public-Amazon&nbsp;AWS-informational?style=flat&logo=Amazon&color=05122A" />
  <img src="https://img.shields.io/badge/Cloud&nbsp;Private-Kubernetes-informational?style=flat&logo=kubernetes&color=05122A" />
  <img src="https://img.shields.io/badge/Container-Docker-informational?style=flat&logo=docker&color=05122A" />
</p>

### Hi there 👋

I am backend software engineer and tech lover.

### Formações
- 🎓 Degree in Analisys and System developement FATEC-AM - 2º/2015
- 🎓 Post degree in Mobile development (Android and iOS) IFSP - 2º/2019

## Hard skils

### Backend
- [x] Java 11 | Spring | Kotlin | Java EE | Python | Node
- [x] Junit | Mockito | PowerMock | RestAssured
- [x] Swagger | OpenApi
- [x] Restful | SOAP | gRPC
- [x] Apache Kafka | Apache ActiveMQ | Rabbit | IBM MQ
### Frontend
- [x] Angular 14 | React | RxJs | TypeScript | Angular JS | Javascript
- [x] Cypress | Jest | Express | Selenium | NodeJs
- [x] Micro Frontends | Module Federation | Web Components | Webpack
### Cloud
- [x] AWS ApiGateway, Lambda, ECS, Bucket, IAM, Dynamo, SQS, SNS, CloudFormation, CloudWatch, CodePipeline
- [x] Azure
### Application
- [x] Tomcat | Jboss EAP | Jboss AS
- [x] Docker | OpenShift | Rancher | Jenkins | Sonar | Git
- [x] Eclipse | IntelliJ IDEA | VSCode | DataGrip | Kafka Tools | Postman | SoapUI
- [x] Linux | Windows | Mac OS 
### Databases
- [x] Postgres | Oracle | SQL Server | MySQL | DB2 | MongoDb
### Others
- [x] Jira | Redmine | Jazz | Kanbanize | Scrum
- [x] English B2 level
- [x] PIX (Instant payment - Brazil)

---

<!--
**leohmcx/leohmcx** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
