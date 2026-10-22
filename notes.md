# HTTP observations (Lab 4, Task 1)
 
| Question | My answer |
|----------|-----------|
| Request method for index.html | GET |
| Status code with Disable cache ticked |200 |
| Status code on a normal reload | 304 |
| Status code for /nothing-here.html | 404 |
| Value of the Content-Type response header | text/html; charset=utf-8 |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |
 
## Why is this address http and not https?
HTTPS encrypts data transferred across a network to protect against eavesdropping.Because 127.0.0.1 represents localhost on your local machine, network traffic never leaves your computer, eliminating the need for SSL/TLS encryption during local testing.
... (two sentences)
