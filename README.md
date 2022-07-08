Mule Microsoft Dot Net Connector Demo
========================================

Introduction
------------
Mule Studio demo for showing how to take advantage of DataSense and execute methods from a .net project.

The project contains a DotNet dll in the resources folder which has different classes with different methods.
There are also 6 flows that show how to use operations exposed by the dll.


## Prerequisites

* Java 8
* Anypoint Studio 7.x.x
* Mule Runtime 4.0.x EE
* DataWeave

Installation and Usage
----------------------

Import the demo project into your workspace.

Run the project in Studio.

Send the payload for the request you want to execute and verify the result. The requests are as follows:

1. http://localhost:8081/sumOfDigits - Computes the sum of the digits of the given number

For the following payload the operation will return 12.
{
	"num": 345
}

2. http://localhost:8081/reverseNumber - reverses the given number

For this payload 563 will be returned.
{
	"num": 365
}

3. http://localhost:8081/formatDate - formats the given input date using the given format

For the payload below the formatted date will be 2013-06-24.
{
	"date": "6/24/2013 12:00:00 AM",
	"format": "yyyy-MM-dd"
}

4. http://localhost:8081/startsWithUpper - checks if the given string starts with an upper case character

For the next request body the result will be true
{
	"str": "Test"
}

5. http://localhost:8081/substring - returns a substring form the given string

For the payload below the returned string will be demo
{
	"str": "My demo string",
	"start": 3,
	"length": 4
}

6. http://localhost:8081/personToString - returns the string representation of the five person

The string representation for the person below will be "Demo 26"
{
	"name": "Demo",
	"age": 26
}