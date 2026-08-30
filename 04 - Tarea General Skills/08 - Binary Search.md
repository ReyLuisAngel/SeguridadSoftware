## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/19/challenge.zip)
## Solución
```
ReyLuis-academy@webshell:~/home/ctf-player/drop-in$ ./guessing_game.sh 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 380
Higher! Try again.
Enter your guess: 440
Higher! Try again.
Enter your guess: 470
Lower! Try again.
Enter your guess: 455
Lower! Try again.
Enter your guess: 448
Higher! Try again.
Enter your guess: 452
Higher! Try again.
Enter your guess: 454
Lower! Try again.
Enter your guess: 453
Congratulations! You guessed the correct number: 453
cat: /challenge/metadata.json: No such file or directory
Here's your flag: 
```
Lo realice bien a la primera pero no me fije que tenia que lanzar una instancia cuando tenia que darme la bandera no genero nada y tuve que buscar hasta que me di cuenta que paso, asi que lo tuve que jugar de nuevo
## Notas adicionales

## Referencias
