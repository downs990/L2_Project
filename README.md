# L2_Project
Description: 

Simulate traffic in a city grid with vehicles, streets and intersections. Vehicles drive around randomly and change direction at each intersection. Each object in the city grid will run independently in its own thread.

Project Tasks
Task L2.1 : In method Vehicle::drive(), start up a task using std::async which takes a reference to the method Intersection::addVehicleToQueue, the object _currDestination and a shared pointer to this using the get_shared_this() function. Then, wait for the data to be available before proceeding to slow down.

Task L2.2 : In method Intersection::addVehicleToQueue(), add the new vehicle to the waiting line by creating a promise, a corresponding future and then adding both to _waitingVehicles. Then wait until the vehicle has been granted entry.

Task L2.3 : In method WaitingVehicles::permitEntryToFirstInQueue(), get the entries from the front of _promises and _vehicles. Then, fulfill promise and send signal back that permission to enter has been granted. Finally, remove the front elements from both queues.
 

Dependencies:
-   OpenCV 

How to run this project:

    root@a9ad274128c4:/home/workspace/L2_Project# mkdir build
    root@a9ad274128c4:/home/workspace/L2_Project# cd build
    root@a9ad274128c4:/home/workspace/L2_Project/build# cmake ..
    root@a9ad274128c4:/home/workspace/L2_Project/build# make
    root@a9ad274128c4:/home/workspace/L2_Project/build# ./traffic_simulation
