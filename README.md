a='y'

while(a=='y'): 
    print("1.Insert task.")
    print("2.Display tasks.")
    print("3.Update status of a task.")
    print("4.Remove a task.")
    n=int(input("Enter your choice: "))

    if(n==1):
        l=[]
        k=int(input("Enter no.of tasks: "))
        for i in range (0,k):
            m=input("Enter task: ")
            l.append(m)

    elif(n==2):

        print()
        for i in range (0,k):
            print(l[i])
        print()

    elif(n==3):

        print("1)Mark as pending.")
        print("2)Mark as completed.")
        j=int(input("Enter choice: "))

        if(j==1):
            m=int(input("Enter task to be updated: "))
            l[m-1]=l[m-1]+" --> Pending"
            print()
            for i in range (0,k):
                print(l[i])    
        else:
            m=int(input("Enter task to be updated: "))
            l[m-1]=l[m-1]+ " --> Completed"
            print()
            for i in range (0,k):
                print(l[i])

    elif(n==4):

        r=int(input("Enter task no. to be removed: "))
        print(l[r-1]," removed!")
        l.remove(l[r-1])
        k=k-1

    else:
        print("invalid choice")
    
    a=input("Do you want to continue(Enter y/n): ")
    print()
    
    if(a=='n'):
        break
