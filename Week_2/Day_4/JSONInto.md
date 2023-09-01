## JSON Intro

### Summary

JSON stands for JavaScript Object Notation. It is a subset of the JavaScript Language. 

</br>

JSON is built of two structures:

* A collection of name/value pairs
* An order list of values

These are universal data structures. Most programming languages support them in some way.

</br>

Here is an example of what JSON looks like:
```json
{
  "name": "New York City",
  "boroughs": [
    "Manhattan",
    "Queens",
    "Brooklyn",
    "The Bronx",
    "Staten Island"],
  "population": 8491079,
  "area_codes": [212, 347, 646, 718, 917, 929],
  "position": { "lat": 40.7127, "lng": -74.0059 }
}
```
The keys are always double-quoted "strings", and the values can be numbers, strings, or objects.

</br>

We have the JSON object for serializing and deserializing. Serialization converts objects into a format that can be stored or transmitted between computers (typically as a string of text). Deserialization is going from string to object.

* JSON.parse()
  * Parse a string as JSON, optionally transform the produced value and its properties, and return the value

* JSON.stringify()
  * Return a JSON string corresponding to the specified value, optionally including only certain properties or replacing property values in a user-defined mannner.

</br>

JSON can be used for configuration files as well (Ex. package.json). 

</br>

JSON is language independent. It's not just used in Node / JS projects but also Python, Ruby, C#, Java, Golang, Rust, and more.