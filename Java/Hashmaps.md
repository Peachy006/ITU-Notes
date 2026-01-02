

Hashmaps contain 2 different types of values,

The keys and the values, the keys are written first and are assigned a value, the way you make a hashmap is

**HashMap<String, Integer> name = new Hashmap<>();**

Here you have the keys which are strings and the values which are integeres

The basic stuff you can do with hashmaps are stuff like:

```Java
name.get("name") 
```

name.get("name") 
this prints the value assigned to the key name


you can also do:

```Java
name.containsKey(name);
```
If the map then has a key called name it will return true, you can also do this with containsValue

you can replace a value assigned to a key by saying:

```Java
name.put("name", 12345);
```

This will assign the new value to the key john
You can also do:

```Java
name.replace("name", 12355) 
```
By using replace instead you ensure that if the key doesnt already excist it doesnt create it for you


But then, what if you want to create a key and a value only if the key doesnt already excist:

```Java
name.putIfAbsent("name", 12211) 
```

If you want to remove a value you can say:

```Java
name.remove("name") 
```
