---
layout: post
title: Quadtree
# subtitle: Each post also has a subtitle
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
tags: [c++][recursion][data structures]
comments: true
---

I did this project for [UBC's CPSC 221 course](https://courses.students.ubc.ca/cs/courseschedule?pname=subjarea&tname=subj-course&dept=CPSC&course=221). The detailed description of this project can be found [here](https://www.students.cs.ubc.ca/~cs-221/2019W1/mps/p3/), and my code for this project can be found [here]().

I implemented a quad-tree data structure, which is a [tree](<https://en.wikipedia.org/wiki/Tree_(data_structure)>) where each node can have up to four children. Each node of the tree represents a group of pixels in an image. The quad-tree splits its leaf nodes to decrease the color variability across its leaf nodes. I implemented recursive algorithms to perform the splits, until a given parameter representing the maximum number of leaf nodes the tree can have, the "leaf bound", is reached. I implemented two different versions of this recursive splitting algorithm; one which performs splits to produce a (possibly) imbalanced quad-tree, and one that produces a [self-balancing tree](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree). The splits might incur imbalance between the heights of the subtrees; that is, similar to an [AVL Tree](https://en.wikipedia.org/wiki/AVL_tree), the tree would be considered "unbalanced" when the height difference of its subtrees becomes greater than 2. The self-balancing quad-tree possibly incurs additional neighboring splits upon every required split, if the quad-tree becomes imbalanced with this split.

This quad-tree data structrue is an application of image compression, since the tree selectively only the nodes with higher color variability than others in the original image, until a given bound is reached. Thus, the output image has reduced color detail in areas that do not contain much color variability in the original image, by representing them with smaller number of nodes, but maintains detail in areas containing lots of variability in the original image, by representing them with greater number of nodes.

See if you can figure out which of these is the unbalanced tree, and the self-balancing tree!

![First example]({{ site.url }}/projects/quadtree/out-smallFrame.png)
![First example]({{ site.url }}/projects/quadtree/out-smallFrameBal.png)

How about now?:)

![Second example]({{ site.url }}/projects/quadtree/out-ada.png)
![Second example]({{ site.url }}/projects/quadtree/out-adaBal.png)