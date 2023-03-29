django uses MTV, pattern it is essentially:
- `Model`
- `Template`
- `View`

# Why MTV??
> In our interpretation of MVC, the “view” **_describes the data that gets presented to the user. It’s not necessarily how the data looks, but which data is presented_**. The view describes which data you see, not how you see it. It’s a subtle distinction.
So, in our case, a “view” is the Python callback function for a particular URL, because that callback function describes which data is presented.

> Furthermore, it’s sensible to separate content from presentation – which is where templates come in. In Django, a “view” describes which data is presented, but a view normally delegates to a template, which describes how the data is presented.

# MVC
Compared to MVC:
- `Template` is just a `View`
- `View` is a `controller`
In other words, in Django views are called templates, and controllers are called views. Hence our HTML code will be in templates and Python code will be in views and models.

`Models`: Models represents how data is organized in the database.   
In other words, in MVC pattern we use models to define our database tables as well as the relationships between them.

`Views`: A view is what you see when you visit a site. For example, a blog post, a contact form etc, are all examples of views.   
A View contains all the information that will be eventually sent to the client i.e a web browser. Generally, views are HTML documents.

`Controllers`: Controller controls the flow of information. When you request a page that request is passed to the controller then it uses programmed logic to decide what information is needed to pull from the database and what information should it pass to the view.  
The controller is the heart of the MVC architecture because it acts as a glue between models and views.

![image](https://user-images.githubusercontent.com/63263301/228045488-74311544-2dcb-46ee-b6df-23c184055aca.png)

Here is the basic flow of MVC:
- Web browser or client sends the request to the web server, asking the server to display a blog post.
- The request received by the server is passed to the controller of the application.
- The controller asks the model to fetch the blog post.
- The model sends the blog post to the controller.
- The controller then passes the blog post data to the view.
- The view uses blog post data to create an HTML page.
- At last, the controller returns the HTML content to the client.

# Django MTV
Django follows MVC pattern very closely but it uses slightly different terminology. Django is essentially an MTV (Model-Template-View) framework. Django uses the term Templates for Views and Views for Controller.   
In other words, in Django views are called templates and controllers are called views.   
Hence our HTML code will be in templates and Python code will be in views and models.
