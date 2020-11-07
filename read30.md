# Readings: Application State With Redux

### Review, Research, and Discussion

![source](https://hackernoon.com/hn-images/0*cntBtPADjE2ykLSP.png)

### What are the advantages of storing tokens in “Cookies” vs “Local Storage”

## Local Storage
#### Pros: It's convenient.

It's pure JavaScript and it's convenient. If you don't have a back-end and you're relying on a third-party API, you can't always ask them to set a specific cookie for your site.
Works with APIs that require you to put your access token in the header like this: Authorization Bearer ${access_token}.
Cons: It's vulnerable to XSS attacks.

An XSS attack happens when an attacker can run JavaScript on your website. This means that the attacker can just take the access token that you stored in your localStorage.

An XSS attack can happen from a third-party JavaScript code included in your website, like React, Vue, jQuery, Google Analytics, etc. It's almost impossible not to include any third-party libraries in your site.

## Cookies
#### Pros: The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks as localStorage.

If you're using httpOnly and secure cookies, that means your cookies cannot be accessed using JavaScript. This means, even if an attacker can run JS on your site, they can't read your access token from the cookie.
It's automatically sent in every HTTP request to your server.
Cons: Depending on the use case, you might not be able to store your tokens in the cookies.

Cookies have a size limit of 4KB. Therefore, if you're using a big JWT Token, storing in the cookie is not an option.
There are scenarios where you can't share cookies with your API server or the API requires you to put the access token in the Authorization header. In this case, you won't be able to use cookies to store your tokens.

[source](https://dev.to/cotter/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-15id)

### Explain 3rd party cookies.

Third-party cookies are cookies that are set by a website other than the one you are currently on.

[source](https://cookie-script.com/all-you-need-to-know-about-third-party-cookies.html#:~:text=Third%2Dparty%20cookies%20are%20cookies,see%20which%20websites%20he%20visited.)

### How do pixel tags work?

What is a tag/pixel?

A tag (or often called pixel) is a short snippet of javascript (code) that does something on your website. In the context of marketing/advertising tags and pixels, they are often collecting some information about the visitor to a website and their behavior on the site. This is then sent back to the respective marketing/advertising platform to be processed and reported.

[source](https://taginspector.com/articles/marketing-tags-and-pixels-form-and-function/#:~:text=A%20tag%20(or%20often%20called,their%20behavior%20on%20the%20site.)

*cookies*

Cookies are usually small text files, given ID tags that are stored on your computer's browser directory or program data subfolders. Cookies are created when you use your browser to visit a website that uses cookies to keep track of your movements within the site, help you resume where you left off, remember your registered login, theme selection, preferences, and other customization functions.The website stores a corresponding file(with same ID tag)to the one they set in your browser and in this file they can track and keep information on your movements within the site and any information you may have voluntarily given while visiting the website, such as email address.

[source](https://www.allaboutcookies.org/cookies/)

*authorization*

Authorization is a process by which a server determines if the client has permission to use a resource or access a file. 

[source](https://www.bu.edu/tech/about/security-resources/bestpractice/auth/#:~:text=Authorization%20is%20a%20process%20by,resource%20or%20access%20a%20file.&text=Most%20of%20the%20web%20pages,require%20no%20authentication%20or%20authorization.)

*access control*

We can determine the abilities of a user based on the access granted to theri account: this allows management of credentials to be determined to better be able to control who is able to do what to our data.

*conditional rendering*

With React, we can build Single Page Applications that are dynamic and highly interactive. One way we fully utilize such interactivity is through conditional rendering.

Conditional rendering as a term describes the ability to render different UI markup based on certain conditions. In React-speak, it is a way to render different elements or components based on a condition.

[source](https://www.digitalocean.com/community/tutorials/7-ways-to-implement-conditional-rendering-in-react-applications)



