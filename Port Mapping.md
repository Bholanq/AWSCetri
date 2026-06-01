![[Pasted image 20260601082203.png|289]]
Port 5000 of the container is not the same a port 5000 of the local machine.
```
PS C:\Users\akash\DOCKER_TUT> docker run -p 5000:5000 --name flask_container flask_image
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:500
 * Running on http://172.17.0.2:500
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 274-396-005

```