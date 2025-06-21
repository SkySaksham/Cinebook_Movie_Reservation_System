'''Create a Text File Named Staff.txt '''
''' if on windows edit clr() fn (line 40) as os.system('cls')'''





from colorama import *
import random as r
import time
import os



def sp(x) :                                                   ### To Leave x no. of lines
    for i in range(x) :
        head('') 


def mc() :                                                  ####  To Generate Random Text Colour
    b=[Fore.RED,Fore.CYAN,Fore.MAGENTA,Fore.GREEN,Fore.YELLOW,Fore.BLUE]
    l=r.randint(0,5)
    return b[l]
    
def head(y,x='',z='*') :                                ### Header (Text Allignment in middle)
    noc=Style.RESET_ALL
    a=x + str(y) + noc
    k=int((40-len(str(y)))/2)
    print(str(z)*10,' '*k,a,' '*(40-k-len(str(y))),str(z)*10)

def line(x,y=1,z="*")     :                             ###Line
   k=40-(int(y)+ len(str(x)))
   print(str(z)*10,' '*y,str(x),' '*k,str(z)*10)   

def stp(x) :                                                  ### Freeze Screen
    time.sleep(x)

def clr() :                                                     ### clear Screen
    os.system('clear')  

def hd(a=mc()) :                                         ### Heading  (in random colour)     
        head('—'*40)
        head('Movie Reservation System',mc())
        head('-'*40)
        sp(1)
        head('Welcome To',a,'*')
        head('SKY Theatres',a,'*')
        sp(1)
                                    
def movies() :                                             ###To Print No. Of Movies
        head('-'*40)
        global serial
        serial = []
        global file
        file=open('staff.txt','r+')
        global a   
        a=file.readlines()
        if len(a) ==0 :
            head('No Movies In Theatre !!')
        else :            
            head("All Movies in Theatre :")
            for b in a :
                serial.append(a.index(b))
                line(str(a.index(b))+' :'+b.strip())
            head('-'*40)  
                                  
def theatre(x) :                                                 ### Visual Representation Of Seats
    global l
    l="A   B   C   D   E   F   G   H"
    global data
    data=[]
    global seats
    seats = []
    def seat(x) :
        hd()
        head('-'*40)
        head(str(x))
        head('-'*40)
        sp(1)
        line('BD = BOOKED')
        sp(1)
        
        pp=mc()
            
        head(l)
        for i in range(1,9) :
            row='  '+str(i)+'  ' +pp
            for j in range(1,9) :                  
                if str(i) + str(j) in data :
                    row+='BD  '                  
                else :
                    row+='——  ' 
            row+='   '                                      
            head(row)
        head('')
        while True :
            sp(1)
            line('Price : ₹ 200/seat only',2)
            line("Want to Book a Seat (y/n) :",2)
            rpl = input('*'*10 +'    ')
            if rpl=='y' or rpl=='Y' or rpl =='n' or rpl == 'N' :
                break
            else :
                line('Give Appopriate Respose !',2)
        if rpl=='y'   or rpl == 'Y' :
            line('Enter Coulmn (eg, 1 2 3)',2)
            clm = input('*'*10 + '    ')
            line('Enter Row (eg, A B C)',2)
            ro=input('*'*10 + '    ')
            row=['A','B','C','D','E','F','G','H']
            if ro in row :
                if str(ro) + str(clm) in seats :
                    head('Seat Already Booked !')
                    head('—'*40)
                    stp(1)
                    clr()
                    seat(x)
                else :
                    data.append(str(clm) + str(row.index(ro)+1))
                    seats.append(ro+clm)                  
                    sp(2)
                    head('Seat Booked !')
                    head('—'*40)
                    stp(2)
                    clr()
                    seat(x)
            else :
                sp(2)
                head('Error!')
                head('—'*40)
                stp(2)
                clr()
                seat(x)                   
        else :
            sp(2)
            head('THANK YOU SIR')
            head('—'*40)
            stp(2)
            clr()                                                                       
    seat(x)

