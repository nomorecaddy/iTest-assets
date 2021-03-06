### Project Information:
Project: Documentation Generator  
Description: Generate project documentation, for Git repository, from QuickCall and Procedure libraries  
Category: library  
Class: Community  
  
___
3 Procedure Libraries in project://ui_documentation
### Library: project://ui_documentation/test_cases/documentation.fftc
___
Headline: Documentation Generator
Description:  
This test case will generate documentation for QuickCall and Procedure libraries and optionally Response Maps. The Headline and Description should be completed for General Information and all procedures. Procedure arguments should also have a description.  
  
Parameters:  
changeDate - Only projects which have changed since that date will have the documentation regenerated. Only .fftc, .ffrm and readme.txt files are checked for change.  
  
uriDocumentationList - If specified and file exists, only the projects listed in the file will be updated, regardless of the change date. Each line, in the file, should be in this format:  
  project://<project name>  
  
includeResponseMaps - If true, inlude a list of response maps along with heading and description.  
  
  
### getProjectList
Return a list of project URI's within the current workspace
### getUriList
Return a list of test case URI's within a given project URI

Argument | Description
------------ | -------------
uriPath | URI of project
### getLibList
Get list of QuickCall Libraries and Procedure Libraries from given list of test case URI's

Argument | Description
------------ | -------------
uriList | List of file URI's
### createFiles
Create HTML and MD files

Argument | Description
------------ | -------------
uriPath | URI to project
### writeLibrariesFound
Build a separate list of QuickCall and Procedure libraries

Argument | Description
------------ | -------------
uriPath | URI to project
### writeInfo
Append to HTML and MD: procedure names, descriptions and arguments

Argument | Description
------------ | -------------
uriPath | URI to project
uriList | List of library URI's 
### writeRMInfo
Append to HTML and MD: procedure names, descriptions and arguments

Argument | Description
------------ | -------------
uriPath | URI to project
uriList | List of response map URI's 
### fileChanged

Argument | Description
------------ | -------------
uri | URI of file to check
dateString | Change date in the form of mm/dd/yy or mmdd/yyyy.<br>Relative time strings can also be used.<br>See Tcl clock scan documentation for more info.
### Library: project://ui_documentation/test_cases/readme_check.fftc
___
Headline: Check for missing documentation/readme.txt
Description:  
Scan the workspace to detect any projects that don't have readmet.txt  
  
Fail if no documentation/readme.txt found.  
Fail if documentation/readme.txt is empty.  
Fail if information is missing. Must be as follows:  
  
Project: <name>  
Description: <Some wording about what the project does or is used for>  
Category: <"library", "automation", or "framework">  
Class: <"Community", "Tested by Spirent", "Reference">  
  
### Library: project://ui_documentation/test_cases/unit_test.fftc
___
Headline: Unit Test - Documentation Generator
Description:  
Add stuff here to test the Documentation Generator tool.  
  
### procWithMultilineArgDescription

Argument | Description
------------ | -------------
arg1 | Line 1
arg2 | Line 1<br>Line 2<br>Line 3
