# simple_chess_js
simple chess game using canvas

simple classes, and objects

responsive chess web game canvas bootstrap

#### last step in game play will be like this with diff gif or use this if decide display message based on socket player who win and keep You Win
![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/d9f9dbec-cf56-45e3-a09c-c0bdb1d106bc)

![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/1754488c-e7ae-41ee-8f7c-321b4ada214b)


#WHat is that:
full OOP Javascript Client side for the new one of top multiple chess games on internet, it sumilate league of legends way but in famus known game chess which played alot by people and not require high graphics so vanila ES6 javascript OOP client side fit the game, also make it better and easy to be integrated with any backend language without diffrent configuration or switch client side, and as it OOP it best match fit all backend languages known used in web, only game vs socket online no computer why as it multiple player lol like chess game, no vs computer, you can train on any web chess game and come here play vs frogien or your friends.


# Comming Soon:
1- socket py-or-ts-node.js or both ez flask api (not included in this repo and will not)
2- database and account is must start play, uses OUATH2 for google,facebook,instagram if any, twitch auth
3- player sign in
4- player click start game button
5- it take it to game start page and config of game, select lvl of player range or random, 
select match type here like League of legends and byoned 
#### game types
* (1v1),
* (2v2),
* (3v3),
* (4v4),
* (5v5),
* (1vall with max number of enemy ex) 1 vs all but max players not more than 32 players or vice versa to find ur need like 32 players vs lowest 1 and sure both have option let system manage as avail now it noob web site yet so few players.
* (all options can have friends in game saved in db play togther and one leader of them send create room request to flask and others join fast auto the room created and leader select settings of game -v- settings
 
6- leader/player ready he and if multiple friends feature (nested socket are ready) will click on button start game queue and all db will save game config selected in db and users meta data for perperae node.js work with same mysql db **microservice app*** many, then flask will take the AJAX game start request and sent web GET request to node.js play_queue endpoint which setup the game room and save in database info
about how many players in room and their config and keep check with socket and while until in database other players meet the ranges of config or managa auto if no settings selected.

7- note as this ES6 client js OOP and almost not less than ts it not make error and have if statment cover all cases, and as i said flask is api brain managaer for website the client side is managed by node.js and rendered
after game end node.js save in db to think with flask and can send flask request to back to player to web app flask original which have all Ouath, homepage, payment if any and all fancy web app for game and settings etc
as seen node.js manage game js client side and socket , flask API is main website and brain and starter of the node.js no direct access for node.js without also ouath of flask best is connect both oauth2 flask and node.js
 advanced devops exp needed.or full game node.js, better client js and backend js togther

---------------------

## Software diagrams and core js works for advanced info and more detials how it works
1. King first Move:
    - ![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/06a558d5-95af-462c-bd80-1b01909b10a1)
    - ![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/1e882042-dbd6-4a04-a873-eee65bb7e663) // lol create newClientError only do all that and handle html 
    - ![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/39544c6c-10f5-471e-bea5-3f2072ebd028)




on database request in database will send request to flask API to send node.js api request to create new room for that player if no other queue room already exist in db with same player selection
