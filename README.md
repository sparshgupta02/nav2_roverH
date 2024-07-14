# nav2_roverH
This repository is to store documentations

![Alt Text](flowchart.png)

Distance_to_goal:

This function uses the Haversine formula to calculate the distance between initial position and goal position.
This use GPS to get the distance only once while initiating the code.

```
def distance_to_goal(self):
    	a = math.pow(math.sin((self.goal_lat - self.initial_lat)*math.pi/360),2)+
            math.cos(self.goal_lat*math.pi/180)*math.cos(self.initial_lat*math.pi/180)*math.pow(math.sin((self.goal_long - self.initial_long)*math.pi/360),2)
    	c = 2*math.atan2(math.sqrt(a), math.sqrt(1-a))
    	print(f"a = {a}, c = {c}")
    	self.distance = 6371 * c *1000
    	self.distance_calculated = True
```

