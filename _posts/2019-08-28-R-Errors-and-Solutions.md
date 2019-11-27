From time to time, I has encountered error messages when I use R. 
Fortunately, I was able to find solutions to these errors from various web communities.
Preventing repeated web searching for solutions to errors, I will record the encountered errors and provide solutions found in various web communities.

1.  Error message   :   `Error in install.packages : ERROR: failed to lock directory ‘C:\Users\cocot\Documents\R\win-library\3.6’ for modifying.`

                        Try removing ‘C:\Users\cocot\Documents\R\win-library\3.6/00LOCK’ 

    Solution        :   Use `--no-lock` argument in the install option.

    Example         :   `install.packages("Rcpp", dependencies=TRUE, INSTALL_opts = c('--no-lock'))`

    Source          :   [Stackoverflow](https://stackoverflow.com/questions/14382209/r-install-packages-returns-failed-to-create-lock-directory)
