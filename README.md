# Latch-Tracker
Latch-Tracker is an descriptor matching based tracking algorithm. At a initial bounding box or patch from previous frame, it builds Latch descriptors at SIFT keypoints and then matches it using BruteForce matcher to get the best match for a keypoint in the next frames' candidate area(the candidate area is a tunable parameter). Floating point descriptors have been used for tracking due to their accuracy of matching, but descriptors like LATCH have been proved to show performance which is comparable  to floating point descriptors. Also, binary descriptors are known to be much faster as compared to floating point descriptors i.e SIFT.

The repository contains a CMakeLists.txt which could be use to fetch a MakeFile.
Hit make in command line.
then, ./<executable>
