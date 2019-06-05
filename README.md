# Week 1, Day 2 Morning Discussion Questions

## Instructions

Take 30 minutes and answer the following questions together with your group. Take turns playing around with the code provided in Pry or IRB.

## Questions

1 . What does the below method return?

```ruby
def greet(name)
  puts "Hello, #{name}"
end
greet("Steven") #=> ?
```

2 . What does this method return?

```ruby
def hate_steven?(name)
  if name == "Steven"
    "OMG He's the worst"
  else
    "You cool"
  end
end
```

3 . How would you select all of the words that start with the letter "a" from the below array?

```ruby
["apple", "pear", "face", "champagne", "palm tree", "aardvark", "pineapple"]
```

4 . Write a method that takes in an argument of a sentence and returns the
number of words in the sentence

```ruby
word_count("Hi, isn't this a great and interesting sentence??")
 # => 8
```

5 . What will the following method return?

```ruby
def rude_greeting(name=nil)
 name ||= "you jerk"
 puts "Hey there, #{name}"
end
```

6 . What will the following `puts`?

```ruby
best_animal = "cat"
favorite_animal = best_animal
puts favorite_animal
# => ?
```

7 . What will the following `puts`?

```ruby
def my_favorite_animal
  "cat"
end

best_animal = my_favorite_animal

puts best_animal
```

8 . What error, if any, will the following code raise?

```ruby
"Blink" + 182
```

9 . How would you `puts` out any and all foods that are delicious?

```ruby
foods = {"pie" => "delicious", "broccoli" => "not delicious",
"carrots" => "not delicious", "apples" => "delicious",
"peanut butter" => "delicious"}
```

10 . Delete all elements of the `foods` hash that are *not* delicious.

11 . What is the return value of this method?
```ruby
  character_names = ["Daenerys Targaryen", "Jon Snow" ,"Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]

  def downcase_all(array_of_strings)
    array_of_strings.each do |one_string|
      one_string.downcase
    end
  end
```

12 . Write a method that `puts` out a random Archer quote.
```ruby
  archer = {
      "name" => "Sterling Mallory Archer",
      "co-workers"=> ["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"],
      "favorite_drink" => "Bloody Mary",
      "Quotes" => ["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]
  }
```

2.6.1 :029 > foods = {"pie" => "delicious", "broccoli" => "not delicious",
2.6.1 :030 >     "carrots" => "not delicious", "apples" => "delicious",
2.6.1 :031 >     "peanut butter" => "delicious"}
 => {"pie"=>"delicious", "broccoli"=>"not delicious", "carrots"=>"not delicious", "apples"=>"delicious", "peanut butter"=>"delicious"}
2.6.1 :032 > foods
 => {"pie"=>"delicious", "broccoli"=>"not delicious", "carrots"=>"not delicious", "apples"=>"delicious", "peanut butter"=>"delicious"}
2.6.1 :033 > foods.each do |k, v|
2.6.1 :034 >     if v == "delicious"
2.6.1 :035?>     puts k
2.6.1 :036?>     end
2.6.1 :037?>   end
pie
apples
peanut butter
 => {"pie"=>"delicious", "broccoli"=>"not delicious", "carrots"=>"not delicious", "apples"=>"delicious", "peanut butter"=>"delicious"}
