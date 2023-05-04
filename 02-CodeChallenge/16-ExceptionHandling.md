# Exercise 1: Football Team Roster Management: Handling Player ID Uniqueness

## Problem Statement

You are given an incomplete Java code that represents a football team and its players. Your task is to complete the code so that it accomplishes the following objectives:

1.  Implement a constructor for the `Player` class with three parameters: `id`, `name`, and `position`.
2.  Complete the `addPlayer` method in the `Team` class to add a new player to the team. If a player with the same `id` already exists in the team, throw an `IllegalArgumentException` with the message "Duplicate player ID: " followed by the player's `id`.

### Instructions

1.  Add an all-argument constructor for the `Player` class that takes `id`, `name`, and `position` as input and initializes the corresponding instance variables.
2.  Complete the `addPlayer` method in the `Team` class: a. Check if a player with the same `id` already exists in the `players` list. If it does, throw an `IllegalArgumentException` with the message "Duplicate player ID: " followed by the player's `id`. b. If there's no duplicate player `id`, add the player to the `players` list.

### Example

When you run the provided `main` method, your program should output:

```
Duplicate player ID: 2
```

### Input/Output Example

#### Input

The input will be taken from the provided `main` method, which includes the following player information:

```
team.addPlayer(new Player(1, "John Smith", "Quarterback"));
team.addPlayer(new Player(2, "Mary Johnson", "Running back"));
team.addPlayer(new Player(3, "Bob Williams", "Offensive lineman"));
team.addPlayer(new Player(2, "Steve Martin", "Wide receiver"));
```

#### Output

When you run the provided `main` method, your program should output:

```
Duplicate player ID: 2
```

In this example, the program throws an exception when trying to add a player with a duplicate `id` (2).


## Hints

1.  To implement the `Player` constructor, use the provided class variables and the constructor's parameters to initialize the object.

```
public Player(int id, String name, String position) {
    this.id = id;
    this.name = name;
    this.position = position;
}
```

2.  To complete the `addPlayer` method in the `Team` class: a. Iterate through the `players` list using a for-each loop. b. Compare the `id` of each player with the `id` of the player to be added. If there's a match, throw an `IllegalArgumentException` with the specified message. c. If no duplicates are found, add the player to the `players` list.



## Solution Explanation

In the given problem, we have two classes: `Player` and `Team`. The `Player` class represents an individual football player, and the `Team` class represents a football team composed of multiple players. The goal is to complete the code by implementing a constructor for the `Player` class and the `addPlayer` method in the `Team` class.

1.  Implement the constructor for the `Player` class:

The constructor should take three parameters: `id`, `name`, and `position`. These parameters should be used to initialize the corresponding instance variables of the `Player` class.

```
public Player(int id, String name, String position) {
    this.id = id;
    this.name = name;
    this.position = position;
}
```
2.  Complete the `addPlayer` method in the `Team` class:

The `addPlayer` method should take a `Player` object as a parameter and add it to the `players` list, which represents the team. Before adding the player to the list, the method should check if a player with the same `id` already exists in the team. If there is a duplicate `id`, an `IllegalArgumentException` should be thrown with the message "Duplicate player ID: " followed by the player's `id`.

```
public void addPlayer(Player player) throws IllegalArgumentException {
    int playerId = player.getId();
    for (Player p : players) {
        if (p.getId() == playerId) {
            throw new IllegalArgumentException("Duplicate player ID: " + playerId);
        }
    }
    players.add(player);
}
```
With these changes, the complete solution code should look like the following:

```
import java.util.ArrayList;
import java.util.List;

public class FootballStats {

    public static class Player {
        public int id;
        public String name;
        public String position;

        // Constructor that takes id, name, and position as input parameters and initializes the corresponding instance variables.
        public Player(int id, String name, String position) {
            this.id = id;
            this.name = name;
            this.position = position;
        }

        public int getId() {
            return id;
        }

        public String getName() {
            return name;
        }

        public String getPosition() {
            return position;
        }
    }

    public static class Team {
        public List<Player> players;

        // Constructor that initializes an empty list of players.
        public Team() {
            this.players = new ArrayList<>();
        }

        // Method to add a player to the team while checking for duplicate IDs.
        public void addPlayer(Player player) throws IllegalArgumentException {
            int playerId = player.getId();
            
            // Iterate through the list of players to check for duplicates.
            for (Player p : players) {
                if (p.getId() == playerId) {
                    throw new IllegalArgumentException("Duplicate player ID: " + playerId);
                }
            }
            
            // If no duplicates are found, add the player to the list.
            players.add(player);
        }
    }

    public static void main(String[] args) {
        Team team = new Team();

        // Add players to the team and handle any IllegalArgumentExceptions.
        try {
            team.addPlayer(new Player(1, "John Smith", "Quarterback"));
            team.addPlayer(new Player(2, "Mary Johnson", "Running back"));
            team.addPlayer(new Player(3, "Bob Williams", "Offensive lineman"));
            team.addPlayer(new Player(2, "Steve Martin", "Wide receiver"));
        } catch (IllegalArgumentException e) {
            System.out.println(e.getMessage());
        }
    }
}

```

