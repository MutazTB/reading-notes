# Interfaces

An interface is defined as a syntactical contract that all the classes inheriting the interface should follow. The interface defines the 'what' part of the syntactical contract and the deriving classes define the 'how' part of the syntactical contract.

Interfaces define properties, methods, and events, which are the members of the interface. Interfaces contain only the declaration of the members.

Interfaces are declared using the interface keyword. It is similar to class declaration. Interface statements are public by default.

**Example**
public interface ITransactions {
   // interface members
   void showTransaction();
   double getAmount();
}

---

***To learn more*** [Interfaces](https://www.javatpoint.com/c-sharp-interface)