- How web apps work?
- search engines use web crawlers to access the source html of web site, they extract content from website and try to access links and follow the links until new links are found on the page.
In case of Angular, the content is dynamic, so cannot find any links.
But most companies prefer server side rendering for SEO for optimization
----------
When you want SPA, but dont want to load the application all at once, which cab be redundant if the role does not want the page etc, this can be achieved by modules.
Modules - Separate your project into section and use these sections to load specific parts only when necessary. That is divide applications into parts and then use lazy loading to load only when it is required.