![image](https://github.com/shruti3032/Learning/assets/78202217/e2eae241-c586-433d-af79-a146b99e2918)


# Euler Circuit in an Undirected Graph

# Approach 1


// User function Template for Java

class Solution {
    public boolean isEularCircuitExist(int v, ArrayList<ArrayList<Integer>> adj) {
        // Code here
        for(ArrayList<Integer> al: adj){
            if(al.size()%2!=0)
                return false;
        }
        return true;
    }
}

# Approach 2
class Solution {
    // Method to check if an Eulerian circuit exists in a graph
    public boolean isEularCircuitExist(int V, ArrayList<ArrayList<Integer>> adj) {
        // Iterate through all vertices in the graph
        for (int i = 0; i < adj.size(); i++) {
            // Get the number of neighbors of the current vertex
            int listSize = adj.get(i).size();
            // If the number of neighbors is not even, return false
            if (listSize % 2 != 0) {
                return false;
            }
        }
        // Return true if all vertices have even degrees
        return true;
    }
}

# MY LOGIC

Elurian circuit is when we are traversing the graph an dstart with one point and end with same point. 
my logic: if every edge has 2 vertices like adjacent vertices then graph contains elurian circuit, otherwise not.
An Eulerian circuit is a circuit that uses every edge exactly once and starts and ends at the same vertex

