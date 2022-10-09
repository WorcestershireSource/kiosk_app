
# Kiosk Application


## Overview:
This is a web application to act as a kisok for a coffee shop. 
It relies on an API with the payment provider 'Square'.
The application is based on a HMTL/CSS and Java front end. It uses JQuery and Ajax for a responsive experience
It uses a python/flask backend, which controls the communication with the payment provider, Square.

## Purpose
This app should allow a small shop to set up a self-service kiosk which will reduce the amount of staffing resource needed to run the shop.
Existing kiosk solutions are expensive and not commonly available in smaller shops. 

## Process
The backend requests the shop's inventory from Square - this is passed to the front end and used to populate the menu that appears to the user
The customer selects their purchases - this is all handled in the front end to ensure a responsive interface
When the customer is ready to pay, the order is posted the server with Ajax and the app makes a call on a Square API to initiate a payment with a Square 'terminal'
The user can pay using the square terminal - details of their payment are processed by Square and not passed through the kiosk app for security
An walkthrough of the process is available here: https://youtu.be/r4SIV6AEF-Y

## Useful commands:
python -m flask --debug run             Start a Flask session
export SQUARE_ACCESS_TOKEN=     Include the correct token for Square to work - get it from the developer dashboard below
source .venv/bin/activate       Start the virtual environment

## Useful links:
Sign into Square Developer dashboard: https://developer.squareup.com/
Bootstrap documentation: https://getbootstrap.com/docs/5.2/getting-started/introduction/
Test values for terminal payment: https://developer.squareup.com/docs/devtools/sandbox/testing 
Square advice on taking payments with the terminal: https://developer.squareup.com/docs/terminal-api/square-terminal-payments

## Square terminal instructions:
Pair terminal and POS application with Devices API: https://developer.squareup.com/docs/terminal-api/pos-integration
Send checkout request with Terminal API - request to API can specify terminal behaviours 
https://developer.squareup.com/docs/terminal-api/square-terminal-payments

