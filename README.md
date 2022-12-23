# Developing a Simple Webserver

# AIM:

Name:Harshavardhan Reddy
 Ref:2207173
# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME: Harsha Vardhan Reddy Bomma</h2>
<h2>REF.NO.:22007173</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-django</h4>
<h4>-meteor</h4>
<h4>-cakePHP</h4>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
```

# OUTPUT:
![MODEL](/WhatsApp%20Image%202022-12-23%20at%2016.42.47.jpeg)

# RESULT:

The program is executed succesfully
