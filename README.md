# Jmeter Exercises

Collection of jmeter tests run against website and APIs.

### Getting Started

These tests are built and run on jmeter. jmeter can be installed [here](https://jmeter.apache.org/download_jmeter.cgi). Ensure you setup environment paths so 
that you can run tests from the command line after creating them using the GUI application. To run a test and store information from the command line follow the format:

jmeter -n -t your_script.jmx -l "location to store results" -e -o "output folder" 

For example:

jmeter -n -t "C:\Program Files\apache-jmeter-5.4.1\tests\GoogleLoadTest.jmx" -l "C:\Program Files\apache-jmeter-5.4.1\report\report1.csv" -e -o "C:\Program Files\apache-jmeter-5.4.1\report"

Tests are stored in the root of the repo with the .jmx exstension. If the test stores results, the results are stored in their corresponding results folder inside "Results".

### Exercises:

GoogleLoadTest: This is a simple HTTP request test pinging the google homepage. The results are saved in a html report.

TransactionAndLoop: This test features a transaction controller with a HTTP Request Default and three sub HTTP Requests, one looping, each requesting a different pokemon using
pokeapi API.

Assertion: This test uses assertion result listeners to confirm the returning information from the HTTP Request is correct. In this example we confirm that the request pokemon,
"1" is called "bulbasaur".

Ghibli: This test has graphs measuring reponse time of the HTTP Request collecting information from the ghibli API about a film. Data is also saved to a csv using the data writer
listener.

LoadSpikeStressTest: This test simulates 3 peformance tests you would run against a application. The Load test sees how the application performs with a certain number of requests,
the Spike test checks performance when there are sudden short bursts or spikes of requests. Finally the stress test gradually increases the request amount looking to see the breaking
point and application stability. The thread user count in this test in unlikley to break an application but serves as an example of the thread graph shape required in a stress test.
This result information is saved in a html report and a csv file.


## Built With

* Jmeter

## Authors

* **Vicente Conte Couto** [vicentecontecouto](https://github.com/ecoutoo)
