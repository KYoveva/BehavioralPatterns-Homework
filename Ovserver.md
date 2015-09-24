# Observer Pattern
## Мотивация 
* Дефинира зависимостта един-към-много между различни обекти, така че когато един обект бъде променен, всички зависими от него обекти
да бъдатт уведомени и да се  актуализирани.

## Употреба
* Когато един обект зависи от друг.
* Когато промяната на един обект изисква промяна в много други обекти.
* Когато промени в даден обект следва да уведомят други обекти, без те да знаят нищо за тези промени.

## Имплементация
```c#
using System;
using System.Collections.Generic;

public class BaggageInfo
{
   private int flightNo;
   private string origin;
   private int location;

   internal BaggageInfo(int flight, string from, int carousel)
   {
      this.flightNo = flight;
      this.origin = from;
      this.location = carousel;
   }

   public int FlightNumber {
      get { return this.flightNo; }
   }

   public string From {
      get { return this.origin; }
   }

   public int Carousel {
      get { return this.location; }
   }
}
```

## UML диаграма
![](http://www.evietonline.com/wp-content/uploads/2015/09/observer-pattern-nlug6pdb.png)
  
