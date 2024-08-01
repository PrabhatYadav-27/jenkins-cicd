1. THE STEPS MENTIONS ARE USE TO SETUP TRIGGERS ON JENKINS USING GITHUB 
  `Triggers ` basically works when developer or someone who performs certain action on that repository on which pipeline or scm had created on
2. In the execute shell type the files that you want to copy e.g `cp * filename/  /var/www/html` 
because this is where your apache/ httpd server store the file to display to the browser.
3. If you do this your build fails as you have no permission to perform any high-order privileged command only root user has the authority.
4. To solve the above problem you have to setup the authorit for it in your terminal open file called `vim /etc/sudoers/` there you can add anywhere user authority like
 NOPASSWD: ALL
`
and save this as this will give Jenkins the root privilege.
5. Then again you can build your job but again it will fail because in the execute shell you have to add `Sudo`  as it gave the root limited privilege to jenkins. This will solve the problem of job building and your job will be build within seconds. AS of now we have done every build manually but this is all done to check where our build is running or not.
6. Make sure to activate the `httpd` on your system to load the web server then refresh the web  page and your site will be up right there.``Cron Tab ``
`min hour date month day`
`5 10 11 04 *`
`5 10 * * *` everyday
`* * * * *` everyminute.

7. `Build Periodically` are based on cron tab when to use build automatically.
This will run in every-minute automatically this is build periodically in jenkins.

8. ``WEBHOOKS`` this is used in github to hook our github repo with other tool so to maintain the chances made in our repo visible to the tools too. So they can operate on the repo accordingly.
9. Jenkins have a `GitHub Hook Trigger for github scm polling` this act on our action of github which is connected to jenkins. For using this trigger setup the webhook.

10. Got to your github repo click on setting select the webhook  on `payload url = your machineip:portnumber`
e.g `http://192.168.xx.x:8080/github-webhook` and also selecte the action on which your jenkins will come to know is there need to perform any action to the specific job. Activate the webhook. 

11. For this you should have an public ip address of your machine for thisu you can use the ngrok which provide the temporary public ip address to use. Otherwise you can face some issues.
