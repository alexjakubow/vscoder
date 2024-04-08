Currently includes the following packages and their related dependencies (See renv.lock for more info)

- `renv`
- `here`
- `httpgd`
- `languageserver`


This minimal installation should be sourced from within VSCode per the instructions listed here:

https://github.com/REditorSupport/vscode-R/wiki/Working-with-renv-enabled-projects


If you are creating your own renv, be sure to explicitly specify which packages to add to the lockfile by including them in the `packages` argument, e.g. `renv::snapshot(packages = c("httpgd", "languageserver", "here")`.  Alternatively create a dummy .R file in your folder that imports those packages.  Per renv [FAQ](https://rstudio.github.io/renv/articles/faq.html#why-isnt-my-package-being-snapshotted-into-the-lockfile), renv will not commit packages to the lockfile unless they are actually invoked by code in the project.