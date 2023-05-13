## dom interface

###### 1. HTML and XML documents are represented in a **Tree** structure using the Object model for easy manipulation with programming languages.<br> 
###### 2. Dom interface doesn't rely on a specific language.<br> 
###### 3. JavaScript is built-in object and can be used directly without processing.<br> 


## host environment

###### 1. The platform that JavaScript runs on is called the host. Each platform provides specific functionality, which is called the host environment.
###### 2. The Browser Object Model (BOM) is an additional object provided by the host environment (the browser) to control everything other than the document.

###### 1) navigator object: Provides information about the browser and operating system.
######    navigator.userAgent; 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.5249.207 Whale/3.17.145.18 Safari/537.36'<br> 
###### 2) Information about the operating system the browser is running on
######    navigator.platform; 'MacIntel'<br> 
###### 3) location object: Allows us to read the current URL and change it (redirect).
######    location.href<br> 

<img src="https://github.com/eileenjang/dom-basic/assets/82510378/1c754ad6-a25b-45c1-b0f4-a000d7c09ff6" width=400px height=300px>
