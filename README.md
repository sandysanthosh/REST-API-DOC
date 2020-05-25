## REST API DOCUMENTATION

### Representational state transfer 

REST != HTTP

Resources are decoupled from their representation variety of formats 

       - HTML, XML, plain text, PDF, JPEG, JSON

HTTPS Methods:

        GET 
        PUT
        POST 
        DELETE
        
HTTPS STATUS CODE:

        200 OK
        201 OK created
        301 Moved t new url
        304 Not modified
        400 Bad reuquest
        401 Unauthorized
        404 Not found
        500 Internal server error

Learn REST API:

https://developer.github.com/v3/#pagination

To Test REST API you can use POSTMAN:


To Test all the user:

https://api.github.com/users

To Test Specific user:

https://api.github.com/users/sandysanthosh


### Fake Rest API:

Resources:

https://jsonplaceholder.typicode.com/

                            /posts	       100 posts
                            /comments	500 comments
                            /albums	100 albums
                            /photos	5000 photos
                            /todos  	200 todos
                            /users        10 Users
                            
Routers:

https://jsonplaceholder.typicode.com/

                            GET	/posts
                            GET	/posts/1
                            GET	/posts/1/comments
                            GET	/comments?postId=1
                            GET	/posts?userId=1
                            POST	/posts
                            PUT	/posts/1
                            PATCH	/posts/1
                            DELETE	/posts/1
                            
  TO LIMIT:
  
  https://jsonplaceholder.typicode.com/todos?_limit=5
  
  
 
 #### Follow US</t><a href="http://starwalt.in/Blogs/index.html">Starwalt</a>
 
 


