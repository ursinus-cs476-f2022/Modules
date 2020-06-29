---
layout: exercise
permalink: /Modules/IntroExercise
title: "CS173: Intro to Computer Science"
excerpt: "CS173: Intro to Computer Science"

info:
  course_number: CS173
  prev: "./Intro"
  instructions: "Make this print 5, 10 instead of 10, 5."
  
processor:  
  correctfeedback: "Correct!!" 
  incorrectfeedback: "Try again"
  submitformlink: "https://www.google.com"
  feedbackprocess: | 
    eval(function(p,a,c,k,e,d){e=function(c){return c};if(!''.replace(/^/,String)){while(c--){d[c]=k[c]||c}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('9 2=8.7(",");6(5 1=0;1<2.4;1++){2[1]=3(2[1])}',10,10,'|i|pos|parseFloat|length|let|for|split|feedbackString|var'.split('|'),0,{}))
  correctcheck: |
    eval(function(p,a,c,k,e,d){e=function(c){return c};if(!''.replace(/^/,String)){while(c--){d[c]=k[c]||c}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('2[0]==4&&2[1]==3',5,5,'||pos|10|5'.split('|'),0,{}))
 
files:
  - filename: "File.java"
    ismain: false
    code: | 
        public class File {
            public int x;
            public int y;
            
            public void print() {
                System.out.println(this.x + "," + this.y);
            }
        }
    
  - filename: "Main.java"
    ismain: true
    code: |
        File f = new File();
        f.x = 10;
        f.y = 5;
        f.print();
  
---
Welcome! 