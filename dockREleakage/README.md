# dockREleakage

In this challenge we are given a docker image. The idea of the challenge is to teach a valueble lesson and to direct players into learn on docker. This is basic and fun challenge.

Solution:

The first part of the flag can be retrieved by the following steps:
1. Loading the docker image into the machine using the command:
docker load -i <tarball file>
2. Deploying an instance of the image and enter into it. Within the container we can find a file named flag.txt which contains part of the flag. 

Second intended part should be to "reversing the image" and retrieve it's dockerfile. Within the dockerfile we can find a base64 encoded plaintext which is the second part of the flag.
It can be retrieved by using different methods such as:
1. Using docker history command
2. Checking the json file that contains information about all the different layers and can hide interesting information. 

Since docker layers are just tarballs files saved locally we can also just untar the tarball and retrieve the p-flag.txt file which is copied as step 3 within the dockerfile.


