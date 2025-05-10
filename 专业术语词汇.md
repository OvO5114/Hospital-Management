<div align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=FFB13C&size=50&width=1000&height=80&lines=Welcome-to-Hospital-Management-App"/>
</div>

NextAuth：是专为 Next.js 应用设计的一个认证库，它的功能十分强大，能够轻松实现各种认证方式，像 OAuth、JWT、凭证认证等都不在话下。借助它，开发者可以用简洁的代码快速搭建起安全可靠的认证系统，大大降低了开发成本。
NextAuth: A specialized authentication library crafted for Next.js applications, it offers robust capabilities to implement a wide array of authentication methods, including OAuth, JWT, and credential - based authentication. With NextAuth, developers can swiftly set up a secure and dependable authentication system using concise code, which significantly cuts down on development expenses.

credentialsProvider：是 NextAuth 里的一个重要组件，主要用于处理基于用户名和密码的认证。当用户登录时，系统会调用相应的授权函数对用户输入的凭证进行验证，验证通过后才会允许用户访问受保护的资源。
CredentialsProvider: A vital component within NextAuth, its main responsibility is to handle username and password - based authentication. During the user login process, the system invokes the corresponding authorization function to verify the credentials provided by the user. Only after successful verification will the user be granted access to protected resources.

MongoDBAdapter：是 NextAuth 与 MongoDB 之间的桥梁，它遵循 NextAuth 的适配器接口规范，负责将认证数据存储到 MongoDB 数据库中。通过使用这个适配器，开发者可以方便地在 MongoDB 中管理用户信息、会话数据等。
MongoDBAdapter: It serves as a bridge between NextAuth and MongoDB. Adhering to NextAuth's adapter interface specifications, it takes charge of storing authentication data into the MongoDB database. By utilizing this adapter, developers can effortlessly manage user information, session data, and more in MongoDB.

JWT：是一种在网络应用间传递声明的安全方式，它由三部分组成，分别是头部、载荷和签名。在认证场景中，服务器会生成一个 JWT 并发送给客户端，客户端在后续的请求中都需要携带这个 token，服务器通过验证 token 的签名和有效期来确认用户身份。
JWT (JSON Web Token): This is a secure means of transferring claims between web applications. Comprising three parts - the header, payload, and signature. In the context of authentication, the server generates a JWT and sends it to the client. Subsequently, the client must carry this token in all subsequent requests. The server validates the token's signature and expiration date to confirm the user's identity.

bcrypt：是一种专门用于密码哈希的算法，它的一大特点是引入了盐值（salt）和计算成本因子（cost factor），这使得它能够有效抵御彩虹表攻击和暴力破解。在存储用户密码时，我们不应该直接存储明文，而是使用 bcrypt 对密码进行哈希处理后再存储。
bcrypt: A dedicated password - hashing algorithm. It incorporates a salt value and a computational cost factor, which makes it highly effective in defending against rainbow table attacks and brute - force cracking. When storing user passwords, instead of saving the plain text, it is advisable to use bcrypt to perform hash processing on the password before storage.

authorize：是认证流程中的一个关键环节，主要任务是验证用户提供的凭证（如用户名和密码）是否有效。在 NextAuth 的 CredentialsProvider 中，需要开发者自定义 authorize 函数，在这个函数里实现具体的验证逻辑，比如查询数据库、比对密码哈希值等。
authorize: A crucial step in the authentication workflow, its core task is to check whether the credentials (such as username and password) supplied by the user are valid. In NextAuth's CredentialsProvider, developers are required to customize the authorize function and implement specific verification logic within it, like querying the database and comparing password hashes.

findOne：是 MongoDB 数据库操作中的一个基本方法，其作用是从集合中查找并返回满足指定条件的第一个文档。在认证流程中，我们经常会使用这个方法根据用户邮箱来查找对应的用户记录。
findOne: A fundamental method in MongoDB database operations. Its function is to search a collection and return the first document that meets the specified criteria. In the authentication process, we often use this method to look up user records based on the user's email.

connectToDatabase：是一个自定义函数，用于建立与 MongoDB 数据库的连接。为了提高性能，我们通常会采用连接池技术，避免每次数据库操作都重新建立连接。
connectToDatabase: A user - defined function used to establish a connection to the MongoDB database. To enhance performance, we usually adopt a connection pool technique to avoid creating a new connection for every database operation.

async：是 ES2017 引入的语法糖，它基于 Promise，目的是让异步代码看起来更像同步代码，从而提高代码的可读性和可维护性。在处理数据库操作、API 请求等异步任务时，这种语法非常实用。
async: Syntax sugar introduced in ES2017, it is built on top of Promises. The aim is to make asynchronous code resemble synchronous code, thereby enhancing the readability and maintainability of the code. This syntax is extremely useful when dealing with asynchronous tasks such as database operations and API requests.

req：在 Node.js 的 HTTP 服务器环境中，req（request）代表客户端发送的 HTTP 请求，通过它我们可以获取请求头、请求体、查询参数等信息。
req: In the HTTP server environment of Node.js, req (request) represents the HTTP request sent by the client. Through it, we can obtain information like the request headers, request body, and query parameters. 

