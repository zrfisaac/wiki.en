# INI

INI (Initialization File) is a simple, plain-text file format used for configuration settings in software applications. It consists of sections, each containing key-value pairs, making it easy to organize and manage configuration data.

## Index

---

### Example

```ini
[metadata]
file_name = example.ini
version = 1.0
created_at = 2024-11-27T15:45:00Z
is_active = true
tags = yaml, example, data, testing

[user]
id = 12345
name = John Doe
email = johndoe@example.com
profile_picture_type = base64
profile_picture_data = iVBORw0KGgoAAAANSUhEUgAAAAUA
theme = dark
notifications_enabled = true
volume_level = 0.75

[data_collection]
entry1_type = temperature
entry1_unit = Celsius
entry1_value = 23.4
entry1_timestamp = 2024-11-27T10:00:00Z
entry2_type = humidity
entry2_unit = %
entry2_value = 65
entry2_timestamp = 2024-11-27T10:00:00Z

[complex_data]
matrix_row1 = 1, 2, 3
matrix_row2 = 4, 5, 6
matrix_row3 = 7, 8, 9
record1_id = a1b2c3
record1_value = 45.67
record1_description = Sample record 1
record2_id = d4e5f6
record2_value = 78.9
record2_description = Sample record 2

[free_text]
value = This is an example of a long text entry. It can include multiple lines, special characters like !@#$%^&*(), and even Unicode like emojis 😊🌟.

[additional_properties]
nullable_field = null
boolean_values = true, false, true
float_array = 1.1, 2.2, 3.3
nested_object_key1 = value1
nested_object_key2 = 2
nested_object_subkey1 = 1, 2, 3
nested_object_subkey2 = nested value
```
