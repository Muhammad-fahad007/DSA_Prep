
Kadane Pattern — Quick Recognition Notes
🔎 Recognition Triggers
Contiguous subarray / substring / segment
Need maximum / minimum / best value
Often involves sum, but can be product, cost, score, etc.
Ask: “What is the best answer ending at index i?”
🧠 Core Mental Model
Extend or Restart
At every element:
Continue the previous segment
        OR
Start a new segment here
Classic:
cur = max(nums[i], cur + nums[i])
ans = max(ans, cur)

🚨 Variations
Problem variation	What to think
Maximum sum	Classic Kadane
Minimum sum	Reverse Kadane
Circular array	max_sum OR total - min_sum
Product	Track max + min
One deletion	Add deletion-used state
Absolute sum	Track max + min
Custom values/costs	Transform → Kadane
Kadane vs Others
Prefix Sum → relationship between two prefix states
Sliding Window → maintain a valid window/constraint
Kadane → find the best contiguous segment using extend vs restart
⭐ One-Line Recognition
Contiguous + optimize a value + best answer ending here → think Kadane.
