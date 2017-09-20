# SimpleWeblogicHTML
Simple demo website example for deployment into Weblogic document Root

>Oracle Weblogic is a common web application server for deploying Java based web applications. In many architectures >a standard HTTP server (Apache, IIS) is used to serve static content “in front” of a Weblogic server. There are >times when deploying a static website into the server root URL would be ideal without the additional HTTP server and >it’s reverse proxy.

Checkout the Blog for more details:
 http://blog.dataroadtech.com/deploying-a-stat…as-document-root/
 
1. Create a folder on your Weblogic server called portal (e.g. c:\portal)

* In that folder create a file called index.html (see the example code)

2. Create a folder in the portal folder called WEB-INF (e.g. c:\portal\WEB-INF)

3. In the WEB-INF directory create a file called web.xml (see the example code)

4. In the WEB-INF directory create a file called weblogic.xml (see the example code)

5. In Weblogic Console -> Click on Deployments.

6. Click Install and set the path to the directory of step 1 (if the directory only contains the html file and the WEB-INF sub-directory you will see no files to select, but the Next button will be enabled anyway).

7. Leave default "Install this deployment as an application" and click Next.

8. Select the servers you wish to deploy this application

9. Accept the defaults and click Finish.

10. Activate Changes if the message appears.

You should now be able to see the application started in the deployments screen.

__REMEMBER to START your Application__

Assuming you choose the name "portal" for your application should should see your live document root here:

\<middleware home\>\\user_projects\\\domains\\base_domain\\servers\\<your server\>\\stage\\portal\\portal

__NOTE:__ You CAN edit these files directly HOWEVER if you need to redeploy in the future you will lose all those changes if they are not back ported to c:\portal