# What is hosting?

The article starts by clearing up one of the biggest sources of confusion for beginners: **the difference between a web page, a website, a web server, and a search engine.** It uses a brilliant analogy *a public library* to tie it all together.

Imagine a library. The **library building itself** is the **web server**; it’s a computer that stores things. Inside, you have different **sections** (Science, History, etc.). Each section is a **website**; they share the same building but have their own unique space. The **books** on the shelves are the **web pages**. Finally, the **card catalog or search index** you use to find a book is the **search engine**.

This analogy made it so easy to understand **hosting**. A **web server** is simply a computer that is “hosting” one or more websites. When you pay for hosting, you are essentially renting space on that computer. You’re putting all your website’s files *HTML documents, images, scripts* onto that server so that when someone types your domain name, the **server** can send those files to their browser.

The article emphasizes not to confuse the server with the site itself. If someone says “my website is down,” they usually mean the server hosting it isn’t responding. A single web server can host dozens of websites, just like one library has many sections.

It also draws a sharp line between the browser and the **search engine**, which is another classic mix-up. The browser is the software on your computer (like Chrome or Firefox). The search engine is a specific type of **web service** (like Google) that lives on a server. You use the browser to visit the search engine’s website.

Later, the article simplifies **how the web works technically**. When you hit Enter on a URL:

   1. Your browser sends an **HTTP request** (a "GET" command) to the web server.

   2. The server responds by sending the requested file (usually an HTML page).

   3. The browser reads that file, sees it needs more stuff (images, CSS, JavaScript), and sends more requests to the server for those files.

   4. Once it has everything, it assembles the page for you to see.

For someone studying hosting, this is the core loop. The hosting server’s job is to just sit there, listen for these requests, and send back the correct files 24/7.

The article finishes with practical advice on **searching for information** as a developer. It suggests using specific resources like MDN for documentation and Stack Overflow for coding problems. It even touches on **using AI** (like ChatGPT) for debugging or optimizing code, but with a huge **cautionary note**: AI can sound confident but be completely wrong, and it doesn’t replace actually understanding the code.

**So, what does this all mean for "hosting"?**
To summarize from this page: Hosting is the act of placing your website’s files on a web server (a computer optimized to run 24/7). That server’s sole purpose is to listen for browsers requesting those files and deliver them using HTTP. Without hosting, your website is just a folder of files on your personal laptop. With hosting, it becomes a website available to the world.

**Sources:**  
- https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Environment_setup/Browsing_the_web
