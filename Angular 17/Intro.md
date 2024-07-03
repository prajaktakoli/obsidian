- How web apps work?
- search engines use web crawlers to access the source html of web site, they extract content from website and try to access links and follow the links until new links are found on the page.
In case of Angular, the content is dynamic, so cannot find any links.
But most companies prefer server side rendering for SEO for optimization
----------
When you want SPA, but dont want to load the application all at once, which cab be redundant if the role does not want the page etc, this can be achieved by modules.
Modules - Separate your project into section and use these sections to load specific parts only when necessary. That is divide applications into parts and then use lazy loading to load only when it is required.
---------------------------------------------------------------------------------------------
Component - It comprises of class, HTML and CSS
Interpolation - way to bind data between HTML and its class. 
- use {{}} to display data dynamically.
Selector - The `selector` property of the component configuration gives you a name to use when referencing the component in another template.
Standalone component - can be used independently without needing to be a part of angular module
- to create standalone components use below syntax
-- ng generate component my-standalone-component --standalone
set **standalone: true**: This property makes the component standalone.
