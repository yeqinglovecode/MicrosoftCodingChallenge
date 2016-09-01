Congratulations! You've won an all-expenses paid weekend trip courtesy of Xortholian Air. Xortholian Air's airplanes are world-renowned for their wonderful hospitality, so you've decided to spend as much time as possible on an airplane this weekend before ending up in a relative's city.

The company will allow you to take any number of flights, to any airports, at any time, for a grand total of two days (48 hours, or 2,880 minutes). You can choose whatever flight path you want (including visiting airports multiple times) so long as you start in your home airport and end in your relative's airport.

Your goal is to determine a flight path satisfying those requirements: one that maximizes the amount of time you spend airborne.

You can spend any amount of time at airports between flights, including 0 minutes. Xortholians have excellent indoor transportation methods.

Input definition

Your input will start with two lines, followed by a blank line.

The first line will be the name of your starting airport.
The second line will be the name of your ending airport.
The rest of the input will be a series of 50 to 75 airport descriptors. An airport descriptor consists of the airport name on one line, followed by 15 to 25 flight descriptors, then a blank line. A flight descriptor contains a flight id, departure airport, and arrival airport in the following format:

Flight {FlightId} from {Departure_Airport} at {Departure_Time} to {Arrival_Airport} at {Arrival_Time}
Xortholians are understanding of the woes of string parsing, so airport names will contain underscores instead of spaces ("Greater_L'howon_Heights" rather than "Greater L'howon Heights"). They're also understanding of the woes of time parsing, so times will be in minutes from the start.

Flight ids will all be unique four-digit numbers. They won't start with 0.

Output definition

Your output file should contain the list of flights you've chosen, in the order in which you plan to take them. Each flight should be listed on its own line and represented by its flight id.

Example input

Start_Airport
End_Airport

Start_Airport
Flight 819 from Start_Airport at 0 to End_Airport at 120
Flight 343 from Start_Airport at 30 to Middle_Airport at 60

Middle_Airport
Flight 117 from Middle_Airport at 90 to End_Airport at 210

End_Airport
Flight 9696 from End_Airport at 240 to Middle_Airport at 300
Example output

343
117