2.6.1 :038 > foods.each do |k, v|
2.6.1 :039 >     foods.delete_if(v == not_deliciousç=^C
2.6.1 :039 > foods.delete_if { |k, v| v == "not delicious" }
 => {"pie"=>"delicious", "apples"=>"delicious", "peanut butter"=>"delicious"}
2.6.1 :040 > character_names = ["Daenerys Targaryen", "Jon Snow" ,"Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
 => ["Daenerys Targaryen", "Jon Snow", "Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
2.6.1 :041 > character_names
 => ["Daenerys Targaryen", "Jon Snow", "Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
2.6.1 :042 > character_names.each do |string|
2.6.1 :043 >     string.downcase
2.6.1 :044?>   end
 => ["Daenerys Targaryen", "Jon Snow", "Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
2.6.1 :045 > character_names.each do |string|
2.6.1 :046 >     ^C
2.6.1 :046 > new_arr = []
 => []
2.6.1 :047 > character_names.each do |string|
2.6.1 :048 >     new_arr << string.downcase
2.6.1 :049?>   end
 => ["Daenerys Targaryen", "Jon Snow", "Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
2.6.1 :050 > new_arr
 => ["daenerys targaryen", "jon snow", "arya stark", "tyrion lannister", "sansa stark", "cersei lannister", "margaery tyrell"]
2.6.1 :051 > new_arr.collect do |string|
2.6.1 :052 >     string.upcase
2.6.1 :053?>   end
 => ["DAENERYS TARGARYEN", "JON SNOW", "ARYA STARK", "TYRION LANNISTER", "SANSA STARK", "CERSEI LANNISTER", "MARGAERY TYRELL"]
2.6.1 :054 > string
 => "Hi, isn't this a great and interesting sentence??"
2.6.1 :055 > character_names
 => ["Daenerys Targaryen", "Jon Snow", "Arya Stark", "Tyrion Lannister", "Sansa Stark", "Cersei Lannister", "Margaery Tyrell"]
2.6.1 :056 > archer = {
2.6.1 :057 >           "name" => "Sterling Mallory Archer",
2.6.1 :058 >           "co-workers"=> ["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"],
2.6.1 :059 >           "favorite_drink" => "Bloody Mary",
2.6.1 :060 >           "Quotes" => ["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]
2.6.1 :061?>     }
 => {"name"=>"Sterling Mallory Archer", "co-workers"=>["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"], "favorite_drink"=>"Bloody Mary", "Quotes"=>["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]}
2.6.1 :062 > archer
 => {"name"=>"Sterling Mallory Archer", "co-workers"=>["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"], "favorite_drink"=>"Bloody Mary", "Quotes"=>["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]}
2.6.1 :063 > def random_archer_quote(hash)
2.6.1 :064?>   archer["Quotes"].each do |string|
2.6.1 :065 >       return string.random
2.6.1 :066?>     end
2.6.1 :067?>   end
 => :random_archer_quote
2.6.1 :068 > random_archer_quote(archer)
Traceback (most recent call last):
        5: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `<main>'
        4: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `load'
        3: from /Users/kara/.rvm/rubies/ruby-2.6.1/lib/ruby/gems/2.6.0/gems/irb-1.0.0/exe/irb:11:in `<top (required)>'
        2: from (irb):68
        1: from (irb):64:in `random_archer_quote'
NameError (undefined local variable or method `archer' for main:Object)
2.6.1 :069 > archer
 => {"name"=>"Sterling Mallory Archer", "co-workers"=>["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"], "favorite_drink"=>"Bloody Mary", "Quotes"=>["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]}
2.6.1 :070 > def random_archer_quote(hash)
2.6.1 :071?>   hash["Quotes"].each do |string|
2.6.1 :072 >       return string.sample
2.6.1 :073?>     end
2.6.1 :074?>   end
 => :random_archer_quote
2.6.1 :075 > random_archer_quote(archer)
Traceback (most recent call last):
        7: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `<main>'
        6: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `load'
        5: from /Users/kara/.rvm/rubies/ruby-2.6.1/lib/ruby/gems/2.6.0/gems/irb-1.0.0/exe/irb:11:in `<top (required)>'
        4: from (irb):75
        3: from (irb):71:in `random_archer_quote'
        2: from (irb):71:in `each'
        1: from (irb):72:in `block in random_archer_quote'
NoMethodError (undefined method `sample' for "I swear to god, I had something for this":String)
2.6.1 :076 > def random_archer_quote(hash)
2.6.1 :077?>   def random_archer_quote(hash)^C
2.6.1 :077 > def random_archer_quote(hash)
2.6.1 :078?>   ^Ccher["Quotes"].sample
2.6.1 :078 > def random_archer_quote
2.6.1 :079?>   archer["Quotes"].sample
2.6.1 :080?>   end
 => :random_archer_quote
2.6.1 :081 > random_archer_quote
Traceback (most recent call last):
        5: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `<main>'
        4: from /Users/kara/.rvm/rubies/ruby-2.6.1/bin/irb:23:in `load'
        3: from /Users/kara/.rvm/rubies/ruby-2.6.1/lib/ruby/gems/2.6.0/gems/irb-1.0.0/exe/irb:11:in `<top (required)>'
        2: from (irb):81
        1: from (irb):79:in `random_archer_quote'
NameError (undefined local variable or method `archer' for main:Object)
2.6.1 :082 > def random_archer_quote
2.6.1 :083?>   archer = {
2.6.1 :084 >             "name" => "Sterling Mallory Archer",
2.6.1 :085 >             "co-workers"=> ["Lana Kane", "Cyril Figgis", "Cheryl Tunt", "Pam Poovey", "Dr Krieger"],
2.6.1 :086 >             "favorite_drink" => "Bloody Mary",
2.6.1 :087 >             "Quotes" => ["I swear to god, I had something for this", "Phrasing", "Boop", "Danger Zone", "Read a book", "Do you not?", "Can't or won't?"]
2.6.1 :088?>       }
2.6.1 :089?>   archer["Quotes"].sample
2.6.1 :090?>   end
 => :random_archer_quote
2.6.1 :091 > random_archer_quote
 => "I swear to god, I had something for this"

<p class='util--hide'>View <a href='https://learn.co/lessons/immersive-week-1-discussion-questions'>Immersive Week 1 Discussion Questions</a> on Learn.co and start learning to code for free.</p>
