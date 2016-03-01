---
title: Hashes
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is a Hash?

A Hash is a collection of key-value pairs. You retrieve or create a new entry in a Hash by referring to its key. Hashes 
are also called 'associative arrays', 'dictionary', 'HashMap' etc. in other languages


# What are some examples of information that would be Hashes as opposed to some other data type?

Anything that does not need to be kept in order, like you would if using an Array. A Hash can have an unlimited (not 
necessarily infinite?) set of data as long as each key has a corresponding element of information along with it. An 
Array can be endless but it has to maintain its order, which is a constraint. Also, you can add and remove at will with 
a Hash.


# How are Hashes and Arrays similar? How are they different?

Arrays are similar to Hashes in that the location number is the key to the information stored there; whereas in Hashes 
the key can be anything. Methods used with Hashes can be used with Arrays.


# How do you retrieve a particular value from a Hash?

By calling its key. For example, puts hash[:leia] will retrieve the corresponding value for that key, which in the 
example I found on Wikibooks was "Princess from Alderaan"


# How do you add information to a Hash?

By using the "=>". In the previous question, I could assign the info to that key like this:
hash = { :leia => "Princess from Alderaan"}
You can also do this
hash['leia'] = "Princess from Alderaan"


# How would you perform an operation on every element inside a Hash?

Using the .each method


# How would you change the value of a particular element in a Hash?

By identifying the particular element and then assigning it a new value.
For example
hash { :leia => "Doesn't die in the new Stars Wars"}


# How do you delete an element from a Hash?

One way is to use the .delete method
For example
hash.delete(:leia)
This would also include using the .delete_if method to search for a key/element


# What happens if you try to retrieve an element from a Hash that does not exist in the Hash?

It will print a blank line - at least that is what it did for me when I tested it out using Atom
and my Start Command with Ruby prompt.
However, the Ruby-Doc says that a 'nil' will be returned if there is nothing corresponding.


# How do you determine how many elements are in a Hash?

By using the .length method
hash.length will tell you how many elements are stored in the hash.

---

Follow-up:

Compare the class documentation for each for more specific details.

Hashes enumerate their values in the order that the corresponding keys were inserted, whereas Arrays are assigned 
linearly (at the front, at the back, or at a specific location along that line). Hashes can use any object type for the 
index while Arrays have to use integers. Hashes are far more useful because they can be used like a dictionary. Visually 
you can think of it as a bucket of Lego compounds (each comprising of two individual yet connected Lego pieces) and 
whose order is random. Arrays are ordered linearly.


How would you perform an operation on every element inside a Hash?
Give me an example of using the .each method

h.each {|key, value| puts "#{key} is #{value}" }
this will print out each key and its corresponding value

or the Ruby Monk example...
restaurant_menu = { "Ramen" => 3, "Dal Makhani" => 4, "Coffee" => 2 }
restaurant_menu.each do | item, price |
which will assign each key as the item, and each value as the price


How would I change it so that when I do puts hash[:leia] it instead prints Has no time for your wookiees?
hash[:leia] = "Has no time for your wookiees?"


What happens if you try to retrieve an element from a Hash that does not exist in the Hash?
  
So for the above 2 issues, I ran this code to test out the value change and the nil

hashy = {:leia => "Don't Die"}
puts hashy
hashy[:leia] = "Wookies"
puts hashy
puts hashy[:x]
puts nil


I saved it in Atom and ran it with Start Command Prompt with Ruby
and the puts hashy[:x] and puts nil each produced a blank line