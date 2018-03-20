Run Application

cd complete
gradlew clean build

cf push



This guide walks you through the process of creating a "hello world" link:/understanding/REST[RESTful web service] with Spring.

== What you'll build

You'll build a service that will accept HTTP GET requests at:

----
http://localhost:8080/greeting
----

and respond with a link:/understanding/JSON[JSON] representation of a greeting:

[source,json]
----
{"id":1,"content":"Hello, World!"}
----

You can customize the greeting with an optional `name` parameter in the query string:

----
http://localhost:8080/greeting?name=User
----

The `name` parameter value overrides the default value of "World" and is reflected in the response:

[source,json]
----
{"id":1,"content":"Hello, User!"}
----

