+++
author = "Krishankant"
authorTwitter = ""
cover = "/uploads/image.png"
date = 2021-11-05T19:58:04Z
description = "DFS approach to detect cycle in directed and undirected graphs"
keywords = []
showfullcontent = false
tags = ["graph", "dfs", "cycle-detection"]
title = "Cycle detection in directed and undirected graphs"

+++
## Cycle detection in graph

**Undirected graph :**

To detect cycle in an undirected graph we do not need any extra space apart from maintaining a `visited[]` array. We just need to keep tract of parent of current node so that the algorithm excludes the single edge loop condition.

Code ( **C++**) : ( [github link](https://github.com/krishankantray/Graph-Algorithms/blob/master/cycle_detection_undirected_graph.cpp "github link") )

```cpp
#include <bits/stdc++.h>
using namespace std;
class Solution {
    public:
        bool isCycle(vector<vector<int>>&adj, vector<bool>&vis, int parent, int cur){
            vis[cur]=true;
            for(int node:adj[cur]){
                if(!vis[node]){
                    if(isCycle(adj, vis, cur, node))
                    	return true;
                }
                else{
                    return node!=parent ; 
                }
            }
            return false;
        }
        bool detectCycle(int V, vector<vector<int>>&adj){
            vector<bool>vis(V, false);
            for(int i=0; i<V; i++){
                if(!vis[i]){
                    if(isCycle(adj, vis, -1, i))
                        return true;
                }
            }
            return false;
        }
}
int main() {
    int V; // number of vertices
    int E; // number of edges
    vector<vector<int>>adj(V); // adjancency matrix
    cin>>V>>E;
    int u,v; 
    while(E--){
        cin>>u>>v;
        adj[u].push_back(v);
        adj[v].push_back(u); // for undirected graph u->v  also imples v->u
    }
    Solution s = new Solution();
    cout<<s.detectCycle(V, adj);
    return 0;
}
```

**Directed graph :**

In directed graph we need to keep tract of `visited[]` nodes and also currently processing dfs stack. 

C++ Code : ( [github link](https://github.com/krishankantray/Graph-Algorithms/blob/master/cycle_detection_in_directed_graph.cpp "Github link") )

```cpp
#include <bits/stdc++.h>
using namespace std;
class Solution {
    public:
        bool isCycle(vector<vector<int>>&adj, vector<bool>&vis, vector<bool>&dfsVis, int parent, int cur){
            vis[cur]=true;
            dfsVis[cur]=true;
            for(int node:adj[cur]){
                if(!vis[node]){
                    if(isCycle(adj, vis, cur, node))
                        return true;
                }
                else if(dfs[cur]){
                    return true ;
                }
            }
            dfsVis[cur]=false;
            return false;
        }
        bool detectCycle(int V, vector<vector<int>>&adj){
            vector<bool>vis(V, false);
            vector<bool>dfsVis(V, false);
            for(int i=0; i<V; i++){
                if(!vis[i]){
                    if(isCycle(adj, vis, dfsVis, -1, i))
                        return true;
                }
            }
            return false;
        }
}
int main() {
    int V; // number of vertices
    int E; // number of edges
    vector<vector<int>>adj(V); // adjancency matrix
    cin>>V>>E;
    int u,v; 
    while(E--){
        cin>>u>>v;
        adj[u].push_back(v);
    }
    Solution s = new Solution();
    cout<<s.detectCycle(V, adj);
    return 0;
}
```