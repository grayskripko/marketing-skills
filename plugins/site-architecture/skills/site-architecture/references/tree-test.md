# Reading pasted tree-test results

Only for results the user pastes. Planning a study or a card sort is out of scope.

## Per task

- n = participants who attempted the task.
- Success = share who ended at a correct location. Directness = share who got there without backtracking. Both as k/n with a Wilson 95% interval, z = 1.96:
  centre = (p + z²/(2n)) / (1 + z²/n); half-width = z · sqrt(p(1−p)/n + z²/(4n²)) / (1 + z²/n).
- First click: share of first clicks per top-level item, and the share that went to the correct top-level item.

## Bands for task success (Albert and Tullis via NN-tree)

| Success rate | Band |
|---|---|
| below 40% | poor |
| 41% to 60% | fair |
| 61% to 80% | good |
| 80% to 90% | very good |
| above 90% | excellent |

Boundaries as published; this plugin reads them as <40, 40–60, >60–80, >80–90, >90 (convention of this plugin).

NN-tree reports a median of 62% across the 98 studies and stresses that the team's own earlier results are the better comparison. Show the band as context, never as a pass mark; when a task's interval spans two bands, say so.

## Reading rules (NN-tree)

- Most first clicks correct but success low → the lower-level labels under that item overlap; make the subcategory labels more distinct.
- First clicks spread across several top-level items → the item may belong in more than one place or the grouping does not match how people think; if this happens on many tasks, revisit the overall grouping.
- Low directness with acceptable success → people find it after trying other branches; check the labels they tried first.

## Sample size

NN-tree says comparisons between two trees typically need 50 or more participants per tree for narrow intervals. Below that, print "below the size NN/g suggests for comparing trees" and compare tasks only through their intervals.
