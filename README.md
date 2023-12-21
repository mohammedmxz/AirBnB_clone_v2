**AirBnB Clone (HBNB) - Project Overview**

*Description:*
This repository serves as the foundation for a student project aiming to create a replica of the AirBnB website. The current phase involves implementing a backend interface, or console, for efficient management of program data. The console commands allow users to create, update, and delete objects, as well as manage file storage. Leveraging JSON serialization/deserialization, the storage ensures persistence between different sessions.

*The Command Interpreter:*
The command interpreter provides a simple REPL (Read-Evaluate-Print-Loop) for interacting with the project's models. It also facilitates testing the functionality of supported storage engines. Examples of usage can be found in the documentation.

*How To Use:*
1. Clone this repository.
2. Locate the "console.py" file.
3. Run the console using the command: `./console.py`
4. The console prompt `(hbnb)` indicates successful access.

*Supported Commands:*
The command interpreter supports various commands for managing objects. Some key commands include:
- `help [command]`: Provides information about a command.
- `quit`: Closes the command interpreter.
- `create Model [prop_key=prop_value]...`: Creates a new instance of the Model class.
- `show Model id`: Prints the string representation of an instance.
- `destroy Model id`: Deletes an instance.
- `all [Model]`: Prints a list of string representations of instances.
- `update Model id attr_name attr_value`: Updates an instance with a new attribute value.
- `update Model id dict_repr`: Updates an instance with key-value pairs from a dictionary.

*Supported Models:*
The project includes several models representing different aspects:
- `BaseModel`: The base class for all models.
- `User`: Represents a user account.
- `State`: Represents the geographical state.
- `City`: Represents an urban area.
- `Amenity`: Represents a useful feature of a place.
- `Place`: Represents a building with rentable rooms.
- `Review`: Represents a review of a place.

*Environment Variables:*
- `HBNB_ENV`: The running environment (dev or test).
- `HBNB_MYSQL_USER`: MySQL server username.
- `HBNB_MYSQL_PWD`: MySQL server password.
- `HBNB_MYSQL_HOST`: MySQL server hostname.
- `HBNB_MYSQL_DB`: MySQL server database name.
- `HBNB_TYPE_STORAGE`: Type of storage used (file or db).

*Examples:*
Primary Command Syntax:
1. **Create an object:**
   ```bash
   (hbnb) create BaseModel
   ```

2. **Show an object:**
   ```bash
   (hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
   ```

3. **Destroy an object:**
   ```bash
   (hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
   ```

4. **Update an object:**
   ```bash
   (hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
   ```

Alternative Syntax:
1. **Show all User objects:**
   ```bash
   (hbnb) User.all()
   ```

2. **Destroy a User:**
   ```bash
   (hbnb) User.destroy("99f45908-1d17-46d1-9dd2-b7571128115b")
   ```

3. **Update User (by attribute):**
   ```bash
   (hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", name "Todd the Toad")
   ```

4. **Update User (by dictionary):**
   ```bash
   (hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", {'name': 'Fred the Frog', 'age': 9})
   ```

**Note:** Before committing, run `./test.bash` to ensure code compliance with the styling standard and test success. 

*Date: December 21, 2023*
