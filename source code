from random import randint

def user_interface(options):
    '''
    function presenting options and asking for player feedback
    returns integer.
    '''
    for index,option in enumerate(options):
        print(f'{index} = {option}')

        user_input = int(input('Co wybierasz? '))
        return user_input


def computer_choice(content):
    '''
    function that generates a random number based on the available options.
    returns random int
    '''
    computer_chose = randint(0,len(content)-1)
    return computer_chose


def check_results(choices, player, computer):
    '''
    function that checks who won.
    returns string
    '''
    if player == computer:
        return 'Remis'
    elif (player == 0 and computer == len(choices)-1) or player>computer and not(player==len(choices)-1 and computer==0):
        return 'Wygrałeś!'
    return 'Przegrałeś!'


def play():
    print('''
    ---------------------------------
    Kamień, Papier i Nożyce!
    Wybierz swoją broń.
    0 = Kamień, 1 = Papier, 2 = Nożyce
    ''')

    #Tłumaczy opcje i każe graczowi i komputerowi wybrać jedną z nich.
    options_list = ('Kamień', 'Papier', 'Nożyce')
    player_result = user_interface(options_list)
    computer_result = computer_choice(options_list)

    #Pokazuje co komputer i gracz wybrał.
    print(f'Gracz wybrał: {options_list[player_result]}')
    print(f'Komputer wybrał: {options_list[computer_result]}')

    #Sprawdza oba wyniki i przedstawia zwycięzce.
    results = check_results(options_list,player_result,computer_result)
    print (f'\n{results}')

def main():

    #Zmusza gracza do zagrania jeszcze raz
    play_again = ''
    while play_again.lower() != 'n':
        play()
        print (f'Chcesz zagrać jeszcze raz? ')
        play_again = input('Wprowadź\'y\' jeżeli tak lub \'n\' jeżeli nie: ')

main()
