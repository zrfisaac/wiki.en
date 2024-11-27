# JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. It is widely used for transmitting data between a server and a client in web applications and for storing structured data.

## Índice

---

### Example

```json
{
  "metadata": {
    "file_name": "example.json",
    "version": 1.0,
    "created_at": "2024-11-27T15:45:00Z",
    "is_active": true,
    "tags": ["json", "example", "data", "testing"]
  },
  "user": {
    "id": 12345,
    "name": "John Doe",
    "email": "johndoe@example.com",
    "profile_picture": {
      "type": "base64",
      "data": "iVBORw0KGgoAAAANSUhEUgAAAAUA"
    },
    "settings": {
      "theme": "dark",
      "notifications_enabled": true,
      "volume_level": 0.75
    }
  },
  "data_collection": [
    {
      "type": "temperature",
      "unit": "Celsius",
      "value": 23.4,
      "timestamp": "2024-11-27T10:00:00Z"
    },
    {
      "type": "humidity",
      "unit": "%",
      "value": 65,
      "timestamp": "2024-11-27T10:00:00Z"
    }
  ],
  "complex_data": {
    "matrix": [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9]
    ],
    "records": [
      {
        "id": "a1b2c3",
        "value": 45.67,
        "description": "Sample record 1"
      },
      {
        "id": "d4e5f6",
        "value": 78.9,
        "description": "Sample record 2"
      }
    ]
  },
  "free_text": "This is an example of a long text entry. It can include multiple lines,\nspecial characters like !@#$%^&*(), and even Unicode like emojis 😊🌟.",
  "additional_properties": {
    "nullable_field": null,
    "boolean_values": [true, false, true],
    "float_array": [1.1, 2.2, 3.3],
    "nested_object": {
      "key1": "value1",
      "key2": 2,
      "key3": {
        "subkey1": [1, 2, 3],
        "subkey2": "nested value"
      }
    }
  }
}
```
