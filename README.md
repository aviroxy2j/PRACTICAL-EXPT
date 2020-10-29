# PRACTICAL-EXPT

#EXPT-3 #:Caesar Cipher
def cipher(txt):
    X=txt.split(' ')
    L=[]
    for I in X:
        A=''
        for J in I:
            M=chr(ord(J)+1)
            A+=M
        L.append(A)
    ciptxt=''
    for K in L:
        ciptxt=ciptxt + K + ' '
    print(ciptxt)
text=str(input('Enter your sentence:'))
print(cipher(text))
#




#EXPT-4
from datetime import time
ID=[]
OUT=[]
C='y'
def inputer(HO,MO,SO):
    while True:
        BID=str(input("enter the plane id:"))
        ID.append(BID)
        if BID=="ZZZ":
            break
        T1=time(HO,MO,SO)
        OUT.append(T1)
        print(ID)
        print(OUT)

def data(EID,HC,MC,SC):
    if ID==[] or ID==['ZZZ'] or ID[0]=="ZZZ":
        print("there are no bikes on the list")
    else:
        for I in range(len(L)):
            if EID == ID[I]:
                Time=OUT[I]
                print(EID)
                print(Time)
                H=Time.hour
                M=Time.minute
                S=Time.second
                h=HC-H
                m=MC-M
                s=SC-S
                OUTPUT=time(h,m,s)
                print(OUTPUT)
            else:
                print("Error:ID not found")
while C=='y':
    APP=str(input("Do you wish to input bike data or find the Bike? For former enter D and for latter enter T:"))
    if APP=="D":
        HO=int(input("enter out time hour:"))
        MO=int(input("enter out time minute:"))
         SO=int(input("enter out time second:"))
        inputer(HO,MO,SO)
    elif APP=="T":
        EID=str(input("enter bike id :"))
        HC=int(input("enter current time hour:"))
        MC=int(input("enter current time minute:"))
        SC=int(input("enter current time second:"))
        data(EID,HC,MC,SC)
    else:
        print("wrong input")
    C=input("Do u wish to continue with the program:")
    
    
    
    
#EXPT-5
PLANE=[]
DUE=[]
CALL=[]
C='y'
def inputer():
    while True:
        P=str(input("enter the plane id:"))
        PLANE.append(P)
        if P=="ZZZ":
            break
        D=int(input("enter take off time:"))
        DUE.append(D)
        C=int(input("enter calling time:"))
        CALL.append(C)
        
def identifier():
    if PLANE==[] or PLANE==['ZZZ'] or PLANE[0]="ZZZ":
        print("there are no planes waiting")
    else:
        print("next plane is ",PLANE[0],"due",DUE[0],'calling',CALL[0])
        PLANE.pop(0)
        DUE.pop(0)
        CALL.pop(0)
        L=len(PLANE)
        print("there are",L,"planes left for take off")
while C=='y':
    APP=str(input("Do you wish to input plane data or find the next plane for take? For former enter D and for latter enter T:"))
    if APP=="D":
        inputer()
    elif APP=="T":
        identifier()
    else:
        print("wrong input")
    C=input("Do u wish to continue with the program:") 
