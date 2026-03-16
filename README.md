# Test


''' 
import time
from pynput import mouse
from pynput.mouse import Controller
import pyautogui as k


m = Controller()
x, y = m.position #
keys = {
    mouse.Button.left: 'a',
    mouse.Button.right: 'd',
    mouse.Button.x1: 'w',
    mouse.Button.x2: 's'
}



def on_scroll(x, y, dx, dy):
    if dy > 0:
        print('Колесо прокручено вверх')
        k.press('up')

    elif dy < 0:
        print('Колесо прокручено вниз')
        k.press('down')


def on_click(x, y, button, pressed):
    global position
    if pressed:
        key = f'{keys.get(str(button))}'
        print(f"нажата кнопка {button} в позиции ({x}, {y})")

        k.press(key)
        print(key)


def press_key(key, n):
        k.keyDown(key)
        time.sleep(n / 2000)
        k.keyUp(key)


def on_move(dx, dy):
    global x

    print(x, y, '->')
    move = abs(x - dx)
    if x - dx > 0:
        print(f'мышь переместилась влево на {move}')
        press_key('left', move)
        x = dx
    if x - dx < 0:
        print(f'мышь переместилась вправо на {move}')
        press_key('right', move)
        x = dx



with mouse.Listener(on_move=on_move, on_click=on_click, on_scroll=on_scroll) as listener:
    listener.join()'''
