# Airport
Because in reality, one often has multiple positions that he/she needs to get to when in an airport. For example, he/she needs to check in the luggage, consult flight information, and arrive at the waiting hall before the flight. Therefore, I designed a multiple points guidance algorithm. The Unity3D is used to simulate and realize the several destination route arrangements. Because the key point of this project is to realize the route navigation, the model of the complicated airport is simplified to several basic brown blocks, the white escalator connects the first floor and the second floor. Square blocks with different color represent different users. In this project, I set four users each with their corresponding destinations.

The system first gets the position of each input destinations and connect them with straight lines, which is the minimum distance between two points. Then, the square block, which represent the user, will move along the arranged route to get to their destinations. This model also allow viewer to change the view angle by sliding or right-clicking mouse.

The original state and the guidance stage is shown in figure 2 and figure 3.

Now, let us focus on one user, to show the guidance process. You can see that there are two yellow users who share the same move direction, but with different height. The fourth yellow user is at the first floor, and the first yellow user is at the ground floor. It is clear that the system can explicitly catch the height information of the input destination points and these two users can flow the guidance correctly. Then, for the blue and green blocks, their path is more complexed and distanced. Here the algorithm manages all the destination points together, and the route is reasonable that can save user's time and energy. You can see that the blue and green blocks can automatically detect the obstacles blocks in their way and choose the shortest way to walk across them.

Figure 4 shows the code realizing the multiple-destination guidance, the core idea is first storing the positions and number of destinations, then calculate the distance and manage the order. After passing one point, the count will decrease accordingly.

P.S. Important information

Guide for opening unity project:

1. Use the same unity3D version 2021.1.17f1c1 to open the project.

2. When running the game, click **Gizmos** option.

3. All codes are in the Scripts
