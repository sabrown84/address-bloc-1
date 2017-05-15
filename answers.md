* A Ruby gem is a packaging system to facilitate the creation, sharing, and installation of libraries. I would use it to solve a problem without having to code every detail by hand.
* Lazy loading is when the method is called when it is needed. Eager loading is when the method is called when the program is initialized.
* CREATE TABLE is where you create a new table with attributes in it. INSERT INTO is where you insert attributes with values into a table.
* Extend only allows us to add class methods from a module, but in order to save changes the methods will need to be included as instance methods.
* The methods need to interact with a particular instance of a class. Rather than it working for the entire class with each change.
* The SQL query will find a record based on the ID and update the data in the table with the correct value.
* The variables need values and to be initialized.

``` ruby
def camelCase(snake_case)
  snake_case.gsub!(/_[a-z]/, &:upcase)
  snake_case.gsub!(/(_)([A-Z])/, '\2')
end
```
``` ruby
def find_by(attribute, value)
  row = connection.get_first_row <<-SQL
    SELECT #{col.join ","} FROM #{table}
    WHERE #{attribute} = #{BlocRecord::Utility.sql_strings(value)};
  SQL

  object_from_row(row)
end
```
