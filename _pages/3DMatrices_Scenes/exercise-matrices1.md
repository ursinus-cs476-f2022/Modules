---
layout: exercise_matrix
permalink: "Scenes/Exercise1"
title: "CS 476: Computer Graphics - Scenes Module Exercise 1"
excerpt: "CS 476: Computer Graphics - Scenes Module Exercise 1"
canvasasmtid: "100575"
canvaspoints: "1"

info:
  prev: "./Video1"
  next: "./Video2"
  points: 1
  instructions: "<p>Construct a single matrix that stretches by a factor of 3 in the y direction, and which then translates by the vector (1, 2, -1)</p><div id = \"matrixdisplay\"></div>"
  goals:
    - Work with fundamental examples of matrix multiplications to transform 3D shapes
    - Work with homogenous coordinates for combinations of linear transformations and translations
    
processor:  
  correctfeedback: "Correct!!" 
  incorrectfeedback: "Try again"
  submitformlink: false
  setupprocess: |
    let matrixDisplay = document.getElementById("matrixdisplay");
    let width = 400;
    let height = 400;
    let sideLength = 100;
    let res = addNCompositionMatrixWidgets(matrixDisplay, 1, true, true, width, height, sideLength, [], shaderPath, meshesPath);
    let AInputs = res.MInputs[0];
  feedbackprocess: | 
    let mat = textToMatrix(AInputs, true, true); 
    solution = JSON.stringify(mat);
    let correct = glMatrix.mat4.fromValues(1, 0, 0, 0, 0, 3, 0, 0, 0, 0, 1, 0, 1, 2, -1, 1);
  correctcheck: |
    glMatrix.mat4.equals(correct, mat) 

---
