# Build a Periodic Table Database

### Part 1: Fix the database

### Part 2: Create a git repository

### Part 3: Create the script

### Subtasks

- Rename the `weight` column to `atomic_mass`
- Rename the `melting_point` column to `melting_point_celsius` and the `boiling_point` column to `boiling_point_celsius`
- The `melting_point_celsius` and `boiling_point_celsius` columns should not accept null values
- Add the `UNIQUE` constraint to the `symbol` and `name` columns from the `elements` table
- The `symbol` and `name` columns should have the `NOT NULL` constraint
- Set the `atomic_number` column from the `properties` table as a foreign key that references the column of the same name in the `elements` table
- Create a `types` table that will store the three types of elements
- The `types` table should have a `type_id` column that is an integer and the primary key
- The `types` table should have a `type` column that's a `VARCHAR` and cannot be `null`. It will store the different types from the `type` column in the `properties` table
- Add three rows to your `types` table whose values are the three different types from the `properties` table
- The `properties` table should have a `type_id` foreign key column that references the `type_id` column from the `types` table. It should be an `INT` with the `NOT NULL` constraint
- Each row in the `properties` table should have a `type_id` value that links to the correct type from the `types` table
- Capitalize the first letter of all the `symbol` values in the `elements` table. Be careful to only capitalize the letter and not change any others
- Remove all the trailing zeros after the decimals from each row of the `atomic_mass` column. You may need to adjust a data type to `DECIMAL` for this. The final values they should be are in the `atomic_mass.txt` file
- Add the element with atomic number `9` to the database. Its name is `Fluorine`, symbol is `F`, mass is `18.998`, melting point is `-220`, boiling point is `-188.1`, and it's a `nonmetal`
- Add the element with atomic number `10` to the database. Its name is `Neon`, symbol is `Ne`, mass is `20.18`, melting point is `-248.6`, boiling point is `-246.1`, and it's a `nonmetal`
- Create a `periodic_table` folder in the `project` folder and turn it into a git repository with `git init`
- The repository should have a `main` branch with all your commits
- The `periodic_table` repo should have at least five commits
- Create an `element.sh` file in your repo folder for the program
- The script (`.sh`) file should have executable permissions
- If you run `./element.sh`, it should output only `Please provide an element as an argument.` and finish running.
- If you run `./element.sh 1`, `./element.sh H`, or `./element.sh Hydrogen`, it should output only `The element with atomic number 1 is Hydrogen (H). It's a nonmetal, with a mass of 1.008 amu. Hydrogen has a melting point of -259.1 celsius and a boiling point of -252.9 celsius.`
- If you run `./element.sh` script with another element as input, you should get the same output but with information associated with the given element.
- If the argument input to your `element.sh` script doesn't exist as an `atomic_number`, `symbol`, or `name` in the database, the only output should be `I could not find that element in the database.`
- The message for the first commit in the repo should be `Initial commit`
- The rest of the commit messages should start with `fix:`, `feat:`, `refactor:`, `chore:`, or `test:`
- Delete the non existent element, whose `atomic_number` is `1000`, from the two tables
- The `properties` table should not have a `type` column
- Finish the project while on the `main` branch. The working tree should be clean and there should not be any uncommitted changes
