# Shortest Flight Path Simulator

**PURPOSE**: Analyze OpenFlights routes and airports datasets by implementing BFS, DFS, Dijkstra's algorithm, and the Landmark Path algorithm. Data from given text files are processed into an efficient graph structure, and there are several user options to test the functionality of the graph.

**AUTHORS**: Calvin Lee, Edward Guo, Tejus Kurdukar, Gloria Xiao

**VERSION**: 12/7/2020

**HOW TO START**: Compile by running "make", then execute ./airports

## USER INSTRUCTIONS

When running ./airports, a menu will display various options to analyze the flights data structure, and a number must be entered
followed by the enter key to choose an option. Note that the graph is built such that each vertex represents an airport and an edge exists between
two vertices if there exists a direct flight between the two airports. The graph is undirected and it is not specified whether an airport is a
source or a destination of a route that it is connected to. Note that for each menu option that requires user input, the 4-digit ICAO code
of the airport must be entered, not the 3-digit IATA code or any other identifier. The code must be entered in capital letters. All flights
are simplified to be traveled in a straight line.

## MENU DETAILS

The first three options on the menu are tests to verify that the graph structure and BFS/DFS algorithms are correctly implemented. 
These options will parse the "test_airports.dat" and "test_routes.dat" data files, two smaller sublists of data from the OpenFlights
datasets that each contain ten data entries. The graph can be found in the repository "BFS/DFS Test Graph.pdf"
The outputs for each will be directly printed to the console in a readable way so that the user can 
draw out the graph on their own and verify that the output is correct, as well as be able to track the order in which BFS/DFS visits each vertex 
and edge. For vertex labels, a 0 label represents an unvisited node (never appears in output) and a 1 respresents a visited node. For edges, a 0 is
undiscovered, a 1 is discovery, and a 2 is a cross/back edge.

The fourth and fifth options on the menu verify Dijkstra's and the Landmark algorithm on separate sample test graphs, not one of the test data
files. A drawing of the test graph can be found in the repository "Dikjstra Test Graph.pdf"
The data will be displayed for each graph before running each algorithm so that the graph can be drawn on paper and the algorithms can be 
verified.

The sixth and seventh options on the menu are used to run Dijkstra's and Landmark on user-inputted airports. Option 6 will specifically find the
shortest route between two user-inputted ICAO codes and will display the path of vertices that must be traversed to get from the first airport to
the second. Option 7 is similar, but is used with a third airport input to see the shortest route between the first two that goes through the third
airport. Again, the 4-digit ICAO codes must be entered and no other input; invalid input or an airport not in the graph will prompt the program
to display an error message and ask to retry input.

Option 8 uses two user-inputted airports to check if there exists an edge between them.
Option 9 displays the degree of a given airport vertex.
Option 10 prints the ICAO codes of all of the adjacent airports of a given airport vertex.
Option 11 displays miscellaneous information about the airport. 

Exit the program by inputting 12 on the keyboard.

## PRESENTATION VIDEO

Skip to the second recording on this link, should be 13 minutes long. 
https://illinois.zoom.us/rec/play/KxGVcdj0WNLyVlA6u-bBp79GrJnNgi5SbtMDOt3WpYtuaEZFyBQ6Q6zVijoOeVHiHGyo9cvlvgMkqkBM.qAkP76vBa12spR_J?_x_zm_rhtaid=59&_x_zm_rtaid=Tv_93xOHQSaYY2LlO7sXdw.1607660368548.596ee4a72574325c61092e835b3cd79f&autoplay=true&continueMode=true&startTime=1607659025000
