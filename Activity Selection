class Solution:
    def activitySelection(self, start, finish):
        if not start or not finish:
            return 0  # No activities available
        
        # Sort activities first by finish time, then by start time to break ties
        activities = sorted(zip(finish, start))
        
        max_activities = 1  # The first activity is always selected
        last_finish_time = activities[0][0]  # Finish time of first activity
        
        for i in range(1, len(activities)):
            start_time, finish_time = activities[i][1], activities[i][0]
            if start_time > last_finish_time:  # Strictly greater to avoid overlap
                max_activities += 1
                last_finish_time = finish_time  # Update last finish time
        
        return max_activities
