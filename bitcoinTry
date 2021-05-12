# bitcoinTry
__author__ = "taurus"
import math
from math import trunc
from math import ceil
import tkinter as tk
import requests
import json

# main
window = tk.Tk()
window.title("currency exchange")
window.geometry("400x600")
window.configure(bg =  "blue")

# GUI title
title1 = tk.Label(text = "EXCHANGE", bg = "blue", fg ="white", font = "none 10 bold")
title1.grid()


# main programdata

def calculate():
    data = "https://www.paribu.com/ticker"
    result = requests.get(data)
    jeson_verisi = result.json()
    mevcutSatoshi = float(entry1.get())
    tlbitcoin = (jeson_verisi["BTC_TL"]["last"])
    entry2.insert(0, tlbitcoin)    
    tlDegeri = ceil(((tlbitcoin /100000000) * mevcutSatoshi ) * 100000000)
    entry3.insert(0, tlDegeri)   
    

# Data entry in tags

label1 = tk.Label(text = "SATOSHI: ", bg = "blue", fg ="white", font = "none 10 bold" )
label1.grid(column = 0, row = 1)

label2 = tk.Label(text = "BITCOIN_TRY: ", bg = "blue", fg ="white", font = "none 10 bold")
label2.grid(column = 0, row = 2)

label3 = tk.Label(text = "TRY: ", bg = "blue", fg ="white", font = "none 10 bold")
label3.grid(column = 0, row = 3)



# Data input text fields:

entry1 = tk.Entry()
entry1.grid(column = 1, row = 1)

entry2 = tk.Entry()
entry2.grid(column = 1, row = 2)

entry3 = tk.Entry()
entry3.grid(column = 1, row = 3)



# Calculation button program run:

button1 = tk.Button(text = "CALCULATE", font = "none 8 bold",fg = "black", command = calculate)
button1.grid(column = 0, row = 6)

# exit from function:
def close_window():
    window.destroy()   
    exit()

# Exit button:
button2 = tk.Button(text = "EXIT",fg = "black", font = "none 8 bold", command = close_window)
button2.grid(column = 0, row = 8)

# clear from function:
def clear():
    entry1.delete(0,"end")
    entry2.delete(0,"end")
    entry3.delete(0,"end")
    

# clear button:
button3 = tk.Button(text = "CLEAR",fg = "black", font = "none 8 bold", command = clear)
button3.grid(column = 0, row = 7)

window.mainloop()
