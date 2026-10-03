# Interval Pattern Cheat Sheet (DSA)

## 1. Recognize an Interval Problem

Look for: - Intervals, ranges, start/end pairs - Meetings, schedules,
bookings - Time slots, events, reservations

Examples: - Merge Intervals - Insert Interval - Meeting Rooms -
Non-overlapping Intervals - Employee Free Time - Minimum Arrows

------------------------------------------------------------------------

## 2. Identify the Goal

Most interval problems fall into one of these categories:

  Pattern                  Typical Goal
  ------------------------ ------------------------------------
  Merge                    Combine overlapping intervals
  Detect Overlap           Check if intervals intersect
  Remove Overlap           Remove minimum intervals (Greedy)
  Find Free Time           Find gaps between intervals
  Count Active Intervals   Meeting Rooms, simultaneous events
  Cover Everything         Minimum Arrows, Video Stitching

------------------------------------------------------------------------

## 3. Sort First (Usually)

Most interval problems start with sorting.

-   By **start time** → Merge, Insert, Overlap
-   By **end time** → Greedy scheduling, Activity Selection

Sorting usually reduces the problem to a single linear scan.

------------------------------------------------------------------------

## 4. Maintain One State

Common variables: - `current_end` - `previous_interval` -
`merged_interval` - `earliest_end` (heap)

------------------------------------------------------------------------

## 5. Compare Adjacent Intervals

After sorting, you usually only compare: - Previous interval - Current
interval

Avoid comparing every interval with every other interval.

------------------------------------------------------------------------

## 6. Overlap Rule

Given:

    A = [s1, e1]
    B = [s2, e2]

(after sorting so `s1 <= s2`)

Overlap if:

    s2 < e1

No overlap if:

    s2 >= e1

------------------------------------------------------------------------

## 7. If They Overlap...

Decide what the problem wants:

-   Merge them
-   Remove one
-   Count them
-   Allocate another room/resource

For greedy removal problems: - Keep the interval with the **smaller end
time**.

Reason: It leaves maximum room for future intervals.

------------------------------------------------------------------------

## 8. Think Locally (Greedy)

Instead of optimizing globally, ask:

> "What is the best interval to keep right now?"

Typical greedy choices: - Earliest ending interval - Merge immediately -
Reuse earliest available room

------------------------------------------------------------------------

# Common Templates

## Merge Intervals

1.  Sort by start.
2.  Scan once.
3.  Merge overlaps.
4.  Append non-overlapping intervals.

------------------------------------------------------------------------

## Non-overlapping Intervals

1.  Sort.
2.  Maintain previous end.
3.  On overlap:
    -   Increment answer.
    -   Keep interval with smaller end.
4.  Else update previous end.

------------------------------------------------------------------------

## Meeting Rooms II

1.  Sort by start.
2.  Maintain a min-heap of ending times.
3.  Reuse room if earliest meeting has ended.
4.  Otherwise allocate a new room.

------------------------------------------------------------------------

## Insert Interval

1.  Add intervals before the new interval.
2.  Merge overlaps.
3.  Append remaining intervals.

------------------------------------------------------------------------

## Sweep Line

Convert intervals into events:

    Start -> +1
    End   -> -1

Sort events and track active intervals.

Useful for: - Maximum overlap - Calendar problems - Skyline - Meeting
Rooms

------------------------------------------------------------------------

# Quick Recognition Guide

If you see...

-   **start/end** → Think intervals
-   **meeting/schedule** → Interval problem
-   **merge** → Sort by start
-   **minimum removals** → Greedy
-   **maximum activities** → Sort by end
-   **rooms/resources** → Heap
-   **free time** → Merge first, then find gaps

------------------------------------------------------------------------

# Mental Decision Tree

``` text
Intervals?
        |
        v
Need ordering?
        |
      Sort
        |
        v
Overlap?
        |
   +----+----+
   |         |
 Merge?   Remove?
   |         |
 Merge    Greedy (keep smaller end)
        |
        v
Need multiple active intervals?
        |
     Heap / Sweep Line
```

------------------------------------------------------------------------

# Five Questions to Ask Every Time

1.  Should I sort?

    -   By start or by end?

2.  What defines an overlap?

3.  What state should I maintain?

4.  If intervals overlap, should I:

    -   Merge?
    -   Remove one?
    -   Count?
    -   Allocate another resource?

5.  Can I solve it in one linear scan after sorting?

If you build the habit of answering these five questions first, you'll
recognize and solve most interval problems much faster.
