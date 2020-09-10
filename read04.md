## Repository Pattern 

“A Repository mediates between the domain and data mapping layers, acting like an in-memory domain object collection. Client objects construct query specifications declaratively and submit them to Repository for satisfaction. Objects can be added to and removed from the Repository, as they can from a simple collection of objects, and the mapping code encapsulated by the Repository will carry out the appropriate operations behind the scenes.”

Repository pattern separates the data access logic and maps it to the business entities in the business logic. Communication between the data access logic and the business logic  is done through interfaces.


### The separation of data access from business logic have many benefits. Some of them are:

- Centralization of the data access logic makes code easier to maintain
- Business and data access logic can be tested separately
- Reduces duplication of code
- A lower chance for making programming errors


### Repository design pattern is  fully stick onto interfaces. An interface acts like a contract which specify what an concrete class must implement. Let’s explore it a little bit. Suppose we have two data objects Uploader and Video, what are common set of operations that can be applied to these two data objects? In most situations we want to have the following operations:

1. Get all records
2. Get paginated set of records
3. Create a new record
4. Get record by it’s primary key
5. Get record by some other attribute
6. Update a record
7. Delete a record


## Testing Node.js + Mongoose with an in-memory database

In-memory database pros & cons
I wasn't convinced about using an in-memory database instead of mocks at first so I did a bit of digging and come up with this list of pros an cons:

Pros:

- No need for mocks: Your code is directly executed using the in-memory database, exactly the same as using your regular database.
- Faster development: Given that I don't need to build a mock for every operation and outcome but only test the query, I found the development process to be faster and more straightforward.
- More reliable tests: You're testing the actual code that will be executed on production, instead of some mock that might be incorrect, incomplete or outdated.
- Tests are easier to build: I'm not an expert in unit testing and the fact that I only need to seed the database and execute the code that I need to test made the whole process a lot easier to me.

Cons:

- The in-memory database probably needs seeding
- More memory usage (dah)
- Tests take longer to run (depending on your hardware).
