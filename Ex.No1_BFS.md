# Ex.No: 1  Implementation of Breadth First Search 
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:


graph= {
         2:[3,4],
         3:[5],
         4:[6,7],
         5:[6],
         6:[],
         7:[8],
         8:[],}

def bfs(visited,node,graph): 
    queue=[]
    queue.append(node)
    visited.append(node)
    while queue: 
        
        poped_node=queue.pop(0)
        print(poped_node)
        
        for child in graph[poped_node]: 
            
            if child not in visited: 
                queue.append(child)
                visited.append(child)
print("the order is")
bfs([],2,graph)





### Output:

<img width="655" alt="image" src="https://github.com/muralikatta12/AI_Lab_2023-24/assets/124357793/9f056910-6811-4731-9e31-b1c14b4b25a8">


### Result:
Thus the breadth first search order was found sucessfully.
