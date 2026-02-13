# Browsers and how they work?

When you type a website address and hit Enter, a bunch of things happen behind the scenes:

1. **Find the Address (DNS):**  
First, your browser checks its "address book" (called DNS) to find the real location of the website. For example, "`google.com`" is actually a number like 216.58.211.46. The browser finds this number.

2. **Connect to the Server (TCP/IP):**  
Once it knows the address, it "shakes hands" with the server (TCP handshake). It’s like saying, "Hey, I’m here. Can I get the page?" If it's a secure site (HTTPS), they also agree on a secret way to talk safely.

3. **Ask for the Page (HTTP Request):**  
The browser sends a request: "Please send me the homepage." The server understands this and gets ready to reply.

4. **Get the Code (HTML, CSS, JS):**  
The server sends back the website files—usually HTML (the structure), CSS (the design), and JavaScript (the interactive stuff).

5. **Build the Page (Rendering):**  
The browser reads the HTML and starts building the page like a house:

    First, it creates the structure (like putting up walls).

    Then, it adds styles (like painting and decorating).

    Finally, it runs JavaScript to make things move or respond when you click.

6. **Keep Communicating:**  
If the page needs more stuff (like images or videos), the browser asks for them separately. And if you click a link, the whole process starts again!