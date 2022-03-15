# Exception

Exception handling in C#, suppoted by the try catch and finaly block is a mechanism to detect and handle run-time errors in code.the errors can be because of user, logic or system errors. If a user (programmer) does not provide a mechanism to handle these anomalies, the .NET runtime environment provide a default mechanism, which terminates the program execution.

---

### try-cath-finally
The try encloses the statements that might throw an exception whereas catch handles an exception if one exists. The finally can be used for any cleanup work that needs to be done.

***example***
---
try
{
 Statement which can cause an exception.
}
---
catch(Type x)
{
 Statements for handling the exception
}
---
finally
{
Any cleanup code
}
---

---

To learn more [Exception handling](https://www.c-sharpcorner.com/article/exception-handling-in-C-Sharp/)
