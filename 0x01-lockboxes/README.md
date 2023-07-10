# 0x01. Lockboxes

## This task involves determining whether all the boxes in a given list of boxes can be opened. Each box is represented as a list, where the index of the box corresponds to its number. The boxes may contain keys to other boxes.

## To solve this task, we use a breadth-first search (BFS) algorithm. Starting from the first box (index 0), we explore the boxes one by one, keeping track of the visited boxes. We add the first box to the visited set, then iterate through its keys to find the next boxes to visit. If a key corresponds to a box that has not been visited before and is within the valid range of box indices, we mark it as visited and add it to the queue. We continue this process until there are no more boxes left to visit in the queue.

## Once the BFS traversal is complete, we check if the number of visited boxes is equal to the total number of boxes. If they are equal, it means that all the boxes can be opened since we have visited all of them. In that case, we return `True`. Otherwise, if there are unvisited boxes, it means that at least one box cannot be opened. In that case, we return `False`.
