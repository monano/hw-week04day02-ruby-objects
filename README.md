# Ruby Objects Homework

## Objectives:

- Apply your knowledge of Ruby to solve a real world problem.
- Get really good at Ruby classes and objects

## Activity

Create a program that models a subway system.

The program takes the line and stop that a user is getting on at and the line and stop that user is getting off at and prints the journey and the total number of stops for the trip in the console:

There are 3 subway lines:

**Red line**
- South Station
- Park Street
- Kendall
- Central
- Harvard
- Porter
- Davis
- Alewife

**Green line** 
- Government Center
- Park Street
- Boylston
- Arlington
- Copley
- Hynes
- Kenmore

**Orange line**
- North Station
- Haymarket
- Park Street
- State
- Downtown Crossing
- Chinatown
- Back Bay
- Forest Hills

All 3 subway lines intersect at Park Street, but there are no other intersection points.

### Goal

Tell the user the number of stops between stations using ruby classes.
```rb
#this will create obj the line
class Subway
  def stops_between_stations(start_line, start_station, end_line, end_station)
  Red = Line.new
  Red.trans(start_station,end_station,[ "South Station","Park Street","Kendall","Central","Harvard","Porter","Davis","Alewife"])
  obj line red
  obj line green
  obj line orange
  end

end
  
# One line, all the stations on that line
#this will create obj the station
class Line
def trans(start_station,end_station,stations)
@start_station = start_station
@end_station = end_station
@stations = station

st1 =Station.new(@station[@station.indexof(start_station)])
end
# def trans
# st1=Station.new(station_name)
# obj station 1
# obj station 2
# .
# .
# .
# obj station n
# end

end

# One station

class Station
  def initialize(name)
  @name = name
  end
  def station_name
  p @name
  end
end
```

And we should be able to find the number of stops with
```rb
mbta = Subway.new
mbta.stops_between_stations('Red', 'Alewife', 'Red', 'Alewife') # 0
mbta.stops_between_stations('Red', 'Alewife', 'Red', 'South Station') # 7
mbta.stops_between_stations('Red', 'South Station', 'Green', 'Kenmore') # 6
```

### Bonus

Tell the user the number of stops between stations AND the stops IN ORDER that they will pass through or change at.
```rb
mbta = Subway.new
mbta.stops_between_stations('Red', 'South Station', 'Green', 'Kenmore') 
# "You must travel through the following stops on the Red line:"
# "South Station and Park Street"
# "Change at Park Street."
# "Your trip continues through the following stops on Green Line:" 
# "Boylston, Arlington, Copley, Hines, and Kenmore."
# "7 stops in total."
```

### Double Bonus

Use `get` to allow the user to input their start line, start station, end line, and end station.