# JavaScript cookie manager
The JavaScript cookie manager aims to allow web developers to easily manage cookies by using helper functions.

<hr/>

## Download

<a href="https://github.com/RayLabz/JS-CookieManager/raw/master/CookieManager.zip">DOWNLOAD HERE</a>

Extract in your website folder, in a folder called "js".

## Usage

##### Import
You can import the cookie manager in your code using:
```js
<script src="js/Cookies.js"></script>
```

##### Defining cookie names

You can define a cookie name inside the Cookies class (located inside Cookies.js):

```js
class Cookies {

    //TODO - Declare your cookies here and access their names using Cookies.<COOKIE_NAME>
    static COOKIE_NAME = "myCookie"; //Sample cookie declaration
    
    //Declare your own cookies here...    

}
```

The Cookies class allows you to organize your cookie names in the same place. This will allow you to group cookie names together for easier reference.
 Alternatively, you can create cookie names anywhere else in your code.
 
##### Setting cookie values
 
You can use ```Cookies.setCookie()``` to set a cookie value by providing the cookie name and value:

```js
Cookies.setCookie(Cookies.COOKIE_NAME, "aValue");
```

The ```setCookie()``` function will create cookies with an expiration period of 30 days by default. To create 
cookies with a custom expiration period, you can use ```setCookieWithExpiration()``` and provide the number of days to expiration as an extra parameter:

```js
Cookies.setCookieWithExpiration(Cookies.COOKIE_NAME, "aValue", expirationDays);
```


##### Getting cookie values

You can retrieve the value of a cookie by using ```getCookie()``` and providing its name as a parameter:

```js
let cookieValue = Cookies.getCookie(Cookies.COOKIE_NAME);
```

If a cookie is not set, the ```getCookies()``` method will return ```null```.

##### Check if cookie exists

You can check if a given cookie exists using ```cookieExists()``` and providing the name of the cookie as a parameter:

```let cookieExists = Cookies.cookieExists(Cookies.COOKIE_NAME);```

The ```cookieExists()``` method will return a boolean value (true if it exists, false otherwise).

##### Deleting cookies

To delete a cookie, you can use the ```deleteCookie()``` method and provide the cookie's name to delete as a parameter:

```js
Cookies.deleteCookie(Cookies.COOKIE_NAME);
```

##### Resetting all cookies

You can reset (delete) all cookies stored by your website at once, using ```resetCookies()```:

```js
Cookies.resetCookies();
```

<hr/>

## Acknowledgements

Part of the code used to create this manager class has taken from W3Schools:

[JavaScript Cookies (W3Schools)](https://www.w3schools.com/js/js_cookies.asp)
