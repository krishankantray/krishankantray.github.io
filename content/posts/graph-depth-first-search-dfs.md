+++
author = "Krishankant"
authorTwitter = ""
cover = ""
date = 2021-10-10T13:06:20Z
description = "Fundamental problems to solve DFS based problems easily."
draft = true
keywords = []
showfullcontent = false
tags = ["DFS", "graph"]
title = "Graph - Depth First Search (DFS)"

+++
## Some basic problems to make DFS undestanding strong

#### Preorder Binary Tree Traversal

```cpp
vector<int> preorderTraversal(TreeNode* root) {
    stack<TreeNode*>s;
    s.push(root);
    vector<int>ans;
    while(!s.empty()){
    	TreeNode* cur=s.top();
    	s.pop();
    	if(!cur) continue; 
    	ans.push_back(cur->val);
    	s.push(cur->right); // first push right because in Stack LIFO works
        s.push(cur->left);
    }
    return ans;
}
```