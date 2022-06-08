# algebralang

Algrabralang is a programming language that is designed to be easy to write and implement complicated algorithms.

Algrebralang works differently to other languages but looks like Python without significant whitespace. Functions are arranged in a call graph and topologically sorted so control flow and looping looks different to other programming languages.

Algebralang is an expression and algebra language that manages iteration for you.

The goal of the language is to define exactly what relationships are true and let the computer resolve them.

Whereas other languages use functional variable application and recursive data structures algebralang uses recursive code and recursive callstacks.

It's important to think of each function as being executed in concurrently even though this is an illusion.

# ÷(point=[middle]=m)

Many algorithms rely on dividing information in half, so algrabelang defines a division operator which works on lists.

# binary search

```
recursive( initialValue(node1.children, s)

÷(point=middle=m,sides=s)
value(m) == input = output = m
if value(m) > searchValue then s=s[0] else s=s[1]
)
```

# a star

```
insert index priorityQueue value = {
recursive( initialValue(priorityQueue, s)
÷(point=middle=m,sides=s)
size = len(s) if size == 0 then s.insert(value)
if index[str(value)] < index[str(m)] then s=s[0] else s=s[1]
)
}

neighbours node =
= neighbours = [(node[0] + 1, node[1]),
(node[0], node[1] + 1),
(node[0] - 1, node[1]),
(node[0], node[1] - 1),
(node[0] + 1, node[1] + 1),
(node[0] - 1, node[1] - 1),
(node[0] + 1, node[1] - 1),
(node[0] - 1, node[1] + 1)
]
path ComeFrom target = {
= path ComeFrom (ComeFrom.get(str(target)) or reject)
}

astar map start target heuristic = {
gScore = {}
fScore = {}
ComeFrom = {}
gScore[str(start)] = 0
fScore[str(start)] = heuristic(start)
OpenSet = [start]
recursive(OpenSet, item=current,
neighbours(current), item=neighbour {
OpenSet.remove(0)
euclidean_range(name=range, current, neighbour)
if str(current) == str(target) then = path ComeFrom target
tentative_gScore = gScore[str(current)] + range
if tentative_gScore < gScore[current] then {
  if neighbour not in OpenSet then insert fScore OpenSet neighbour
  ComeFrom[neighbour] = current
  gScore[str(neighbour)] = tentative_gScore
  fScore[str(neighbour)] = tentative_gScore + heuristic(neighbour) 
}
})
}
```

# travelling salesman problem

```
tsp cities = {
(array(name=pairs)=cities
.permutations(name=pair, 2))
.permutations(name=solution, previous=s[i][1], size=len(cities), value+=(solution[-1][1], solution[0][0]))
thread(solution, rule(index, item)=(if item[i][0]==item[i-1][1] then item[i][0] else reject, item[i][1]))
euclidean_distance(name=distance, pair[0], pair[1])
euclidean_distance(name=solution_distance, solution)
sort(name=per_order, distance, order=ascending)
sort(name=solution_order, solution_distance, order=ascending)
pairs = first(per_order, solution_order)
= pairs
}
```

# btree

```
insert t node = recursive_deepest_first(items=t.children,item=t,
lastRecursion=l)(
if len(t.children) == 0 t.activate()
location = reversed(t.children).find(item=i, item.value >= node.value)
output = insert t node
if len(t.children) > 3 {
replace(t, Node(value=t.children÷(point=middle=m) 
= m.value,children.sort(item=i,sortKey=i.value)=t) 
output = l.t }
else deepest t.children.append(node)
)
```
