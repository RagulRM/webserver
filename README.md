# Developing a Simple Webserver
## AIM:

To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1:

HTML content creation
### Step 2:

Design of webserver workflow
### Step 3:

Implementation using Python code
### Step 4:

Serving the HTML pages.
### Step 5:

Testing the webserver
## PROGRAM:
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>NAME: PRANAVE B</h1>
<H1>REF NO: 21500582<H1>
<H1>DEPT: AI&ML<H1>
</body>

</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8080)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
~~~
## OUTPUT:
## server output:
![image](https://github.com/RagulRM/webserver/assets/121609342/04073d08-55f1-45b1-b742-4c93a201fb01)

## Client Output:
![Untitled](https://github.com/RagulRM/webserver/assets/121609342/c08a9bee-4d21-4de6-a4dd-134fe1e86231)


## RESULT:
<H4>THE WEB SERVER HAS BEEN SUCCESSFULLY CREATED<H4>
