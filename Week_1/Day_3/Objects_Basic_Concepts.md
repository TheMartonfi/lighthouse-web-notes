## Objects at a Glance
* Contain key-value pairs; each key maps to a value
* Contain keys which are always strings (or symbols, but it's less common and not important right now)
* Have unique keys; the same key cannot appear twice in an object
* Have their keys point to values which can be of any type

## Objects as Values

We can nest objects within objects.

```javascript
const person = {
  name: "Paul",
  address: {
    street: "310 W 95th",
    city: "New York",
    zipCode: 10027
  }
};
```
## Object Keys and Object.keys(...)

* Keys are always `strings`
* Each key is `unique` (can only occur once in the object)
* Each key is `associated` with exactly `one value`. (Note that technically, an array or another object would count as "one value" here, even though they contain other values.)

```javascript
//Square bracket notation with a string inside lets you access the keys
const mary = { name: "Mary Sue" };
mary["name"] = "Mary Jane";
mary["age"]  = 22;

//Dot notation is another way of accessing values
const mary = { name: "Mary Sue" };
mary.name = "Mary Jane";
mary.age  = 22;

//Stores an array of all key names of object you passed
const maryKey = Object.keys(mary);

```

## Objects Iteration

We can traverse all the `properties` of this object using a `for-loop`, like so

```javascript
var planetMoons = {
  mercury: 0,
  venus: 0,
  earth: 1,
  mars: 2,
  jupiter: 67,
  saturn: 62,
  uranus: 27,
  neptune: 14
};

for (var planet in planetMoons) {
  var numberOfMoons = planetMoons[planet];
  console.log("Planet: " + planet + ", # of Moons: "+ numberOfMoons);
}
```
We should be careful with this looping technique, as it can produce some [unexpected results](https://stackoverflow.com/questions/684672/how-do-i-loop-through-or-enumerate-a-javascript-object). For reasons which we'll cover in later activities, objects can sometimes have properties that they inherit from their prototype chain as well as method names. 



