# XML

XML (Extensible Markup Language) is a markup language designed to store and transport data in a format that is both human-readable and machine-readable. It is highly flexible and allows users to define their own tags, making it suitable for a wide variety of applications, including document storage, configuration files, and data exchange between systems.

## Índice

---

### Example

```xml
<?xml version="1.0" encoding="UTF-8"?>
<document>
  <metadata>
    <file_name>example.xml</file_name>
    <version>1.0</version>
    <created_at>2024-11-27T15:45:00Z</created_at>
    <is_active>true</is_active>
    <tags>
      <tag>xml</tag>
      <tag>example</tag>
      <tag>data</tag>
      <tag>testing</tag>
    </tags>
  </metadata>

  <user>
    <id>12345</id>
    <name>John Doe</name>
    <email>johndoe@example.com</email>
    <profile_picture>
      <type>base64</type>
      <data>iVBORw0KGgoAAAANSUhEUgAAAAUA</data>
    </profile_picture>
    <settings>
      <theme>dark</theme>
      <notifications_enabled>true</notifications_enabled>
      <volume_level>0.75</volume_level>
    </settings>
  </user>

  <data_collection>
    <entry>
      <type>temperature</type>
      <unit>Celsius</unit>
      <value>23.4</value>
      <timestamp>2024-11-27T10:00:00Z</timestamp>
    </entry>
    <entry>
      <type>humidity</type>
      <unit>%</unit>
      <value>65</value>
      <timestamp>2024-11-27T10:00:00Z</timestamp>
    </entry>
  </data_collection>

  <complex_data>
    <matrix>
      <row>1 2 3</row>
      <row>4 5 6</row>
      <row>7 8 9</row>
    </matrix>
    <records>
      <record>
        <id>a1b2c3</id>
        <value>45.67</value>
        <description>Sample record 1</description>
      </record>
      <record>
        <id>d4e5f6</id>
        <value>78.9</value>
        <description>Sample record 2</description>
      </record>
    </records>
  </complex_data>

  <free_text>
    <![CDATA[
    This is an example of a long text entry. It can include multiple lines,
    special characters like !@#$%^&*(), and even Unicode like emojis 😊🌟.
    ]]>
  </free_text>

  <additional_properties>
    <nullable_field xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    <boolean_values>
      <value>true</value>
      <value>false</value>
      <value>true</value>
    </boolean_values>
    <float_array>
      <value>1.1</value>
      <value>2.2</value>
      <value>3.3</value>
    </float_array>
    <nested_object>
      <key1>value1</key1>
      <key2>2</key2>
      <key3>
        <subkey1>1 2 3</subkey1>
        <subkey2>nested value</subkey2>
      </key3>
    </nested_object>
  </additional_properties>
</document>
```
