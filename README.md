
## How to Install lara-graphql

first of all

``git clone https://github.com/hudabikhoir/lara-websocket.git``

update your composer dependencies

``composer update``

migrate database 

``php artisan migrate``

start websocket server

``php artisan websocket:init``

Now open your console in both browser and write this

``var conn = new WebSocket('ws://127.0.0.1:{{your_port}}');``

same like this write the following lines and enter in both browser:

``conn.onopen = function(e) { console.log("Connection established!"); };``


``conn.onmessage = function(e) { console.log(e.data); };``


``conn.send(JSON.stringify({command: "subscribe", channel: "mychannel"}));``

Now in only one browser's console write this code

``conn.send(JSON.stringify({command: "message", message: "this is message"}));``
