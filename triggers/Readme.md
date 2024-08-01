1. ThE STEPS MENTIONS ARE USE TO SETUP TRIGGERS ON JENKINS USING GITHUB 
  `Triggers ` basically works when devleoper or someone who perform certain action on that repository on which pipeline or scm had created on
2. In the execute shell type the files which you want to copy e.g `cp * filename/  /var/www/html` 
because this is where your apache/ httpd server store the file to display to the browser.
3. If you do this your build get failed as you have no permission to perform any high order privilleged command only root user has the authority.
4. To solve the above problem you have to setup the authorit for it in your terminal open file called `vim /etc/sudoers/` there you can add anywhere user authority like
 NOPASSWD: ALL
`
and save this as this will give jenkins the root privillege.
5. Then again you can build your job but again it will fail because in the execute shell you have to add `Sudo`  as it gave the root limited privillege to jenkins. This will solve the problem of job building and your job will be build within seconds. AS of now we have done every build manually but this is all done to check where our build is running or not.
6. Make sure to activate the `httpd` on your system to load the web server then refresh the web  page and your site will be up right there.``Cron Tab ``
`min hour date month day`
`5 10 11 04 *`
`5 10 * * *` everyday
`* * * * *` everyminute.

7. `Build Periodically` are based on cron tab when to use build automatically.
This will run in everyminute automatically this is build periodically in jenkins.

8. ``WEBHOOKS`` this is used in github to hook our github repo with other tool so to maintain the chances made in our repo visible to the tools too. So they can operate on the repo accordingly.
9. Jenkins have a `GitHub Hook Trigger for github scm polling` this act on our action of github which is connected to jenkins. For using this trigger setup the webhook.

10. Got to your github repo click on setting select the webhook  on `payload url = your machineip:portnumber`
e.g `http://192.168.xx.x:8080/github-webhook/` and also selecte the action on which your jenkins will come to know is there need to perform any action to the specific job. Activate the webhook. 

11. For this you should have an public ip address of your machine for thisu you can use the ngrok which provide the temporary public ip address to use. Otherwise you can face some issues.

12. ``Trigger build remotely`` this trigger is used to build the job remotely by accessing a token authenitication or just a `api url` that is provided to  build the job but this one is quite risky because it  expose your login so avoid to use this. There are more triggers in jenkins that differ in their use case.

13. Every trigger has it's own use case use the triggers according to your use case.

14. For more  do follow the documentation for new features and implementation.