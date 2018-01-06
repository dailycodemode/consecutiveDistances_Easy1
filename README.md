https://www.reddit.com/r/dailyprogrammer/comments/759fha/20171009_challenge_335_easy_consecutive_distance/?sort=confidence

	inputs = ["76 74 45 48 13 75 16 14 79 58 78 82 46 89 81 88 27 64 21 63",
		  "37 35 88 57 55 29 96 11 25 42 24 81 82 58 15 2 3 41 43 36",
		  "54 64 52 39 36 98 32 87 95 12 40 79 41 13 53 35 48 42 33 75",
		  "21 87 89 26 85 59 54 2 24 25 41 46 88 60 63 23 91 62 61 6",
		  "94 66 18 57 58 54 93 53 19 16 55 22 51 8 67 20 17 56 21 59",
		  "6 19 45 46 7 70 36 2 56 47 33 75 94 50 34 35 73 72 39 5"]

	for x in range(len(inputs)):
	    inputs[x] = inputs[x].split()

	gap = 1

	for line in range(len(inputs)):

	    sumDistance = 0
	    for x in inputs[line]:
		distance = 0
		target = [str(int(x) + gap), str(int(x) - gap)]

		for y in range(inputs[line].index(x) + 1, len(inputs[line])):
		    distance += 1
		    if inputs[line][y] in target:
			sumDistance = sumDistance + distance

	    print(sumDistance)

