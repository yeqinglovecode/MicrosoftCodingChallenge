You are an airline consultant who has been tasked with improving plane boarding times. The airline in question has been plagued with a set of customers that appear to be very bad at finding their seats. You suspect these passengers are just lazy and that there is a pattern to their movement. In order to test your theory, you will plot these "lazy" passengers' movements through a plane.

Given a plane layout and a passenger list (in boarding order) with the "lazy" passengers tagged, your task is to plot the path that the "lazy" passengers take to their final seat to confirm your theory.

Input definition

The input will consist of:

The width of the plane (always an even number between 2 and 26).

The length of the plane (between 1 and 1000 rows).

A comma separated list of passengers that describes the seats that they are assigned, the order in which they board, and whether or not they are lazy (indicated with an asterisk). You can assume the list will contain no more passengers than the number of seats on the plane and that it will contain at least one passenger. There will be a minimum of 1 and a maximum of 100 lazy passengers.

Consider this example passenger list:

A1,B2,C7,A2,D3*,A3

The first passenger on to the plane will be A1 (1 based index rather than 0), followed by B2, and so on. Each of the non-lazy passengers will simply take their seats. Our first lazy passenger is the fifth person to board the plane. They will simply find the first available seat that they prefer and sit there. If a subsequent passenger is to occupy a seat a lazy passenger is in, the lazy passenger will move to the next closest seat according to their preferences.

Lazy passengers will always first choose seats closer to the front of the plane (lower numerical values) and then the left most seats in a given row (lower alphabetical values). This holds true for boarding the plane as well: given an empty plane, a lazy passenger will always sit at A1. Further, every seat in a given row (increment letter values) must be exhausted before a lazy passenger will move on to the next row (increment numerical values).

Front of Plane

Seat A	Seat B	Seat C	Seat D
Row 1	A1	B1	C1	D1
Row 2	A2	B2	C2	D2
Row 3	A3	B3	C3	D3
Rear of Plane

Output definition

The output will be a series of rows that describes the path of seats taken by each lazy passenger.

Each row should correspond to a single lazy passenger and rows should be in the order that the lazy passengers boarded the plane (i.e. the order in that they appeared in the passenger list input). The individual rows should contain a comma separated list of the seats that each lazy passenger occupied.

Example input

2
9
A1,A6,B2,A3,B4,B3,A5*,A7,B1,B5,A2
Example output

B1,A2,A4