def ticket(x,y,z) :                                                            ### Print Out Ticket
    hd()
    head('TICKET')
    head('-'*40)
    head(y)
    sp(1)
    line('Reservation Confirmed : {} Tickets'.format(len(z)),2)
    for i in z :
        line('Seat {} : {} '.format(z.index(i)+1,i),2)
    line('Name : '+x[0],2)
    line('Age : '+ x[1],2)
    line('Contact : ' + x[2],2)
    line('Email Id : ' +x[3],2)
    line('Time : 3:00 PM to 6:00 PM',2)
    line('Amount Payable : {} ₹ only'.format(200*len(z)),2)
    head('HAVE A GOOT TIME SIR !')
    head('-'*40)
    sp(1)
    line('Kindly Pay Using Cash')
    head('—'*40)

def start() :                                                  ### 1st Interface
    a= mc()
    def pg(a) :
        head('—'*40)
        head('Movie Reservation System',mc())
        head('-'*40)
        sp(1)
        head('Welcome To',a,'*')
        head('SKY Theatres',a,'*')
        sp(2)
        line("Option")
        line("   1 : Staff")
        line("   2 : Customer")
        sp(2)
       
    while True :
        pg(a)
        op=input("*"*10+"   • Choose Your Option :")
        if op == '2' :
            line("WELCOME SIR !!")
            sp(4)
            head("  LOADING..")
            head('—'*40)
            stp(3)
            clr()
            break
        if op== '1' :
            line("• PassWord Sir :")
            nt=input('*'*10+"   ")
            if nt== '16082006' or nt == '03012007':
                       if nt=='16082006' :
                            op='1'
                       else :
                            op="3"                       
                       line("Welcome Sir")
                       sp(4)
                       head("   LOADING..")
                       head('—'*40)
                       stp(3)
                       clr()
                       break
            else :
                       sp(1)
                       line("Wrong PassWord !!")
                       line("Cancel Program And")
                       line("Try Again ...")
                       head('—'*40)
                       stp(1000000)                     
        else :
            line('Wrong Input !')
            line('Loading...')
            sp(3)
            head('–'*40)
            stp(2.3)
            clr()
            continue ;            
    return int(op)                                            

def start2(run) :                                                            ### 2nd Interface        
    if run == 1 or run == 3:
        hd()    
        if run==1 :
            line('Welcome Mr. Saksham Yadav')
        else :
            line('Welcome Mr. Aditya Yadav') 
        movies()
        while True :
            head('-'*40)
            sp(2)
            b=input("*"*10+'   Add More Movies (y/n) :')
            if b=='y' or b== 'Y' :
                l=input("*"*10+'  Name :')
                head("Adding..")
                head('—'*40)
                file.write(l+'\n')
                stp(1)
                clr()
                file.close()
                start2(run)
            if b=='n' or b== 'N' :
                head('THANK You Sir')
                sp(2)
                line('Close The Program !!')
                head('—'*40)
                stp(999999999)
                break                
    if run==2 :
        hd()
        sp(1)
        head('Enter Your Credentials :')
        sp(1)
        line('• NAME ---',2)
        Name=input("*"*10+'    ')
        sp(1)
        line('• AGE ---',2)
        Age=input("*"*10+'    ')
        sp(1)
        line('• MOBILE NO. ---',2)
        Mobile =input("*"*10+'    ')
        sp(1)
        line('• EMAIL ID ---',2)
        Email = input("*"*10+'    ')
        sp(1)
        head('Thank You Sir')
        sp(1)
        head('—'*40)
        stp(2)
        global userdata
        userdata=[Name , Age , Mobile, Email]
        clr()
 
        def jkk() :
            hd()
            line('Time Slot - 3PM to 6PM')
            line('Only time Available')
            line('Sorry For Inconvenience Caused !')
            movies()
            while True :
                line("Which Movie (Enter Serial No.) :")
                user=input('*'*10+'   ')
                if user in str(serial) :
                    sp(1)
                    head('Thank You')
                    sp(1)
                    head('—'*40)
                    stp(2)
                    clr()
                    break
                else :
                    head('Enter Appopriate Input')
                    head('-'*40)
            global movie_name                        
            movie_name = a[int(user)]
            

        jkk()
        theatre(movie_name.strip())
        ticket(userdata,movie_name.strip(),seats)
               

start2(start())                                                                  ###RUN