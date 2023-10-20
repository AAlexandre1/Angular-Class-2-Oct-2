Use the terminal or CMD to create the project
go to the folder you want the project in
ng new projectname --no-strict
select no for routing
select css
cd into the project folder with cd project name
open the project in VSCode by entering
code .
make sure there is a space between the word code and the period
Immediately create a github repository by clicking source control
Make sure you cd into the project in the terminal in VSCode before continuing
Then add bootstrap by typing
npm install --save bootstrap@4 or 
npm install bootstrap@4 
typically you may not need to use --save
Use the version of the tutorial you are following
Go to angular.json file
in the styles array under build enter the path for bootstrap under node modules. 
"node_modules/bootstrap/dist/css/bootstrap.min.css"
Use a bootstrap component in app.component.html to test if bootstrap is working
<div class="container">
  <div class="row">
    <div class="col-md-12">
      <h1>I'm working.</h1>
    </div>
  </div>
</div>

enter ng serve 
Go to localhost/4200 or whichever port it tells you to
see if bootstrap is working
Switch to a new terminal in VSCode since that terminal will run updates to your code

create
div.container
div.row
div.col-md-10
h1 BookIt

make sure you cd into the project book-it
DO NOT go into any of the folders in the terminal

create new components
the g c stand for generate component
ng g c bookshelf
ng g c library

create a child component in the bookshelf
ng g c bookshelf/book-list
ng g c bookshelf/book-details
ng g c bookshelf/book-results
ng g c bookshelf/book-search

create a shared folder with a navigation component and a book component
shared is not a component it is a folder to hold the components that will be used in multiple places
ng g c shared/navigation
ng g c shared/book

under src folder under app folder under shared folder
in app.compnent.html

build out components
div.container
<app-navigation>
div.row


under bookshelf go to html
div.row.justify-content-between
div.col-md-6
h1 My saved books
<app-book-list>

Under booklist html
div.row.mb-3
div.col-12
app-book*3

go to library component html
div.row
div.col-md-6
h1 API library Results
div.col-md-6
app-book-search

book results html
same as booklist

copy bootstrap navigation bar

[class.show] = "show"
class.classname
class is an attribute of the div
classname does not matter the second show is the bootstrap class that we are toggling

We tell angular what a book should look like using a class/model
add the properties under the constructor

make sure to import components when using them in other componenets

After coding enter a commit message and commit then sync changes
Or
in the VSCode terminal
git status
git add -A
git status
git commit -m "message"
git push
