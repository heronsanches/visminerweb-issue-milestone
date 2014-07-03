visminerweb-issue-milestone
===========================

Examples of Visualization utilizing the <a href="https://github.com/visminer/Visminer">API Visminer</a> and <a href="https://developers.google.com/chart/">Google Charts</a>.<br>
Examples mostly utilizing information about Issues, Milestones and correlations get from Visminer API.<br>


<h4>Instructions:<h4>
<h5>1- you have to install the database mysql.<h5>
<h5>2 - you have to install Tomcat v7 and add the connector of mysql in your lib folder.</h5>
<b>For example:</b><br>
folder path for your instalation of Tomcat v7:<br>
..apache-tomcat-7.0.53/lib/<br><br>
add in this folder:<br>
mysql-connector-java-5.1.26-bin.jar (this version is used by API visminer 0.7.0)<br><br>

<h5>3 - you have to fill the fields in  <a href="https://github.com/heronsanches/visminerweb-issue-milestone/blob/master/VisualizationsWeb-Visminer/src/org/visminer/web/main/Visminer.java">Visminer.java</a> with "" with your respective means, and the field where
has api_cfg_local.put(VisMiner.LOCAL_REPOSITORY_PATH,"/LocalPathRepositoryProject/.git");
you have to change LocalPathRepositoryProject by your local path where was cloned the repository github. Don't forgot the "/.git", use the format above.<br><br></h5>

<h5>Means of the fields required in Visminer.java</h5>
String JDBC_USER = ""; <b>put here the user root of database mysql</b><br>
String JDBC_PASSWORD = ""; <b>put here the password of the user root above of database mysql</b><br>
api_cfg_local.put(VisMiner.LOCAL_REPOSITORY_PATH,
				"/LocalPathRepositoryProject/.git"); <b>already explaned</b>
				
<b>
https://github.com/heronsanches/Visminer<br>
VisMiner.LOCAL_REPOSITORY_OWNER === heronsanches<br>
VisMiner.LOCAL_REPOSITORY_NAME === Visminer (can be Uppercase or lowcase or mix them)<br>
</b>
api_cfg_local.put(VisMiner.LOCAL_REPOSITORY_NAME, "visminer");<br>
api_cfg_local.put(VisMiner.LOCAL_REPOSITORY_OWNER, "visminer");<br>

api_cfg_remote.put(VisMiner.REMOTE_REPOSITORY_LOGIN, ""); <b>your login in GitHhub</b>
api_cfg_remote.put(VisMiner.REMOTE_REPOSITORY_PASSWORD, "");<b>your password in GitHhub</b>


<h5> 4- executing the visualizations</h5>
after instructions from 1 to 3 put these url below in your browser for to visualize visualizations<br>
the port 8080 is default for TomCat v7<br><br>
![Alt text](https://github.com/heronsanches/visminerweb-issue-milestone/blob/97e39202f6f6cab30e4eba0208eed4fb2970beac/VisualizationsWeb-Visminer/visualizations-images/labelQuantity.png?raw=true "Optional Title")<br>
http://localhost:8080/VisualizationsWeb-Visminer/labelIssues<br>

![Alt text](https://github.com/heronsanches/visminerweb-issue-milestone/blob/97e39202f6f6cab30e4eba0208eed4fb2970beac/VisualizationsWeb-Visminer/visualizations-images/ocCorrelation.png?raw=true "Optional Title")<br>
http://localhost:8080/VisualizationsWeb-Visminer/labelIssues_OpenedClosed_byLabel<br>






