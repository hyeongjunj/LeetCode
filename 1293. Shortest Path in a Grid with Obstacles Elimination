class Solution {
public:
    int shortestPath(vector<vector<int>>& grid, int k) {
      queue<pair<pair<int,int>, int>> Q;
      Q.push({{0,0},0});
      pair<pair<int,int> , int> location_;
      int count_obs_ = 0;
      int path_cost_ = 0;
      int min_path_cost_ = 2147483647;
      int m = grid.size();
      int n = grid[0].size();
      int x, y, cost;
      while(!Q.empty()) {
       location_ = Q.front();
       x = location_.first.first;
       y = location_.first.second;
       cost = location_.second;
       // grid[x][y] = -1; 
       // check visited place 
       Q.pop();
       path_cost_++;
       if(grid[x][y]) { 
         // this location has obstacle
         count_obs_++;
       }
       if(x == m-1 && y == n-1) {
         // reach to our destination <m,n>
         std::cout<<cost<<"\n";
       }
       else { 
         if(x > 0   &&   grid[x-1][y] != -1) 
           Q.push({{x-1, y},cost+1});
         if(x < m - 1 && grid[x+1][y] != -1) 
           Q.push({{x+1, y},cost+1});
         if(y > 0   &&   grid[x][y-1] != -1)  
           Q.push({{x, y-1},cost+1});
         if(y < n - 1 && grid[x][y+1] != -1) 
           Q.push({{x, y+1},cost+1});
       }
      }
      return -1;
    }
};
