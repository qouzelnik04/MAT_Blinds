# Menu_structure CZ
uint8_t menu_layer[2]
//menu_layer[0] = vybira (okno(A,B,C,D)/nastaveni)
//menu_layer[1] = vybira (roztztahnout,zatahnout,stinini,cas,kalibrace,motory)
//menu_layer[2] = vybira (roztáhnout,zatahnout,stineni,1/3,2/3.............)



- menu_layer[0] = 0
- OKNO A
    - menu_layer[0] = 1
    - zpět
        - menu_layer[0] = 0
    - Roztáhnout
        - menu_layer[1] = 1
        - zpět
            - menu_layer[1] = 0
        - Roztáhnout
            - menu_layer[2] = 1
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 1/3
            - menu_layer[2] = 2
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 2/3
            - menu_layer[2] = 3
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - Manuální
            - menu_layer[2] = 4
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
    - Zatáhnout
        - menu_layer[1] = 2
        - zpět
            - menu_layer[1] = 0
        - Zatáhnout
            - menu_layer[2] = 5
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 1/3
            - menu_layer[2] = 2
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 2/3
            - menu_layer[2] = 3
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - Manuální
            - menu_layer[2] = 6
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
    - Stínění
        - menu_layer[1] = 3
        - zpět
            - menu_layer[1] = 0
        - Stínění
            - menu_layer[2] = 7
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 1/3
            - menu_layer[2] = 8
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - 2/3
            - menu_layer[2] = 9
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
        - Manuální
            - menu_layer[2] = 10
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[0] = 0
            - menu_layer[1] = 0
            - menu_layer[2] = 0
- OKNO B
    - menu_layer[0] = 2
    - -//-
- OKNO C
    - menu_layer[0] = 3
    - -//-
- OKNO D
    - menu_layer[0] = 4
    - -//-
/*
- OKNO E
    - menu_layer[0] = 5
    - -//-
- OKNO F

    - menu_layer[0] = 6
    - -//-  






*/
bk 0 a 1 vyuzity pro casy
bk 2 vyuzit pro invert
19 nastavena na 0xF0F0
kdyz nebude bk regisr nastaven tak to nesmi dovolit pouzivat zaluzie nejdriv kalibrace

bk 3 and 4 1/3
 


if(0xF0F0 == false)
    zaluzie dolu
if(0xFOFO == true)
    zaluzie dolu // kvuli kalibrace tak by meli byt dole
    kazdou polohu 
    vytahnbout nahoru

kalibrace  // pojedne
    zaluzie nahoru
    kdyz nahore zmacknou button
    pak dolu 

    1/3 stineni BK 3,4
    1/3         BK 5,6
    2/3 stineni BK 7,8
    2/3         BK 9,10
    stineni     BK 11,12
    zatahnout   BK 13,14
    current     BK 15,16


- NASTAVENI
    - menu_layer[0] = 7
    - zpět
       - menu_layer[0] = 0
    - Čas
        - menu_layer[1] = 4
        - zpět
            - menu_layer[1] = 0
        - Nas. Čas
            - menu_layer[2] = 1
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - Roztáhnout V:
            - menu_layer[2] = 2
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - Zatáhnout V:
            - menu_layer[2] = 3
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
    - Kalibrace
        - menu_layer[1] = 5
        - zpět
            - menu_layer[1] = 0
        - Kalibrace A
            - menu_layer[2] = 1
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - Kalibrace B
            - menu_layer[2] = 2
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - Kalibrace C
            - menu_layer[2] = 3
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - Kalibrace D
            - menu_layer[2] = 4
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
    - Motory
        - menu_layer[1] = 6
        - zpět
            - menu_layer[1] = 0
        - Test
            - menu_layer[2] = 1
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - invertovat A
            - menu_layer[2] = 2
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - invertovat B
            - menu_layer[2] = 3
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - invertovat C
            - menu_layer[2] = 4
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0
        - invertovat D  
            - menu_layer[2] = 5
            - void(menu_layer[0], menu_layer[1], menu_layer[2])
            - menu_layer[2] = 0





menu_layer[0] = 10; //0xF0F0 test - zkalibrovano

menu_layer[0] = 11; //neni - jede nahoru
    dokud nezmacknu
    curent = 4000
    required = 0 














- NASTAVENI
    - zpět
    - Čas
        - zpět
        - Nas. Čas
        - Roztáhnout V:
        - Zatáhnout V:
    - Kalibrace
        - zpět
        - Kalibrace A
        - Kalibrace B
        - Kalibrace C
        - Kalibrace D
    - Motory
        - zpět
        - Test
        - invertovat A
        - invertovat B
        - invertovat C
        - invertovat D