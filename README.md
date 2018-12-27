# loginform.py
Login form for a community
def loginform():
	
    f = open("loginform.txt", "a")
    
    print("Hello.  To join this community \nwe need to know some things about you.")
    
    aname = input("Please enter your first name: ")
    
    bname = input("Please enter your surname: ")
    
    age = int(input("Please enter your age: "))
    
    print("\nYour name is " + aname + " " + bname + " and you are " + str(age) + " years old")
    
    if int(age) < 12:
    	
        print("You are too young for this site")
        return
        
    while True:
    	
        email = input("Please enter your email address: ")
        
        email1 = input("Please confirm your email address: ")
        
        if email != email1:
            print("\nThe email addresses don't match.")
            
        else:
        	
            break
            
    while True:
    	
        pw = input("Please enter a password: ")
        
        pw2 = input("Re-enter your password: ")
        
        if pw != pw2:
        	
            print("The passwords don't match.")
            
        else:
        	
            break
            
    detail = (aname + "\n" + bname + "\n" + str(age) + "\n" + email + "\n" + pw)
    
    #print(detail)
    
    f.write(detail)
    
    f.close()
