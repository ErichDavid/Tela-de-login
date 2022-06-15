import PysimpleGUI
from PysimpleGUI import PysimpleGUI as sg 

#layout
sg.theme('reddit')
layout = [
    [sg.Text('Usuario'),sg.input(key='Usuario')],
    [sg.Text('senha'),sg.input(key='Senha',password_char'*')],
    [sg.Checkbox('Salvar o login?')]
    [sg.Button('Entrar')]
]
#janela
janela = sg.Window('Tela de login', layout)
#ler os eventos
while True:
    eventos, valores = janela.read()
    if eventos == sg.WINDOW_CLOSED:
        break
    if eventos == 'Entrar':
        if valores['usuario'] == 'jhonatan' and valores['senha'] == '123456':
            print('Bem vindo')
