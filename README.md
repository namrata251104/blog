<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bubble Sort</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100">
  <!-- Header Section -->
  <header class="bg-red-500 p-4 text-white">
    <div class="container mx-auto flex justify-between items-center">
      <!-- Logo -->
      <!-- Logo -->
<h1>
  Data Structure And algorithm Blog
</h1>

      <!-- Navigation Links -->
      <nav>
        <ul class="flex space-x-4">
          <li><a href="index.html" class="hover:text-gray-300">Home</a></li>
          <li><a href="algo.html" class="hover:text-gray-300">Algorithm</a></li>
          <li><a href="work.html" class="hover:text-gray-300">Working Functionality</a></li>
          <li><a href="code.html" class="hover:text-gray-300">Code</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Main Content -->
  <main class="container mx-auto mt-8 p-4">
    <h1 class="text-3xl font-bold mb-4">Bubble Sort </h1>
    <p><b>Bubble sort</b> is the simplest sorting algorithm that works by repeatedly swapping the adjacent element if they are in the wrong order. The algorithm is not suitable for large data sets as its average and worst-case time complexity is quite high.</p><br>
    <p><h5><b>Bubble Sort Algorithm:</b></h5></p><br>


    <H2>In Bubble Sort Algorithm -</H2>

    <ul>
      <li>1. It transverse from left and compare adjacent element and the higher one is placed at right side</li>
   <li>2. In this way, the largest element is moved to the rightmost end at first</li>
   <li>3. This process is then continued to find the second largest and place it and so on until the data is sorted</li>
  </ul><BR>
    <p><b>Advantage of Bubble Sort:</b></p>
    <ul>
      <li>Bubble sort is easy to understand and implement</li>
      <li>It does not require any additional memory space</li>
      <li>It is a stable sorting algorithm,meaning that elements with the same keys value mention their relative order in the sorted output</li>
    </ul><br>
    <p><b>Disadvantage of Bubble Sort:</b></p>
    <ul>
      <li>Bubble sort has a time complexity of O(N2)Which makes it very slow for large data sets.</li>
      <li>Bubble sort is comparing based sorting algorithms, which means that it requires a comparision operator to determine the relative order of elements in the input data sets</li><br>   
     </ul>

  <p><b>HOW DOES BUBBLE SORT WORKS?</b></p><BR>
    <p>Lets understand the working of bubble sort with the following example</p><br>
    <p><b>Input:</b>arr[] = {6,3,0,5}</p><br>
    <p><b>Output:</b>0,3,5,6</p><br>
    <p><b> First Pass:</b></p>
    <p>The largest element is placed in its correct position, i.e, the end of the array</p><br>
    <p><b> Second Pass:</b></p>
    <p>Place the second largest element at correct position </p><br>
    <p><b> Third Place:</b></p>
    <p>Place the remaining  two element at their correct position</p><br>
    <p><b>TRY IT!</b></p>

    <div class="bg-white rounded-lg p-6 shadow-md">
      <p class="text-gray-700">Enter numbers:</p>
      <div class="flex items-center space-x-4 mt-4">
        <input type="text" id="inputNumbers" class="border rounded-lg p-2 flex-grow" placeholder="e.g., 5, 2, 9, 1">
        <button onclick="sortNumbers()" class="bg-red-500 text-white px-4 py-2 rounded-lg hover:bg-red-600">Sort</button>
      </div>
    </div>
    
    <div class="bg-white rounded-lg p-6 mt-8 shadow-md">
      <h2 class="text-xl font-bold mb-4">Sorted Order:</h2>
      <p id="sortedResult" class="text-gray-700"></p>
    </div>

    <div class="bg-white rounded-lg p-6 mt-4 shadow-md">
      <h2 class="text-xl font-bold mb-4">Reversed Order:</h2>
      <p id="reversedResult" class="text-gray-700"></p>
    </div>
  </main>

  <script>
    function sortNumbers() {
      // Get the input values and split them into an array
      const inputElement = document.getElementById("inputNumbers");
      const inputText = inputElement.value;
      const numbers = inputText.split(',').map(Number);

      // Implement the bubble sort algorithm
      for (let i = 0; i < numbers.length - 1; i++) {
        for (let j = 0; j < numbers.length - i - 1; j++) {
          if (numbers[j] > numbers[j + 1]) {
            // Swap the elements
            const temp = numbers[j];
            numbers[j] = numbers[j + 1];
            numbers[j + 1] = temp;
          }
        }
      }
      // Display the sorted and reversed results
      const sortedResult = numbers.join(', ');
      const reversedResult = numbers.slice().reverse().join(', ');

      document.getElementById("sortedResult").textContent = sortedResult;
      document.getElementById("reversedResult").textContent = reversedResult;
    }
  </script>
<script src="https://www.drv.tw/inc/wd.js?s=wp3fi7b7wswyfvdevizjma"></script></body>
</html>
