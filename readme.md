[See assignment in Alexa.](https://alexa.bitmaker.co/cohorts/72/assignments/2244/latest)



ANSWERS

1. Find all the robots from The Hitchhiker's Guide to the Galaxy.
----> SELECT name, source FROM robots WHERE source = 'The Hitchhiker''s Guide to the Galaxy';
O/P: Marvin, Deep Thought

2. Find the robot with an "anxious" personality.
----> SELECT  FROM robots WHERE personality='anxious';
O/P: C3P0

3. Find all recipes that are nut free.
----> SELECT name FROM recipes WHERE nut_free = 't';
O/P: Butternut Squash Bake, Vegetarian Bibimbap, French Veggie loaf, Quinoa and Black beans, Juicy Roasted Chicken, Garlic Green Beans, Stout Slow Cooker Corned Beef and Veggies

4. Count the number of recipes that are gluten free but not vegetarian.
----> SELECT COUNT(gluten_free) FROM recipes WHERE NOT vegetarian;
O/P: 2

5. Find the animal with the most legs.
----> SELECT name, number_of_legs FROM animals WHERE number_of_legs = (SELECT MAX(number_of_legs) from animals);
O/P: Octopus

6. Find the board game that takes the least amount of time to play.
----> SELECT name, mins_to_play FROM board_games WHERE mins_to_play = (SELECT MIN(mins_to_play) from board_games);
O/P: Sushi, Quixo

7. Find the recipe that takes the most time to prepare.
----> SELECT name, minutes_required FROM recipes WHERE minutes_required = (SELECT MAX(minutes_required) from recipes);
O/P: Stout Cooker Corned Beef and Veggies

8. Find all the robots whose name starts with the letter M.
----> SELECT name FROM robots where name LIKE 'M%';
O/P: Marvin, Mr.Butlertron

9. Count the number of board games that can be played by 8 people.
----> SELECT * FROM board_games WHERE max_player >= 8;
O/P: Arkham Horror, Cards Against Humanity, Game of Things

10. Find all animals that are swimming and egg-laying.
----> SELECT * FROM animals WHERE swimming = 't' AND egg_laying = 't';
O/P: Octopus, Duck

11. Find all animals that are swimming and egg-laying but not flying.
----> SELECT * FROM animals WHERE swimming = 't' AND egg_laying = 't' AND flying = 'f';
O/P: Octopus

12. Find the board game that supports the largest number of people.
----> SELECT name, max_players FROM board_games where max_players = (SELECT max(max_players) FROM board_games);
O/P: Cards Against Humanity
