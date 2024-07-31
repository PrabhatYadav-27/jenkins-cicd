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
6. Make sure to activate the `httpd` on your system to load the web server then refresh the web  page and your site will be up right there.  