# Chess JS rules and (core moves)

###### this main for me while devloping and for other js dev to know how handle chess game movment easy with 2D array all needed from u use same, array and use rule that uses row index and i index

note game (uses auto detect all posible position valid before play and remove and draw only the character class for performance instead of redraw all, and for ux so user know all valid move, also help full later when make mode vs computer can detect posible valid movements

#### MAP (JS pandas part like 2DArray for move) (this make all pues movement lows using direct 2d array and just i and r to get target sqaure and assign it holder if accepted
```javascriptarr
this.charactersIndexes = [
                    [
                     { img: blackRook,       Class: Rook,     r: 0, c: 0, color: 'black' },
                     { img: blackHourse,     Class: Hourse,   r: 0, c: 1, color: 'black' },
                     { img: blackElephant,   Class: Alfil,    r: 0, c: 2, color: 'black' },
                     { img: blackQueen,      Class: Queen,    r: 0, c: 3, color: 'black' },
                     { img: blackKing,       Class: King,     r: 0, c: 4, color: 'black' },
                     { img: blackElephant,   Class: Alfil,    r: 0, c: 5, color: 'black' },
                     { img: blackHourse,     Class: Hourse,   r: 0, c: 6, color: 'black' },
                     { img: blackRook,       Class: Rook,     r: 0, c: 7, color: 'black' }
                    ],

                    [
                      { img: blackSolder, Class: Solider,     r: 1, c: 0, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 1, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 2, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 3, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 4, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 5, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 6, color: 'black' },
                      { img: blackSolder, Class: Solider,     r: 1, c: 7, color: 'black' }
                    ],

                    [],
                    [],
                    [],
                    [],
                    [
                      { img: whiteSolder, Class: Solider,     r: 6, c: 0, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 1, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 2, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 3, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 4, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 5, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 6, color: 'white' },
                      { img: whiteSolder, Class: Solider,     r: 6, c: 7, color: 'white' }
                    ],

                    [
                      { img: whiteRook,        Class: Rook,   r: 7, c: 0, color: 'white' },
                      { img: whiteHourse,      Class: Hourse, r: 7, c: 1, color: 'white' },
                      { img: whiteElephant,    Class: Alfil,  r: 7, c: 2, color: 'white' },
                      { img: whiteQueen,       Class: Queen,  r: 7, c: 3, color: 'white' },
                      { img: whiteKing,        Class: King,   r: 7, c: 4, color: 'white' },
                      { img: whiteElephant,    Class: Alfil,  r: 7, c: 5, color: 'white' },
                      { img: whiteHourse,      Class: Hourse, r: 7, c: 6, color: 'white' },
                      { img: whiteRook,        Class: Rook,   r: 7, c: 7, color: 'white' }
                    ],
                ];

```

ALl need first get square it exist on., as it OOP game, will be move method on character parent class, all inhirts can get, but if was tell if this class of king give this only this method will see instance likes

1. Important rule based on white or black it change direction for + on rows and minus, ex, white to move
frowrad he need minus row, as, (this for soliders only)

3. if last or first row, block movments can done sperate.
(note math used to final get I and r of target so getSqueras by Index and thats it


1. **The Rook**:
    - to move vertical from squares array get all cols same [i] except square it exist on it. (I call it verticalLine all)
    - to move horizontal from squares array get all cols from same row except col it within.  (I call it horizontal all)

2. The king (allow used methods[ verticalLineOne(this), horizontalOne(this), diagonallyOne(this)  ])
    - Note:first point u can get prev and after i of current pos, ex it in 1, so 0 and 2,
    - look below <br />
    `<1>`- First **(i+1,same r)**  -- **(i-1,same r)** if any horizontal <>  (I call it verticalLine one) <br />
    `|2|`- second **(r+1,same i)** -- **(r-1,same i)** if any vertical |   (I call it horizontal one) <br />
    `\/`3------>? ? **(i+1, r-1)** >/ --   **(i-1, r-1)** <\  ,,,,  **(i+1, r+1)** >\ -- **(i-1, r+1)** </  -> (diagonally one) **التحرك السموكسي** <br />
    `/\`

    - **Software diagrams and core js works for advanced info and more detials how it works**
        - 1. Digrams:
            - ![image](https://github.com/MahmoudHegazi/simple_chess_js/assets/55125302/06a558d5-95af-462c-bd80-1b01909b10a1)


-----------------------------------


##### next dev steps at part on ver5 require improve
require isready real function, count holders on it and chars and validate objects and forbiden the extra draw of peices when move as it htmlelm_jquery.remove() Iam wrong and forbiden in OOP game will handled with max chartacters classes when move count Not Forget check game Object data also i call this meta optional unlimited data sure or sqlalchemt GameError Table with relation ClientError, SocketError when socket inhirtance and other new discover


## the AI vs Computer 2 methods that beat any begniner and random 51% beat the number 1 chess player in world



OOP time, and sqlalchemy follow relationship nested , now we had squares with getAllGreen next get the square holders if any and if enemy class ! instanceof this so this 1 red posible kill and oop again will tell me what peaice, is hourse is queen is king and math time each peaee have weight so if king lol in getAllAttacksPossible in second move do it with same methods used by deep blue 1990 i did not used something not supported or react even or fancy lib 


## top methods AI without AI for bot my job
1. ```getAllGreenForAllPeaces()```
      -  which all allowed movments of all my peaces
2. ```getAllAttacksPossible()```
      - OOP time, and sqlalchemy follow relationship nested , now we had squares with getAllGreen next get the square holders if any and if enemy class ! instanceof this so this 1 red posible kill and oop again will tell me what peaice, is hourse is queen is king and math time each peaee have weight so if king lol in getAllAttacksPossible in second move do it with same methods used by deep blue 1990 i did not used something not supported or react even or fancy lib 

#### note about bot mode of this game
human never calc all posible w8 when *2 the after move and *3
mean calc if i move each char with forEach to square and what will be next reds possible
but here need based on new part which ignore 1 step player can make, for example he possible dead if hourse move 2 things solider and king so he must move one, so i may say try do this way based on peaice weight (which decide aggresive of bot to try get the high weight if player moved the wrong peaice but this will done even after socket to not lose internset in socket as this better feature)

