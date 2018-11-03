# Run node on port 80
This script runs a simple **Hello World** at port 80.

## Usage
Run this command:

    sudo node app.js
You can then access your application by entering **localhost** in your browser or by accessing your device's public IP.

## Troubleshooting
### Error: listen EACCES 0.0.0.0:80
This error occurs when we run `node app.js`  as is without elevated privileges. We need elevated privilege since ports below 1024 can only be opened in that way. To fix this, simply run the same command with `sudo`.

    sudo node app.js

### Error: listen EADDRINUSE 0.0.0.0:80
This error occurs when something else is already bound to port 80. To fix this, simply kill the process using port 80. To do this, first find the process's ID (PID) via `ps ax | grep <process_name>`. Then, kill that process via `sudo kill <PID>`.

## Sources:
 - [Start node js on port 80
 ](quora.com/What-are-the-simplest-steps-to-start-node-js-work-on-port-80-in-Windows)
 - [Connect to localhost:3000 from another computer
 ](stackoverflow.com/questions/30712141/connect-to-localhost3000-from-another-computer-expressjs-nodejs)
