# assignment5
challenge1
class Point:
    def_init_(self,x,y,z):
    self.x=x
    self.y=y
    self.z=z
  def sqSum(self):
    return(self.x)**2+(self.y)**2+(self.z)**2

  point1=Point(1,3,5)
  print(point1.sqSum())
  
  challenge-2
  class Calculator:

    def _init_(self,num1,num2):
      self.num1=num1
      self.num2=num2
    def add(self):
      return self.num1+self.num2
    def multiply(self):
      return self.num2*self.num1
        def subtract(self):
      return self.num1-self.num2
    def divide(self):
      return self.num2/self.num1

    obj=Calculator(10,94)
    print(obj.add())
    print(obj.subtract())
    print(obj.multiply())
    print(obj.divide())

  challenge-3:
  class Student:
    def getname(self):
      return self._name
        def getRollnum(self):
      return self._Rollnum
        def setname(self,name):
      return self._name=name
            def setRollnum(self):
      return self._Rollnum=Rollnum
    demo1=Student()
    demo1.setname("afreen")
    print("Name:",demo1.getname())
    demo1.setRollnum(1432)
    print(:Rollnum:",demo1.getRollnum())
    
  chalenge-4
  Implement a Banking Account
class Account:
    def __init__(self, title=None, balance=0):
        self.title = title
        self.balance = balance


class SavingsAccount(Account):
    def __init__(self, title=None, balance=0, interestRate=0):
        super().__init__(title, balance)
        self.interestRate = interestRate
        
challenge-5
 Handling a Bank Account
class Account:  # parent class
    def __init__(self, title=None, balance=0):
        self.title = title
        self.balance = balance

    def withdrawal(self, amount):
        self.balance = self.balance - amount

    def deposit(self, amount):
        self.balance = self.balance + amount

    def getBalance(self):
        return self.balance


class SavingsAccount(Account):
    def __init__(self, title=None, balance=0, interestRate=0):
        super().__init__(title, balance)
        self.interestRate = interestRate

    def interestAmount(self):
        return (self.balance * self.interestRate / 100)
demo1 = SavingsAccount("Mark", 2000, 5)  # initializing a SavingsAccount object


class BankAccount:
    # create the constuctor with parameters: accountNumber, name and balance 
    def __init__(self,accountNumber, name, balance):
        self.accountNumber = accountNumber
        self.name = name
        self.balance = balance
        
    # create Deposit() method
    def Deposit(self , d ):
        self.balance = self.balance + d
    
    # create Withdrawal method
    def Withdrawal(self , w):
        if(self.balance < w):
            print("impossible operation! Insufficient balance !")
        else:
            self.balance = self.balance - w
    # create bankFees() method
    def bankFees(self):
        self.balance = (95/100)*self.balance
        
    # create display() method
    def display(self):
        print("Account Number : " , self.accountNumber)
        print("Account Name : " , self.name)
        print("Account Balance : " , self.balance , "Rs")
        
# Testing the code :
newAccount = BankAccount(181909121511, "Samchandu" , 2700)
# Creating Withdrawal Test
newAccount.Withdrawal(300)
# Create deposit test
newAccount.Deposit(200)
# Display account informations
newAccount.display()
        print(str(e))


main()
