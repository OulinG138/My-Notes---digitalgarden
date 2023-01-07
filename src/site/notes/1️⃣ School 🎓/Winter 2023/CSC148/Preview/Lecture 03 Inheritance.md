---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-03-inheritance/"}
---

# 抽象，继承，多态

```toc
```

&nbsp;


## Inheritance 
```python
class Cat(object):

    def __init__(self, name='George', color='black') -> None:
        self.name = name
        self.color = color
    
    def run(self):
        print(f'{self.name} is running.')
    

class Dog(Cat):
    pass


if __name__ == '__main__':
    dog = Dog()
    print(dog.name)
    print(dog.color)
```

&nbsp;

## Abstract Classes
```python
class Creature(object):

    def eat(self):
        raise NotImplementedError 
		# We should add this function in each of the subclass.

class Cat(Creature):

    def __init__(self, name='George', color='black') -> None:
        self.name = name
        self.color = color
    
    def run(self):
        print(f'{self.name} is running.')
    

class Dog(Cat):
    pass


if __name__ == '__main__':
    cat = Cat()
    cat.eat()
```

&nbsp;

## Superclass


```python
class Employee(object):

    def __init__(self, first: str, last: str, ssn: str) -> None:
        self.__first_name = first
        self.__last_name = last
        self.__social_security_number = ssn
    
    def earnings(self) -> float:
        raise NotImplementedError


class SalariedEmployee(Employee):

    def __init__(self, first: str, last: str, ssn: str, salary: float\
    ) -> None:
        super().__init__(first, last, ssn)
        self.__weekly_salary = 0 if salary < 0 else salary


    def earnings(self) -> float:
        return self.__weekly_salary


class HourlyEmployee(Employee):
    def __init__(self, first: str, last: str, ssn: str, wage: float, \ hours: float) -> None:

        super().__init__(first, last, ssn)
        self.__wage = 0 if wage < 0 else wage
        self.__hours = hours if 0 <= hours <= 168 else 0


    def earnings(self) -> float:
        if self.__hours <= 40:
            return self.__wage * self.__hours
        else:
            return self.__wage * 40 + (self.__hours - 40) * self.__wage * 1.5


class Company(object):

    def __init__(self) -> None: #多态: 将子类装到list里
        self.employees = []
        # self.employees: list[Employee] = list()

    def add_employee(self, employee) -> None:
        self.employees.append(employee)
    
    def pay_all(self):
        for emp in self.employees:
            print(emp.earnings())
        #【print(emp.earnings()) for emp in self.employees]


if __name__ == '__main__':
    company = Company()
    emp1 = SalariedEmployee('Kevin', 'Zhao', '0001', 300)
    emp2 = HourlyEmployee('Andy', 'Qiang', '0002', 20, 42)
    company.add_employee(emp1)
    company.add_employee(emp2)
    company.pay_all()
```
