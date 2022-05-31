# HTTP Cookies

## Introduction

HTTP Cookie is some piece of data which is stored in the user's browser. HTTP cookies play a vital role in the software world. We can store users' related information in cookies and there are many other usages. In asp.net core working with cookies is made easy.

In ASP.NET, we can access cookies using httpcontext.current but in ASP.NET Core, there is no htttpcontext.currently. In ASP.NET Core, everything is decoupled and modular.
 
Httpcontext is accessible from Request object and the IHttpContextAccessor interface which is under "Microsoft.AspNetCore.Http" namespace and this is available anywhere in the application. 

## What is a cookie?

a cookie is a small text file that is stored by a browser on the user’s machine. Cookies are plain text; they contain no executable code. A web page or server instructs a browser to store this information and then send it back with each subsequent request based on a set of rules. Web servers can then use this information to identify individual users. Most sites requiring a login will typically set a cookie once your credentials have been verified, and you are then free to navigate to all parts of the site so long as that cookie is present and validated. Once again, the cookie just contains data and isn’t harmful in and of itself.

## Reading Cookie 

```
//read cookie from IHttpContextAccessor  
string cookieValueFromContext = _httpContextAccessor.HttpContext.Request.Cookies["key"];  

//read cookie from Request object  
string cookieValueFromReq = Request.Cookies["Key"];  
```

## Writing cookie 
```
/// <summary>  
/// set the cookie  
/// </summary>  
/// <param name="key">key (unique indentifier)</param>  
/// <param name="value">value to store in cookie object</param>  
/// <param name="expireTime">expiration time</param>  
public void Set(string key, string value, int? expireTime)  
{  
   CookieOptions option = new CookieOptions();  

   if (expireTime.HasValue)  
         option.Expires = DateTime.Now.AddMinutes(expireTime.Value);  
   else  
         option.Expires = DateTime.Now.AddMilliseconds(10);  
   
   Response.Cookies.Append(key, value, option);  
}   
```

## Remove Cookie
Delete the cookie by key name.
```
/// <summary>  
/// Delete the key  
/// </summary>  
/// <param name="key">Key</param>  
public void Remove(string key)  
{  
      Response.Cookies.Delete(key);  
}  
```

## Cookie Options
1. Domain - The domain you want to associate with cookie
2. Path - Cookie Path
3. Expires - The expiration date and time of the cookie
4. HttpOnly - Gets or sets a value that indicates whether a cookie is accessible by client-side script or not.
5. Secure - Transmit the cookie using Secure Sockets Layer (SSL) that is, over HTTPS only.  
