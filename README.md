# raicamp2025

   #####Dictionary in Modile Robot
   #     A
   #    / \
   #   B   C
   #  / \   \
   # D   E   F
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': [],
    'F': []
  }
start = 'A'
goal = 'E'
frontier = [start]
explored = set() #Use a set for unique (ignore duplicate append)

print(frontier, explored)

while len(frontier) > 0:
  current = frontier.pop()# Remove and put into varaible
  print(current)
  if current == goal:
    print("Goal reach")
    break
  print(f"neighbor of {current}is {graph[current]}")
  
  for neighbor in graph[current]:
      frontier.append(neighbor)




