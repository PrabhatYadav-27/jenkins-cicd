``This will be a explanation ground for pipelins on Jenkins``

`Build Server` this is something that use to build or compile the code or application this is called buil server.

`Worker node ` this is not the final node this all the nodes which perform a single work or function to attain the whole job e.g `1.git node`, `2.maven node`, `3.deploy node`.
By combining all the step of 1, 2 and 3 we create a whole job that all are dependent to each other.

By considering the above scenario of all the three jobs
`Job 1` is called the ``UpStream Job ``  with respect to `Job 2` 
Where as `Job 3` will be known as ``DownStream Job``  this create the whole pipleine for you and this scenario can include hundreds of job and the upstream and downstream will change accordingly with the respect to the job.