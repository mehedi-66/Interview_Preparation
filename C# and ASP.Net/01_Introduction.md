
# Introduction of ASP.net & C#

### Asp.net Page Life cycle 

![ASP.Net Page Life cycle](https://drive.google.com/uc?export=view&id=1cMGoj0hqphDdMwvjTVQV8FmJpjQE0Rfu)

### ASP.Net Application Life Cycle 

![MVC 2 Life Cycle ](https://drive.google.com/uc?export=view&id=1ePzaIRej4lVJVixqrGGulGSlSKnNxgbu)

- Applicaiton Start => When user request to server start.cs
- Object Creatation  => HttpContext, HttpRequest (user cookies, sesion, browser info), HttpReponse (send to client) this type of object are created 
- HttpApplication Creation => two application News and Card order each application work respectively 
- Dispose => clear the unused resocers 
- Application End =>  applicaiton finaly uloaded from the memory 


### MVC Life Cycle 

![MVC Life Cycle ](https://drive.google.com/uc?export=view&id=1140etNMDvQusPt6mSUohbBlywsWa1yEp)

![MVC 2 Life Cycle ](https://drive.google.com/uc?export=view&id=1bZCpZDTSS9YLP1zZQih1PTyBYJEytuMg)

- First request come from web browser 
- Router Router Receive the request
- Initialize the cotroler 
- TempData
- Action 
- Respnse view or Return Result 
