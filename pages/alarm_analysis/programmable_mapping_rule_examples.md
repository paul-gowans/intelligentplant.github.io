# Programmable mapping rule examples

For example, to convert an EventType "Alarm\_RTN" to RTN you could use
the following code:

``` c#
var type = Convert.ToString([[EventTypeName]]);
if(type.Equals("Alarm_RTN"))
{
      return "RTN";
} 
else {
      return type;
};
```

8-o

To assign a priority order, you could use something like this:

``` c#
var priority = "P" + [[Priority]]; return priority;
```
