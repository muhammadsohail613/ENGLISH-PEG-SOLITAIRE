# ENGLISH-PEG-SOLITAIRE

In this project we were expected to get a solution path for english peg solitaire by applying 5 different search algorithms with limited time and if necessary limited memory. The game starts with the following board below called INITIAL and reaches to goal state with the following board below called SOLUTION which are located under i​tem.py​file.


Searching Algorithms(s​earch.py)​
a. Breadth First Search:
Current board state is chosen from head of frontier list and new states created from current states are sorted in a sublist according to their ​move_values​ and appended to the frontier list. I had to put a memory limit on this because my computer didn’t work well after it reached huge memory usage, I couldn’t save even move pointer so I put keyboard interrupt option which turns current sub optimal solution and it also stops when memory limit is reached. So I couldn’t make it run 1 hour but I put memory limit that I will need the program not to interrupt my computer usage and it runned almost 210 seconds. It had visited 1,347,089 nodes which is not a lot but in the frontier list it had 1,202,132 nodes which makes use of memory. I assume that if I run it 1 complete hour it will just get to 8th depth level and the rest will freeze my computer. The sub optimal board state can be seen below and the rest of outputs are located under ​output_files/bfs.txt.​



# b. Depth First Search:
Depth First Search was easy to implement didn’t consume so much memory. New states are appended to frontier list and current node selected was last element of frontier list. It ended up searching after 833 seconds which is almost 14 minutes by visiting 7,667,889 nodes and in the frontier list just 118 nodes left, memory is free which is good. The game board for each move state can be seen in ​output_files/dfs.txt.​




# Functions
search.py
Breadth First Search:
def​​bfs​(cur_node,point_table,time_limit): Depth First Search:
def​​dfs​(cur_node,point_table,time_limit): Iterative Deepening Search:
def​​ids​(cur_node,point_table,time_limit): Depth First Search with Random Selection:
def​​dfs_rand​(cur_node,point_table,time_limit): Depth First Search with Special Selection:
def​​dfs_spec​(cur_node,time_limit): mynode.py
MyNode Class
board.py
Except Board class it had make_moves function with given peg coordinate and direction and return a new board:
def​​make_move​(board_array_param,x,y,direction) heuristic.py
Manhattan Distance implemented here:
def​​man_dist​(board_array):
item.py
all small calculation functions and variables are located here.
