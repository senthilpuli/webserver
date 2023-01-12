# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer , BaseHTTPRequestHandler
content="""
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class myhandler(BaseHTTPRequestHandler):
     def do_GET(self):
         self.send_response(200)
         self.send_header('content-type','text/html; charset=utf-8')
         self.end_headers()
         self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running....")
httpd.serve_forever()
```
## OUTPUT:
## server side output:
![output](/WhatsApp%20Image%202023-01-12%20at%2010.16.03%20AM%20(1).jpeg)
## client side output:
![output](/WhatsApp%20Image%202023-01-12%20at%2010.16.03%20AM.jpeg)
## RESULT:
The program is executed succesfully
