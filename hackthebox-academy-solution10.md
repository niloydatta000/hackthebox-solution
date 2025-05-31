 # Hack The Box Solution  10

### 1. Find a way to start a simple HTTP server inside Pwnbox or your local VM using "npm". Submit the command that starts the web server on port 8080 (use the short argument to specify the port number).
**Answer:** RUN  `npm install -g http-server` command to install **http-server** module
```bash
sudo npm install -g http-server
if [ ! -d "httpserver" ]; then
	mkdir "httpserver"
fi
cd ./httpserver
http-server -p 8080
```
Your answer is `http-server -p 8080`.

### 2. Find a way to start a simple HTTP server inside Pwnbox or your local VM using "php". Submit the command that starts the web server on the localhost (127.0.0.1) on port 8080.
**Answer:** RUN `php -S 127.0.0.1:8080` command
```bash
php -S 127.0.0.1:8080
```
Your answer is `php -S 127.0.0.1:8080`
