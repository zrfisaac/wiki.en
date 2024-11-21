# Ruby

---

### **Table of Contents**  
1. [Introduction to Ruby](#introduction-to-ruby)  
2. [Installing Ruby](#installing-ruby)  
3. [Environment Setup](#environment-setup)  
4. [Code Examples](#code-examples)  
5. [Useful Ruby Commands](#useful-ruby-commands)  
6. [Additional Resources and Links](#additional-resources-and-links)  

---

### **Introduction to Ruby**  

Ruby is a high-level, interpreted, and dynamic programming language known for its simplicity and readability. Developed in the mid-1990s, Ruby is often used in web applications (thanks to the Ruby on Rails framework), automation scripts, API development, and more.  

---

### **Installing Ruby**  

#### Using a Version Manager (Recommended)  
`rbenv` or `RVM` are popular tools for managing Ruby versions.  

- **Install with `rbenv`:**  
  ```bash
  curl -fsSL https://github.com/rbenv/rbenv-installer/raw/main/bin/rbenv-installer | bash
  rbenv install 3.2.2
  rbenv global 3.2.2
  ruby -v
  ```

- **Install with `RVM`:**  
  ```bash
  curl -sSL https://get.rvm.io | bash -s stable
  rvm install 3.2.2
  rvm use 3.2.2 --default
  ruby -v
  ```  

#### Direct Installation  
For Debian/Ubuntu-based systems:  
```bash
sudo apt update
sudo apt install ruby-full
ruby -v
```  

---

### **Environment Setup**  

1. **Creating a Ruby Project:**  
   Create a directory for your project and initialize a Ruby file.  
   ```bash
   mkdir my_ruby_project
   cd my_ruby_project
   touch app.rb
   ```

2. **Installing Gems (Libraries):**  
   Use the `bundler` package manager to manage dependencies.  
   ```bash
   gem install bundler
   bundler init
   ```

3. **Ruby Project Structure:**  
   ```
   my_ruby_project/
   ├── app.rb
   ├── Gemfile
   ├── lib/
   └── spec/
   ```

---

### **Code Examples**  

#### Hello World  
```ruby
puts "Hello, Ruby!"
```

#### Functions and Classes  
```ruby
class Person
  attr_accessor :name, :age

  def initialize(name, age)
    @name = name
    @age = age
  end

  def greet
    "Hi, I'm #{@name} and I'm #{@age} years old."
  end
end

person = Person.new("Alice", 30)
puts person.greet
```

#### Array and Hash Manipulation  
```ruby
# Arrays
numbers = [1, 2, 3, 4, 5]
squared = numbers.map { |n| n**2 }
puts squared.inspect

# Hashes
person = { name: "Bob", age: 25 }
puts "Name: #{person[:name]}, Age: #{person[:age]}"
```

#### File Manipulation  
```ruby
File.open("example.txt", "w") { |file| file.write("Hello, File!") }

content = File.read("example.txt")
puts content
```

#### HTTP Requests with `Net::HTTP`  
```ruby
require 'net/http'
require 'json'

url = URI("https://jsonplaceholder.typicode.com/posts/1")
response = Net::HTTP.get(url)
data = JSON.parse(response)

puts "Title: #{data['title']}"
```

---

### **Useful Ruby Commands**  

1. **Run a Ruby File:**  
   ```bash
   ruby app.rb
   ```

2. **Interact with Ruby in the Console (`irb`):**  
   ```bash
   irb
   > puts "Hello, Console!"
   ```

3. **Manage Dependencies with Bundler:**  
   Install the dependencies listed in the `Gemfile`:  
   ```bash
   bundle install
   ```

4. **Create Tests with `RSpec`:**  
   Install `RSpec` and initialize:  
   ```bash
   gem install rspec
   rspec --init
   rspec
   ```
