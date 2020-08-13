# AP FAQ : Build Optimization

Recently Frontend builds are mostly failing to build , because of some memory issue.

so I followed below approaches to fix them temporarily ,

I have removed Few modules which were not required and few libraries which were not being used by any Modules.

I also changed few build commands in Employee , so that both employee and citizen module will built by same commands , Its dependencies will remain same.

In the package.json of root folder ie web/rainmaker/package.json

In Scripts removed egov-boilerplate dependency.

In Dependency `file-saver` and `js-file-download` was removed \(none of the module uses these files just import was found in few files that was also removed \)

In the package.json of Employee Package ie web/rainmaker/packages/**employee**/package.json

In Dependency removed `egov-boilerplate` , `jsonpath-plus`,`print-js` ,`react-jquery-datatables`,`react-responsive-carousel` libraries

In scripts changed from npm to yarn \(similar to citizen module\) like in

`"watch-css"` command from `"npm run build-css` to `"yarn run build-css` ,

`"start"` command from `"npm-run-all -p watch-css` to `"run-p watch-css`

`"build"` command from `"npm-run-all build-css` to `"run-s build-css`

and In devDependencies removed `@storybook/addon-knobs ,` `"@storybook/react"` `storybook-addon-material-ui` libraries

In the package.json of Citizen Package ie web/rainmaker/packages/**citizen**/package.json

In Dependency removed `egov-boilerplate` , `jquery`,`jsonpath-plus`,`print-js` ,`react-jquery-datatables`,`react-responsive-carousel`,`npm-run-all"` libraries

in devDependencies removed `@storybook/addon-knobs ,` `"@storybook/react"` `storybook-addon-material-ui` libraries

Note few libraries like `print-js` was found in two three places in few modules but not used , remove them by refering same file from master branch.

