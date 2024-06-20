---
{"Created:":"2022-05-16","tags":["on/Science/ComputerScience","School"],"date created":"2022-05-16 Mon","edited":"2023-04-06 Thu","dg-publish":true,"permalink":"/cards/display-json-in-php/","dgPassFrontmatter":true}
---

# Display JSON in PHP

```
$url = 'http://www.omdbapi.com/?i=tt0076759&r=json&apikey=79672bfd'; // URL of API

$contents = file_get_contents($url); //Get data from URL

$json = json_decode($contents, true); //Converting JSON

echo $json["Title"] . '<br/>'; //Display Title

echo $json["Year"] . '<br/>'; //Display Year

echo $json["Runtime"] . '<br/>'; //Display Runtime

echo $json["Plot"] . '<br/>'; //Display Plot

  

echo "<img src='".$json["Poster"]."'>"; // Display Poster



echo '<pre>' . var_export($json, true) . '</pre>'; //Data Dump
```

- [[Cards/Application Programming Interface\|API]] URL **must** be [[Cards/Hyper Text Transfer Protocol\|Hyper Text Transfer Protocol]], not HTTPS

# Reference

- [[Cards/Application Programming Interface\|Application Programming Interface]]
- [[Cards/JavaScript Object Notation\|JavaScript Object Notation]] 