res：在 Node.js 的 HTTP 服务器环境中，表示服务器返回的 HTTP 响应，我们可以通过它设置响应状态码、响应头和响应体等。
res: In the HTTP server environment of Node.js, res (response) stands for the HTTP response returned by the server. We can use it to set the response status code, response headers, and response body.

POST：是 HTTP 协议中的一种请求方法，主要用于向服务器提交数据，比如提交表单数据、上传文件等。与 GET 请求不同，POST 请求会将数据包含在请求体中，而不是直接暴露在 URL 中，因此更适合传输敏感信息。
POST: One of the HTTP request methods, mainly used for submitting data to the server, such as form data and file uploads. Different from GET requests, POST requests enclose the data within the request body instead of exposing it directly in the URL. Hence, it is more suitable for transmitting sensitive information.

hash：在密码学领域，hash 指的是将任意长度的输入数据通过哈希函数转换为固定长度的输出（哈希值）的过程。哈希函数具有单向性，也就是说无法通过哈希值反推出原始数据，而且对于不同的输入，哈希函数几乎不可能产生相同的输出（即哈希冲突的概率极低）。在用户认证中，我们通常使用哈希函数来安全地存储密码。
hash: In the field of cryptography, hashing refers to the process of transforming input data of any length into a fixed - length output (hash value) through a hash function. Hash functions are one - way, meaning it is impossible to derive the original data from the hash value. Moreover, for different inputs, it is highly improbable for a hash function to produce the same output (the probability of a hash collision is extremely low). In user authentication, we typically use hash functions to store passwords securely.

status：在 HTTP 响应中表示状态码，它是一个三位数字，用于表示 HTTP 请求的结果。常见的状态码有 200（成功）、400（错误请求）、401（未授权）、403（禁止访问）、404（未找到）、500（服务器内部错误）等。
status: In an HTTP response, the status code is a three - digit number that indicates the outcome of an HTTP request. Common status codes include 200 (success), 400 (bad request), 401 (unauthorized), 403 (forbidden), 404 (not found), 500 (internal server error), etc.

uuidu4：是生成通用唯一识别码（UUID）的一种算法，它基于随机数生成 UUID。UUID 是一个 128 位的数字，通常用 36 个字符的字符串表示，格式为 8-4-4-4-12。在分布式系统中，UUID 经常被用来唯一标识资源，避免 ID 冲突。
uuidv4: An algorithm for generating Universally Unique Identifiers (UUIDs). It generates UUIDs based on random numbers. A UUID is a 128 - bit number, usually represented as a 36 - character string in the format 8 - 4 - 4 - 4 - 12. In distributed systems, UUIDs are frequently used to uniquely identify resources and prevent ID conflicts.

json：（JavaScript Object Notation）是一种轻量级的数据交换格式，它基于 JavaScript 对象语法，但又独立于编程语言。JSON 格式简洁、易于阅读和编写，同时也很容易被机器解析和生成，因此在 Web 应用中被广泛用于数据传输。
json: (JavaScript Object Notation) A lightweight data interchange format. It is based on JavaScript object syntax but is independent of programming languages. JSON is concise, easy to read and write, and can be easily parsed and generated by machines. Therefore, it is widely used for data transmission in web applications.

express：是一个基于 Node.js 的轻量级 Web 应用框架，它提供了简洁的 API 来处理 HTTP 请求、路由、中间件等，帮助开发者快速构建 Web 应用和 API。
express: A lightweight web application framework built on Node.js. It offers a simple API to handle HTTP requests, routing, middleware, etc., assisting developers in quickly building web applications and APIs.

post：在 Express 框架中，post 是用于定义 HTTP POST 请求处理程序的方法。通过它，我们可以为特定的 URL 路径设置回调函数，当客户端发送 POST 请求到该路径时，对应的回调函数就会被执行。
post: In the Express framework, post is a method used to define HTTP POST request handlers. By using it, we can set up callback functions for specific URL paths. When a client sends a POST request to such a path, the corresponding callback function will be executed.

Router：是 Express 框架中的一个功能模块，它允许我们将路由逻辑组织成独立的模块，使代码结构更加清晰。通过使用 Router，我们可以将不同功能的路由处理分开管理，提高代码的可维护性。
Router: A functional module in the Express framework. It enables us to organize routing logic into independent modules, making the code structure clearer. By using Router, we can manage different routing handlers separately, which improves the maintainability of the code.

routes：指的是应用程序中定义的路由集合，也就是客户端请求的 URL 路径与服务器端处理函数之间的映射关系。合理组织路由可以使应用的功能结构更加清晰，便于开发和维护。
routes: Refers to the collection of routes defined in an application, that is, the mapping relationship between the URL paths requested by the client and the processing functions on the server side. Properly organizing routes can make the functional structure of the application more distinct and facilitate development and maintenance.

<!-- by 莫杰 -->
