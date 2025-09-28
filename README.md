# Decathlon Scoring System

A Java + Angular application for calculating and ranking decathlon results.
It implements the official IAAF scoring formulas for all ten events, allowing results to be read from CSV files, generated randomly, or entered via a Swing GUI.

The system computes each athlete’s event points, sums them into a total score, and outputs the final ranking.

---

## Features

* **CSV input** – Load athlete results from a file in the format:

```
Name;100m;LJ;SP;HJ;400m;110mH;DT;PV;JT;1500m
John Doe;10.2;790;18.75;217;46.00;13.70;57.50;478;81.00;3:40.2
```

* **IAAF Scoring** – Calculates event points using official tables.
* **Ranking** – Athletes are sorted by total score.
* **Swing GUI** – Quick calculator interface for verifying scores.
* **Random Data Generator** – Create synthetic athletes for testing.
* **Command-line execution** – Run the full application with a custom input file.

---

## Requirements

* Java 1.8+
* Maven 3+

---

## Quick Start

Run everything with the included script:

```bash
./run.sh
```

---

## Usage

### 1. Verify calculations with Swing GUI

```bash
mvn exec:java -Dexec.mainClass="calculator.gui.DecathlonFrame"
```

### 2. Clean, compile, and run tests

```bash
mvn clean; mvn compile; mvn test
```

### 3. Generate random participants

```bash
mvn exec:java -Dexec.mainClass="generator.FakeAthleteGenerator" -Dexec.args="100"
```

*(Replace `100` with the number of athletes you want.)*

### 4. Run the application with a custom CSV file

```bash
mvn exec:java -Dexec.mainClass="main.Application" -Dexec.args="</path/to/your/file>"
```

If no file is provided, a default input file is used.

---

## Screenshots

* ![Swing Calculator](https://raw.githubusercontent.com/FA810/DecathlonScoringSystem/blob/master/decathlon.png)
* ![Web UI Ranking View](https://raw.githubusercontent.com/FA810/DecathlonScoringSystem/blob/master/webUI_ranking.png)


---

## References

* [IAAF Decathlon Scoring Tables (PDF)](http://www.decathlon2000.com/upload/file/pdf/scoringtables.pdf)
* [Online Decathlon Calculator](http://www.decathlon2000.com/884/decathlon-points-calculator/)

---

## Author

Fabio Rizzello
📧 [fabio.rizzello@tiscali.it](mailto:fabio.rizzello@tiscali.it)
