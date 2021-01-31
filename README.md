print("Welcome to ATM machine")
a=0.00
l=1234
q=3
M=[2222]
I=int(input("Insert the card:"))
if I in M:
    while 1:
        print('''                press 1 for balance
                press 2 for deposit
                press 3 for withdrawl
                press 4 to end the transaction
                press 5 to change pin''')
        n=int(input("Press here:"))
        if n==1:
            p=int(input("Enter pin:"))
            if p==l :
                q=3
                print('''                        press 1 for savings account
                        press 2 for current account ''')
                N=input()
                print(f'''The amount is :{a}
                      Press 1 to continue
                      press 2 to end the transaction''')
                o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
            else:
                q-=1
                if q==0:
                        print("Exceeded the number of attempts\n Please try after 24hrs\n Thank you visit again")
                        break
                else:
                        print(f'''                           Invalid pin
                                {q} attempts left''')
                        
                        print('''                      Press 1 to continue
                          press 2 to end the transaction''')
                        o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
        elif n==2:
            p=int(input("Enter pin:"))
            if p==l:
                q=3
                print('''                    press 1 for savings account
                    press 2 for current account ''')
                N=input("Press here:")
                A=int(input("Put the denomitions in the specified area:"))
                if A%10==0 and len(str(A))>2:
                    a+=A
                    print(f'''Transaction is successful. The amount is successfully added to your account.
                                press 1 to continue
                                press 2 to end the transaction''')
                    o=int(input("Press here:"))
                    if o==1:
                        continue
                    elif o==2:
                        print("Thank you visit again")
                        break
                    
                else:
                    print("Enter a valid amount")
            else:
                q-=1
                if q==0:
                        print("Exceeded the number of attempts\n Please try after 24hrs\n Thank you visit again")
                        break
                else:
                        print(f'''                           Invalid pin
                                {q} attempts left''')
                        
                        print('''                      Press 1 to continue
                          press 2 to end the transaction''')
                        o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
        elif n==3:
            p=int(input("Enter pin:"))
            if p==l:
                q=3
                print('''                        press 1 for savings account
                         press 2 for current account''')
                N=input("Press here:")
                A=int(input("Enter the amount you want to with draw:"))
                if A<=a:
                    if A%100==0 and A<=20000:
                            a-=A
                            print(f'''Transaction complete: amount is {a}''')
                    else:
                        print("Enter valid amount\n The amount should be multiple of 100 and not more than 20000")
                    
                else:
                    print("Insufficient balance")
                print('''                        Press 1 to continue
                        press 2 to end the transaction''')
                o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
            else:
                q-=1
                if q==0:
                        print("Exceeded the number of attempts\n Please try after 24hrs\n Thank you visit again")
                        break
                else:
                        print(f'''                           Invalid pin
                                {q} attempts left''')
                        
                        print('''                      Press 1 to continue
                          press 2 to end the transaction''')
                        o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
                
        elif n==4:
            print("Thank you visit again")
            break
        elif n==5:
            p=int(input("Enter the old pin:"))
            if p==l:
                x=int(input("Enter the new pin:"))
                y=int(input("Re-enter the new pin:"))
                if x==y:
                    l=x
                    print("Pin successfully changed")
                else:
                    print("Values does not match")
                print('''                          Press 1 to continue
                          press 2 to end the transaction''')
                o=int(input("Press here:"))
                if o==1:
                    continue
                elif o==2:
                    print("Thank you visit again")
                    break
                
            else:
                print("Enter valid pin")
        else:
            print("Invalid option")
