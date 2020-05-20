# Day 13 Readings


## Sending Form Data MDN Docs
- An HTML form servesas a simple way to create HTTP requests to send data to a server from the client. Allow information to be taken from the user to the server.
- The action attribute can used to send the data to different locations, either absolute urls or relative ones. If no action is defined it will send data tot he page it's currently on. HTTPS urls will encrypt the data if the action is sent there, even data coming from insecure HTTP connections, but HTTP urls in the action field will cause the data to remain unencrypted and cause the browser to display a security warning.
- The method attribute define show data is sent, the most common choices being get and post. The get methods will ask the server to send back a given resource, and key value pairs from the form to be displayed in the search field of the browser. The post method allowx the browser to talk to the server when asking for a response that takes data provided in the body of the HTTP into account.
- These requests can be viewed in the Network tab of the developer tools. 
- Each programming language has different technologies and frameworks for handling data sent back from forms, Express is most common for JS.
- Adding and enctype to a form allows the type of encoding that the data will undergo. For instance, file content can be sent as "multipart/form-data" w/ input type=file controls.
- HTML forms are by far the most common server attack vectors, problems come not from the forms themselves but how the data is handled on the server end. Advice given in the docs:
  -Escape potentially dangerous characters. The specific characters you should be cautious with vary depending on the context in which the data is used and the server platform you employ, but all server-side languages have functions for this. Things to watch out for are character sequences that look like executable code (such as JavaScript or SQL commands).
  - Limit the incoming amount of data to allow only what's necessary.
  - Sandbox uploaded files. Store them on a different server and allow access to the file only through a different subdomain or even better through a completely different domain.