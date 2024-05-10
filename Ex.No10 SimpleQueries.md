# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 06/05/2024                                                                     
### REGISTER NUMBER : 212221060123
### AIM: To write a prolog program to find the answer of query.
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
indoorgame(tabletennis).
easygame(X):-indoorgame(X).
hard(boxing).
likes(john,X):-food(X).
food(apple).
food(vegetable).
eats(bill,peanuts).
eats(sue,X):-eats(bill,X).
alive(bill).
```
### Output:
![image](https://github.com/muralikatta12/AI_Lab_2023-24/assets/124357793/ba114f67-c10c-4dc8-afb2-19f4516113ea)


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
    course(X,dept(havefun)).
course(bk301,dept(havefun)).
```
### Output:
![image](https://github.com/muralikatta12/AI_Lab_2023-24/assets/124357793/f1a9d6a4-545b-4443-88de-f683f40d3eff)


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
criminal(X):-
	american(X),
	weapon(Y),
	hostile(Z),
	sells(X,Y,Z).

weapon(Y):-
    missile(Y).

hostile(Z):-
    enemy(Z,X).

sells(west,Y,nano):-
    missile(Y),
	owns(nano,Y).

missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```
### Output:
![image](https://github.com/muralikatta12/AI_Lab_2023-24/assets/124357793/3a423ef7-c70f-4dc4-a783-1a3478ef2348)


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
