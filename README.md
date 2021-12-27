c   Bita 16
org 0x7C00
;--------------------------------------
jmp Main

Main:
mov si. msg
call Print

Print:
lodsb
cmp al, 0
je return
mov ah, 0eh
int 10h
jmp Print
return:
ret 

msg db    'Loading red Queen' ,0
;--------------------------------------
tiems S10-($−$$)      db    0 
dw  0xAA55
