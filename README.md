# DOM-Bases-XSS-Lab
DOM-based cross-site scripting (DOM-XSS) is a client side vulnerability where 
attacker-controlled data is interpreted by the browser in a way that modifies the 
page’s DOM (Document Object Model) and allows script execution. Unlike reflected 
or stored XSS, the dangerous transformation happens entirely in the browser. The 
server typically returns the same HTML to everyone, and the client-side JavaScript 
takes untrusted input (from the URL, fragment etc.) and writes it into the page using a 
“sink” that interprets it as code or HTML.
