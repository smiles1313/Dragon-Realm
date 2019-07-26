# Dragon-Realm
A short text adventure.

#Dragon Realm
import random

def intro():
	print('You are in a land full of dragons. In front of you, you see two caves. \nIn one cave, the dragon is friendly and will share his treasure with you.\nThe other dragon is greedy and hungry, and will eat you on sight.')

def question():
	treasure = random.randint(1,2)
	choice = 'You approach the cave... \nIt is dark and spooky... \nA large dragon jumps out in front of you! He...\n'
	decision = input('Which cave will you go into? (1 or 2)')

	if decision == '1':

		decision = int(decision)
		if decision == treasure :
			print(choice)
			print('Gives you a generous amount of valuable jewels!')
		elif decision != treasure:
			print(choice)
			print('Gobbles you down in one bite!')


	elif decision == '2':

		decision = int(decision)
		if decision == treasure :
			print(choice)
			print('Gives you a generous amount of valuable jewels!')
		elif decision != treasure:
			print(choice)
			print('Gobbles you down in one bite!')

	else:
		print('There are no secret caves!')



def play():

	intro()
	print('')

	question()
	print('')

	repeat = (input('Do you want to play again? (yes or no)'))
	
	while repeat == 'yes':
		print('')
		intro()
		print('')

		question()
		print('')

		repeat = (input('Do you want to play again? (yes or no)'))


	else:
		print('The end.')


play()

