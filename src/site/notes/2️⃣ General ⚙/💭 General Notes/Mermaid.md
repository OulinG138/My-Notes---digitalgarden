---
{"dg-publish":true,"dg-home":false,"permalink":"/2-general/general-notes/mermaid/","dgPassFrontmatter":true}
---

```mermaid
flowchart LR
	A -- Great --> C -.-> B
```
```mermaid
flowchart LR
	A -. Great .-> C
```
```mermaid
flowchart LR
A-.->B
```
```mermaid
classDiagram
direction TD
	Employee <|-- SalariedEmployee: Inheritance
	Employee <|-- HourlyEmployee: Inheritance
	class Employee{
		<<abstract>>
		-first_name: str
		-last_name: str
		-social_security_number: int
		+earnings() str
		}
	class SalariedEmployee{
		-first_name: str
		-last_name: str
		-social_security_number: str
		-Weekly_salary: float  
		+earnings() float
	}
	class HourlyEmployee{
		-first_name: str
		-last_name: str
		-social_security_number: str
		-wage: float
		-hours: float
		+earnings() float
	}
```
```mermaid
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
```

```mermaid
pie showData
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```



```mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```


```mermaid
graph TD
	1 --- 2
	2 --- 3
	3 --- 4
	3 --- 5
	2 --- 6
	1 --- 7
	8 --- 9
	9 --- 10
	9 --- 11
	8 --- 12
	1 --- 8
```

```mermaid
classDiagram
class Square{
    -id: int
    -position: list[int]
    +setPoints(List~int~ points)
    +getPoints(): List[int]
	+getMessages(): Union[int, str]
}

Square : +withdrawal(amount) Union[int, str]
```

```mermaid1
classDiagram 
classA --|> classB : Inheritance 
classC --* classD : Composition 
classE --o classF : Aggregation 
classG --> classH : Association 
classI -- classJ : Link(Solid) 
classK ..> classL : Dependency 
classM ..|> classN : Realization 
classO .. classP : Link(Dashed)
```