<h1>About this document</h1>

<p>This document will descript what is docker-compose and how to implement the docker-compose to build up the Webserver, WordPress and MySQL server. Moreover, there will descript some of the threat that the Webserver, WordPress and MySQL server may face with. Also, there will provide the solution to deal with those attack method in order to reduce the risk for the attack.</p>


<h3>Docker-compose</h3> 
  
<p>Docker-compose is a powerful tool that can have multi-container to conduct the services. Normally, the YAML file will be used to define the services and the specified command. Once the user downloads the file which include the YAML, they can immediately use the service and have the same environment to conduct their work. After download the file, the command “docker-compose up -d” need to be entered to start the docker-compose and the user must inside that directory which having the YAML file. The services can be removed or added into the YAML file.</p>

<i>(Notice: the docker-compose need to be downloaded first in the Linux/Ubuntu/Nginx/Others)</i>
 
<i>Start command = docker-compose up -d</i> 

<i>Turn off command = docker-compose down</i>

<h3>Securit threats</h3>
<ul>
<li>SQL Injection

SQL Injection is a web security vulnerability that allows attackers to interfere with the queries that an application makes to its database. Attackers are able to view the data that aren't normally retrievable. This damages data confidentiality.</li>

<li>XSS

Cross-Site Scripting (XSS) is also a type of injection. Attackers use a web application to send the malicious scripts to end users to confuse the browser where there is no way to tell that whether or not the script should or should not be trusted and will simply just execute the script. This gives attackers access to the victims' cookies, session tokens, or even some other sensitive information held by the browswer.</li>

<li>Brute force attack

Brute-force attack, a cryptanalytic attack which consists of an attacker submitting many passwords with the eventually guessing correctly. All possible passwords and passphrases until the correct one is found will be checked by the attacker systematically. If the strength of the encryption is weak, the attacker can take less time to mount the brute-force attack.


</li>

<li>Leakage of Data in MySQL

Data leakage happens when data ends up somewhere it’s not supposed to be. Data leaks lead errors made during model creation or during configuration and expose sensitive information which may violate laws and the privacy of the client
</li>


<li>Unauthorized use of resources


</li>
</ul>

<h3>Prevention</h3>

<ol>
<li>POLP is an idea where people apply the practice of minimizing data access by restricting access rights for users in a data system. Granting the minimum level of user rights allows them to acces specific resources needed only to perform their role. The reduces the risk of exploitation and improves productivity.</li>


<li>Multi-Factor authentication can enforce data confidentiality. In our WordPress, we used the miniOrange plugin to implement this feature, where we used one-time passwords through Telegram for authentication</li>

</ol>

<h3>FAQ</h3> 
  
<h4>Why use docker-compose?</h4> 
 
<p>To enhance the efficiency, it is suggested to use the docker-compose to conduct the services because it contains multiple containers to store the application like MySQL server, Web Server and others. When the docker-compose start process, all the application will be up and don’t need to set up one by one like using the individual container. Therefore, docker-compose will be suggested to used due to the YAML that can include all the application and the user can set up the configuration inside this YAML file like image, volume and others.</p>

<h4>Why use WordPress security plugin?</h4> 

<p>In the real world, application attack such as Cross-site scripting and SQL injection are very dangerous. By using the security plugin, it can reduce the risk that the attacker can use the XSS to inject some malicious payload into the website and get some sensitive information / do some malicious action.</p>
 
<p>The security plugin can provide the ability to</p>
<ol>
<li>Prevent Brute-force attack</li>
<li>XSS attack</li>
<li>SQL injection</li>
<li>DoS attack</li>
</ol>
<p>Demo Video</p>
<li[>https://youtu.be/EHP2o4NmFb</li>
