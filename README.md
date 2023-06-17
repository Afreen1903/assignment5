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
  class Account:
    def __init__(self,owner,balance=0):
        self.owner = owner
        self.balance = balance
        
    def __str__(self):
        return f'Account owner:   {self.owner}\nAccount balance: ${self.balance}'
        
    def deposit(self,dep_amt):
        self.balance += dep_amt
        print('Deposit Accepted')
        
    def withdraw(self,wd_amt):
        if self.balance >= wd_amt:
            self.balance -= wd_amt
            print('Withdrawal Accepted')
        else:
            print('Funds Unavailable!')

         # 1. Instantiate the class
acct1 = Account('Afreen',100)

# 2. Print the object
print(acct1)

# 3. Show the account owner attribute
acct1.owner

# 4. Show the account balance attribute
acct1.balance

# 5. Make a series of deposits and withdrawals
acct1.deposit(50)

acct1.withdraw(75)

# 6. Make a withdrawal that exceeds the available balance
acct1.withdraw(500)

#challenge-5
class BankAccount():

    def __init__(self, acct_no, balance):
        if balance < 0:
            raise ValueError('Balance cannot be negative')
        self._account_number = acct_no
        self._balance = balance

    def withdraw(self, amount):
        if amount < 0:
            raise ValueError("Withdrawn amount is negative.")
        if amount > self._balance:
            raise ValueError('Dont have sufficient balance')
        self._balance -= amount

    def deposit(self, amount):
        if amount < 0:
            raise ValueError("Deposit amount is negative.")
        self._balance += amount

    def getBalance(self):
        return self._balance


class CheckingAccount(BankAccount):

    def __init__(self, acct_no, balance, fees, minimumBalance):
        super().__init__(acct_no, balance)
        self._fees = fees
        self._minimumBalance = minimumBalance
        if self.checkMinimumBalance():
            self.deductFees()

    def deductFees(self):
        print('${} deducted for not maintaining sufficient balance'.format(self._fees))
        self._balance -= self._fees

    def checkMinimumBalance(self):
        return self.getBalance() < self._minimumBalance


def withdraw(self, amount):
    super().withdraw(amount)

    if self.checkMinimumBalance():
        self.deductFees()


def __str__(self):
    return 'Account Number: {}, Current Balance: ${:.2f}'.format(self._account_number, self.getBalance())


class SavingsAccount(BankAccount):
    def __init__(self, acct_no, balance, interest_rate):
        super().__init__(acct_no, balance)
        self._interest_rate = interest_rate

    def addInterest(self):
        interest = self.getBalance() * self._interest_rate / 100
        self.deposit(interest)


def main():
    id = input('Enter checking account id: ')
    balance = float(input('Enter checking account initial balance: '))
    min_balance = float(input('Enter minimum balance to be maintained: '))
    fees = float(input('Enter fees to be deducted for not maintaining minimum balance: '))
    try:
        checkAccount = CheckingAccount(id, balance, fees, min_balance)
        print(checkAccount)
    except Exception as e:
        print(str(e))


main()
