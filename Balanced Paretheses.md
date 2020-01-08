# Balanced Paretheses


class Stack():
    
    def __init__(self):
        self.open=[]
    def push(self,string):
        global flag #Declaring flag global here
        if len(string)==0:
            print('Yes')
            exit(0)
        for i in range(0,len(string)):
            if string[i] in "({[":
                self.open.append(string[i])
            else:
                if string[i] in ")}]":
                    if self.open==[]:
                        print('No')
                        exit(0)
                    if self.open.pop() in "({[":
                        flag=0
                    else:
                        flag=1
                        break
    def check(self):
        if flag==0:
            print('Yes')
        else:
            print('No')
s=Stack()
n=input()
s.push(n)
s.check()
