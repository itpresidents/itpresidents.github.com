---
title: Putting Objects into Arrays
author: Steve
layout: post
permalink: /putting-objects-into-arrays/
categories:
  - ICM
---
# 

Here’s a small Processing sketch to exhibit working with arrays of Objects. I’ve split the sketch up in to 2 sections, “setting” a Point to each position in the array and then going through the array and getting the object out of the array.

If you have any questions, please put them in the comments and I’ll do my darnedest to answer.

    class Point {
      int year;
      int population;
      float rateOfChange;
      
      
      Point(int _year, int _population){
        year = _year;
        population = _population;
      }
    }
    
    Point[] points;
    
    void setup() {
      size(400,400);
      points = new Point[10];
      
      println("SET 'points'");
      
      for(int i=0; i < points.length; i  ) {
        int newYear = 1900   i*5;
        int newPop = (int)random(30000);
        println(i   " "   newYear   " "   newPop);
        
        // Create a new Point instance and set its year and population
        Point newPoint = new Point(newYear, newPop);
        // Store newPoint into the points array.
        points[i] = newPoint;
      }
      
      println("GET from 'points'");
      
      for(int i = 0; i < points.length; i  ) {
        // Get the ith Point from the points array and store it as 'tempPoint'
        Point tempPoint = points[i];
        // Print out attributes of tempPoint
        println(i   " "   tempPoint.year   " "   tempPoint.population);
      }
    }