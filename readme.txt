newman run AutomationSample.postman_collection.json -e reqres_SSL.postman_environment.json

cd d:\git\PostmanAutomation
newman run d:\git\PostmanAutomation\AutomationSample.postman_collection.json -e d:\git\PostmanAutomation\reqres_SSL.postman_environment.json --reporters cli,html --reporter-html-template d:\git\PostmanAutomation\htmlreqres.hbs --disable-unicode


-Dhudson.lifecycle=hudson.lifecycle.WindowsServiceLifecycle

cd d:\git\PostmanAutomation
newman run d:\git\PostmanAutomation\AutomationSample.postman_collection.json 
-e d:\git\PostmanAutomation\reqres_SSL.postman_environment.json 
--reporters cli,html --reporter-html-template htmlreqres.hbs --disable-unicode

Jenkins.xml

 <executable>%BASE%\jre\bin\java</executable>
  <arguments>-Xrs -Xmx256m -Dhudson.lifecycle=hudson.lifecycle.WindowsServiceLifecycle -Dhudson.model.DirectoryBrowserSupport.CSP -jar "%BASE%\jenkins.war" --httpPort=9080 --webroot="%BASE%\war"</arguments>
