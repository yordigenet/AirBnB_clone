# AirBnB clone - The console

![bnb_screenshot](https://github.com/yordigenet/AirBnB_clone/blob/396c43efe2c1bcb89b76051282d3271f290bd987/img_readme/Airbnb_screenshot.PNG/)
## Description

This team project is part of the ALX Software Engineer program.
It's the first step towards building a first full web application: an AirBnB clone.
This first step consists of a custom command-line interface for data management, and the base classes for the storage of this data.

## Usage

The console works both in interactive mode and non-interactive mode, much like a Unix shell.
It prints a prompt **(hbnb)** and waits for the user for input.

## Models

The folder [models](./models/) contains all the classes used in this project.

File | Description | Attributes
---- | ----------- | ----------
[base_model.py](./models/base_model.py) | BaseModel class for all the other classes | id, created_at, updated_at
[user.py](./models/user.py) | User class for future user information | email, password, first_name, last_name
[amenity.py](./models/amenity.py) | Amenity class for future amenity information | name
[city.py](./models/city.py) | City class for future location information | state_id, name
[state.py](./models/state.py) | State class for future location information | name
[place.py](./models/place.py) | Place class for future accomodation information | city_id, user_id, name, description, number_rooms, number_bathrooms, max_guest, price_by_night, latitude, longitude, amenity_ids
[review.py](./models/review.py) | Review class for future user/host review information | place_id, user_id, text

## File storage

The folder [engine](./models/engine/) manages the serialization and deserialization of all the data, following a JSON format.

A FileStorage class is defined in [file_storage.py](./models/engine/file_storage.py) with methods to follow this flow:
```<object> -> to_dict() -> <dictionary> -> JSON dump -> <json string> -> FILE -> <json string> -> JSON load -> <dictionary> -> <object>```

The [__init__.py](./models/__init__.py) file contains the instantiation of the FileStorage class called **storage**, followed by a call to the method reload() on that instance.
This allows the storage to be reloaded automatically at initialization, which recovers the serialized data.

## Tests

All the code is tested with the **unittest** module.
The test for the classes are in the [test_models](./tests/test_models/) folder.

## Authors

- [Ezeji Davidson](https://github.com/Dav0202) ~ (davidbrain162@gmail.com)
- [Yordanos Girma](https://github.com/yordigenet) ~ (yordigenet@gmail.com)
