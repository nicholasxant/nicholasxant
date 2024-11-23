#task 1: X si O DADDY!
board=[" ","1","2","3","1","-","-","-","2","-","-","-","3","-","-","-"]

p1_turn = True
have_w = False
while not have_w:
    for i in range(0, 16, 4):
        print(board[i] + "|" + board[i+1] + "|" + board[i+2] + "|" + board[i+3] + "|")
    if p1_turn:
        print("X's turn")
    else:
        print("O's turn")
    new_place = False
    while not new_place:
        row = col = 10
        while row > 3 or row < 1:
            row = int(input("Witch row you wanna place? \n"))
        while col > 3 or col < 1:
            col= int(input("Witch colum you want to place? \n"))
        if board[4 * row + col] == "-":
            new_place=True
#Player Mark
    if p1_turn:
        board[4*row+col] = "x"
    else:
        board[4*row+col] = "o"

#Veificam randuri:
    if board[5] == board[6] and board[5]==board[7] and board[5] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
    have_w = True
    if board[9] == board[10] and board[9]==board[11] and board[9] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
    have_w = True
    if board[13] == board[14] and board[13]==board[15] and board[13] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
        have_w = True

#verificare coloane:
    if board[5] == board[9] and board[5]==board[13] and board[5] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
        have_w = True
    if board[6] == board[10] and board[6]==board[14] and board[6] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
    have_w = True
    if board[7] == board[11] and board[7]==board[15] and board[7] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
        have_w = True

#verificare diagonale
    if board[5] == board[10] and board[5]==board[15] and board[5] != "-": #NICE
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
        have_w = True
    if board[7] == board[10] and board[7]==board[13] and board[7] != "-":
        if p1_turn:
            print("X wins.")
        else:
            print("O wins.")
        have_w = True
    #Remiza
    if not have_w and "-" not in board:
        have_w = True
        print("REMIZA, egaliztate.")
    if not have_w:
        if p1_turn:
            have_w = False
        else:
            p1_turn = True
for i in range(0, 16, 4):
    print(board[i] + "|" + board[i + 1] + "|" + board[i + 2] + "|" + board[i + 3] + "|")











    # FACETI PROIECTE NOI! NU mai flositi pe ale mele! OPRITIVA din a face pyrhin stuff i nprouectel mele!!!!
    #Stop your stupidity!