When you run the provided `main` method, the program should output:

```
Duplicate player ID: 2
```



## Student File

```
import java.util.ArrayList;
import java.util.List;

public class FootballStats {

    public static class Player {
        public int id;
        public String name;
        public String position;

        // Create Player all arg constructor
        // TODO: Implement a constructor that takes id, name, and position as input parameters and initializes the corresponding instance variables.

        public int getId() {
            return id;
        }

        public String getName() {
            return name;
        }

        public String getPosition() {
            return position;
        }
    }

    public static class Team {
        public List<Player> players;

        public Team() {
            this.players = new ArrayList<>();
        }

        public void addPlayer(Player player) throws IllegalArgumentException {
            // Complete the code
            // TODO: Check if a player with the same id already exists in the players list.
            // If it does, throw an IllegalArgumentException with the message "Duplicate player ID: " followed by the player's id.
            // If there's no duplicate player id, add the player to the players list.
        }
    }

    public static void main(String[] args) {
        Team team = new Team();

        try {
            team.addPlayer(new Player(1, "John Smith", "Quarterback"));
            team.addPlayer(new Player(2, "Mary Johnson", "Running back"));
            team.addPlayer(new Player(3, "Bob Williams", "Offensive lineman"));
            team.addPlayer(new Player(2, "Steve Martin", "Wide receiver"));
        } catch (IllegalArgumentException e) {
            System.out.println(e.getMessage());
        }
    }

}

```


## Solution Code

```

   

import java.util.ArrayList;
import java.util.List;

public class FootballStats {

    public static class Player {
        public int id;
        public String name;
        public String position;

        public Player(int id, String name, String position) {
            this.id = id;
            this.name = name;
            this.position = position;
        }

        public int getId() {
            return id;
        }

        public String getName() {
            return name;
        }

        public String getPosition() {
            return position;
        }
    }

    public static class Team {
        public List<Player> players;

        public Team() {
            this.players = new ArrayList<>();
        }

        public void addPlayer(Player player) throws IllegalArgumentException {
            int playerId = player.getId();
            for (Player p : players) {
                if (p.getId() == playerId) {
                    throw new IllegalArgumentException("Duplicate player ID: " + playerId);
                }
            }
            players.add(player);
        }
    }

    public static void main(String[] args) {
        Team team = new Team();

        try {
            team.addPlayer(new Player(1, "John Smith", "Quarterback"));
            team.addPlayer(new Player(2, "Mary Johnson", "Running back"));
            team.addPlayer(new Player(3, "Bob Williams", "Offensive lineman"));
            team.addPlayer(new Player(2, "Steve Martin", "Wide receiver"));
        } catch (IllegalArgumentException e) {
            System.out.println(e.getMessage());
        }
    }

}




```

## Evaluation Code

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertTrue;
import static org.junit.jupiter.api.Assertions.assertFalse;
import java.util.logging.Logger;

public class Evaluate {
    private final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_add_player_to_team(){
        FootballStats.Team team = new FootballStats.Team();
        FootballStats.Player player = new FootballStats.Player(1, "John Smith", "Quarterback");
        team.addPlayer(player);
        assertTrue(team.players.contains(player), "Should add player to team");

        logger.info("Actual Output: " + team.players.contains(player));
        logger.info("Expected Output: " + true);
    }

    @Test
    public void test_add_duplicate_player_to_team(){
        FootballStats.Team team = new FootballStats.Team();
        FootballStats.Player player1 = new FootballStats.Player(2, "John Smith", "Quarterback");
        FootballStats.Player player2 = new FootballStats.Player(2, "Mary Johnson", "Running back");
        team.addPlayer(player1);
        try {
            team.addPlayer(player2);
        } catch (IllegalArgumentException e) {
            assertTrue(e.getMessage().contains("Duplicate player ID"), "Should throw exception for duplicate player ID");

            logger.info("Actual Output: " + e.getMessage());
            logger.info("Expected Output: " + "Duplicate player ID: " + player2.getId());
        }
    }
}


```