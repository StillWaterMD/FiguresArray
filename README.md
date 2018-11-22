# FiguresArray

program creates Frame exibits few randomly generated figures.

Code structure:
1. Class MainFunction - contains main function where Frame is created and expanded with MyController and Exibition canvas
2. Class Pair - contains pair of integers. further it used to store coordinates
3. Interface print contains function print:
   3.1 Class PrintOval. implements print, this class will be using ti print ovals
   3.2 Class PrintPolygon. implements print, this class will be used to connect any set of dots in class figure (it can be random        set, line, rectangle, triangle and ect.)
4. Class Figure is contaner for set of coordinates and interface print for diffirent print() functions:
  4.1 Class Oval describes ovals, by coordinates of center and  width/height, there are 2 constructors -  with randomly generated parameters based on container form and  with inputed parameters (this one is not used yet in code). Either way parameters are transformed to set of coordinates - left top corner of described rectangle, the most left point of oval and the most top point of oval. Coordinates are stored in ArrayList of parent class, interface printer stores object of PrintOval class
  4.2 Class Line. Basic line - described by coordinates of start and end. there are 2 constructors as well - randomly generated line based on container and inputed parameters. Coordinates are stored in ArraList of parent class, interface printer stores object of PrintPolygon class
  4.3 Class Polygon - just set of coordinates. like in other classes this one contains 2 constructors, coordinates are stored in ArrayList of parent class and printer contains PrintPolygon object
  4.4 Class rectangle. Describes rectangle with coordinates of top left corner and width/height. Contains 2 constracors pretty much same to previous. Parameters transformed into coordinates stored in ArrayList of parent class, printer contains object of PrintPolygon class
5. Class MyContoller - simple controller which only reacts for pressing [x] button of the Frame. works as "Close window" function
6. Class FigureList - contains ArrayList of Figures, there are also some basic funtions like remove, add, get and print
7. Class ExibitionCanvas basicly field where all figures are printed. There are 2 constructors - 1st takes FigureList as parameter and 2d dont. 1st constructor is not used in code. There is also function to generate FigureList filled with few figures based on size of Frame
