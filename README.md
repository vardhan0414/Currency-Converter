# Currency-Converter
In this project I designed currency converter using Python Modules

A currency is a system of money in common use, especially for people in a nation, eg, INR, USD and Bitcoin (₿) is a cryptocurrency. In this Blog article, we will learn how to Create Currency Converter. We will see the implementation in Python.

What is BitCoin?:
Bitcoin is a cryptocurrency,an innovative payment network, invented in 2008 by an unknown person or group of people using the name Satoshi Nakamoto and started in 2009.
If you wish to know more about it, you can refer to BitCoin Wikipedia Page.

What is Currency?:
Currency is a medium of exchange for goods and services. In short, it's money, in the form of paper or coins, usually issued by a government and generally accepted at its face value as a method of payment.
If you wish to know more about it, you can refer to Currency Wikipedia Page.

Module Used:
forex-python Module:
Forex Python is a Free Foreign exchange rates and currency conversion.

Features:
List all currency rates.
BitCoin price for all curuncies.
Converting amount to BitCoins.
Get historical rates for any day since 1999.
Conversion rate for one currency(ex; USD to INR).
Convert amount from one currency to other.(‘USD 10$’ to INR).
Currency symbols, Currency names, etc.


In order to access the Python library, you need to install it into your Python environment
#importing libraries for python currency converter project
from forex_python.converter import CurrencyRates
import tkinter as tk
from tkinter import *
import tkinter.messagebox
# Tkinter library – This is for creating an easy and fast GUI in python.
# tkinter.messagebox – This is used to display a message box in python. It displays messages according to the system’s requirements.
# forex_python.converter – Module for foreign exchange rates and currency conversions.

# These libraries are important for creating our project.
# Creating a GUI Window and Grid:
window = Tk()# creating empty window
window.title("ProjectGurukul Currency Conversion")# adding title to the window
window.geometry("700x400")
head = tk.Label( font=('Helvetica', 19, 'bold'), text='Currency Converter',
bg='grey', fg='black')
head.grid(row=1, column=0, sticky=W)
window = Tk()# creating empty window
window.title("ProjectGurukul Currency Conversion")# adding title to the window
window.geometry("700x400")
head = tk.Label( font=('Helvetica', 19, 'bold'), text='Currency Converter',
bg='grey', fg='black')
# head.grid(row=1, column=0, sticky=W)
# window= Tk() – for creating an empty GUI window.
# Here we have given a title to the window using window.title().
# We have created a grid to place the labels. Grid is an imaginary graph-like structure that divides a window into rows and columns and places them as we specify the row and column numbers.

# Creating and Initializing Variables:
#declaring variables
from_var = tk.StringVar(window)
to_var = tk.StringVar(window)
#initializing variables
from_var.set("currency")
to_var.set("currency")
# Creating global two variables- from_var (from variable) and to_var(to variable).
# And variables are initialized at “currency”.

# Defining a function for RealTime Currency Conversions:
#function for realtime conversion
def RealTimeCurrencyConversion():
  from forex_python.converter import CurrencyRates
  c = CurrencyRates()

  from_currency = "currency"
  to_currency = "currency"

  if (Amount1.get() == ""):
    tkinter.messagebox.showinfo("Error !!")

  elif (from_currency == "currency" or to_currency == "currency"):
    tkinter.messagebox.showinfo("Error !!")

  else:
     new_amt = c.convert(from_currency, to_currency, float(Amount1.get()))
     new_amount = float("{:.4f}".format(new_amt))
     Amount2.insert(0, str(new_amount))
      
# get() – This method returns the input as a string. If the field is empty then an error message displays.
# If both the currencies are not selected then also display an error message.
# Then we convert the string to float.
# The converted amount is displayed as Amount2.

# List Of Currency:
CurrenyCode_list = ["INR", "USD", "CAD", "CNY", "DKK", "EUR"]
# Here we specify a list of currencies we will be using in our project.
# Creating Labels for GUI:

#creating labels
Label_1 = Label(window, font='Helvetica', text="", padx=2, pady=2, bg="grey", fg="black")
Label_1.grid(row=1, column=0, sticky=W)

amount = tk.Label(window, font='Helvetica', text=" Amount : ", bg="grey", fg="black")
amount.grid(row=2, column=0, sticky=W)

from_curr = tk.Label(window, font='Helvetica', text=" From Currency : ", bg="grey", fg="black")
from_curr.grid(row=3, column=0, sticky=W)

to_cur = tk.Label(window, font='Helvetica', text=" To Currency : ", bg="grey", fg="black")
to_cur.grid(row=4, column=0, sticky=W)

convert_amt = tk.Label(window, font='Helvetica', text=" Converted Amount : ", bg="grey", fg="black")
convert_amt.grid(row=8, column=0, sticky=W)

Label_1 = Label(window, font='Helvetica', text="", padx=2, pady=2, bg="grey", fg="black")
Label_1.grid(row=5, column=0, sticky=W)

Label_2 = Label(window, font='Helvetica', text="", padx=2, pady=2, bg="grey", fg="black")
Label_2.grid(row=7, column=0, sticky=W)


# Creating labels and then placing them on the grid.
# font() – for specifying the font of the text in the label.
# text() – specifies the text that will be displayed in that particular label.
# Bg- background color.
# Fg- foreground color.
# Padx,pady – padding of x and y.
# Here we have created a total of 4 labels- “From Currency” , “To Currency”, “Amount” and “Converted Amount”.


# 7. Fetching Data:
FromCurrency = tk.OptionMenu(window, from_var, *CurrenyCode_list)
ToCurrency = tk.OptionMenu(window, to_var, *CurrenyCode_list)

FromCurrency.grid(row=3, column=1, ipadx=45, sticky=E)
ToCurrency.grid(row=4, column=1, ipadx=45, sticky=E)

Amount1 = tk.Entry(window)
Amount1.grid(row=2, column=1, ipadx=28, sticky=E)

Amount2 = tk.Entry(window)
Amount2.grid(row=8, column=1, ipadx=31, sticky=E)

button= Button(window, font='arial', text=" Convert ", padx=2, pady=2, bg="blue", fg="white",
command=RealTimeCurrencyConversion)
button.grid(row=6, column=0)

Label_1 = Label(window, font='Helvetica', text="", padx=2, pady=2, bg="grey", fg="black")
Label_1.grid(row=9, column=0, sticky=W)

window.configure(background='grey')
window.mainloop()

# Entry() – provides a text field to enter the amount.
# command=RealTimeCurrencyConversion – gives a command to perform the RealTimeCurrencyConversion() function.
# Button() – to make conversion we have created a convert button.
# Configure()- to configure the window and set background colour as grey.
# Mainloop() – This is the command to run the application.






With these steps, we have successfully Created Currency Converter using python. That's it!
Thank You

