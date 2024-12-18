import networkx as nx
import matplotlib.pyplot as plt

# Define the nodes and edges, incorporating the annotations
nodes = [
    '0 (All characters 0)', 
    '(Change: Character 1, 0 -> 1)', 
    'Node 1', 
    'Node 2', 
    'Node 3', 
    'A (6)',  # Include the numbers with the leaf nodes
    'B (2, 5, 10)', 
    'C (3, 4, 7, 9, 8)', 
    'D (8)'
]
edges = [
    ('0 (All characters 0)', '(Change: Character 1, 0 -> 1)'), 
    ('(Change: Character 1, 0 -> 1)', 'Node 1'), 
    ('Node 1', 'Node 2'), 
    ('Node 1', 'Node 3'), 
    ('Node 2', 'A (6)'), 
    ('Node 2', 'B (2, 5, 10)'), 
    ('Node 3', 'C (3, 4, 7, 9, 8)'), 
    ('Node 3', 'D (8)')
]

# Create the tree using NetworkX
tree = nx.Graph()
tree.add_nodes_from(nodes)
tree.add_edges_from(edges)

# Visualize the tree
pos = nx.spring_layout(tree)  # You can experiment with different layouts
nx.draw(tree, pos, with_labels=True, node_size=2000, node_color="skyblue", font_size=8) 
plt.title("Annotated Tree Visualization")
plt.show()
