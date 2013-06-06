flipper
=======

3D flow over a humpback whale flipper with OpenFOAM

Usage
-----

To generate the mesh, execute the Allrun script:  
`$ ./Allrun`  
(this runs blockMesh, surfaceFeatureExtract, and snappyHexMesh)

Then, to run the flow solver in the background:  
`$ foamJob simpleFoam`

While the solver is running, you can peek at the last 10 lines of output with:
`$ tail log`  
or, to see a live update of the log file:  
`$ tail -f log`

Once the job completes, extract data of residuals and iterations with:  
`$ foamLog log`

Then, you can plot the residuals over time to check if the solution has
converged. Files are located in the 'logs' sub-directory. (Hint: pull the logs
directory out with Dropbox, then plot the files with pylab.)
