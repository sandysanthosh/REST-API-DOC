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
        PATCH

HTTP status codes:

        200 OK — successful read or update response
        201 Created — a new resource was created
        204 No Content — successful request with no response body
        301 Moved Permanently — resource has a new permanent URL
        304 Not Modified — cached response is still valid
        400 Bad Request — malformed or invalid request
        401 Unauthorized — authentication is missing or invalid
        403 Forbidden — authenticated caller lacks permission
        404 Not Found — requested resource does not exist
        409 Conflict — request conflicts with current resource state
        500 Internal Server Error — unexpected server failure

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
  
  ### Download Axios folder and run index.html:
  
  ![axios](https://user-images.githubusercontent.com/11579239/82775884-a9bfe600-9e66-11ea-9364-daef55b3ac91.JPG)

  
@Restcontroller 
@ResponseBody
@RequestMapping
  
  
 
 #### Follow US</t><a href="http://starwalt.in/Blogs/index.html">Starwalt</a>
 
 



### Production API error handling

For a practical, consistent error format, status-code guidance, and Spring Boot implementation notes, see [REST API Error Response Standard](docs/error-response-standard.md).
