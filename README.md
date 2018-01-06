https://www.reddit.com/r/dailyprogrammer/comments/759fha/20171009_challenge_335_easy_consecutive_distance/?sort=confidence

	 def rate(line, difference=1):
	     nums = {int(n):i for i, n in enumerate(line.split())}
	     s = sorted(nums)
	     rating = 0
	     for i, j in zip(s, s[1:]):
		 if j - i == difference:
		     rating += abs(nums[i]-nums[j])
	     return rating

	 for x in range(len(inputs)):
	     inputs[x] = inputs[x].split()
	     print(rate(x)) 
	
