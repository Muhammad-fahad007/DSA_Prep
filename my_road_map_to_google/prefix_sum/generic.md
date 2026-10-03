Notes :- 
for no of subarrays == k 
    At every right, current_prefix - k tells me which previous prefix sums would make a subarray ending at right have sum k. The frequency of that prefix tells me how many valid starting points exist.

