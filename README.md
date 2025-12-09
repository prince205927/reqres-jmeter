
# ReqRes JMeter Project

A Maven-driven **API Testing Framework** using **Apache JMeter**, **Groovy**, and **Selenium WebDriver** (headless Chrome).  
This project automates API testing for ReqRes endpoints, supports **data-driven testing via CSV**, and dynamically injects an **API key** fetched from a dashboard using Selenium.


## 🔧 Tech Stack

- **Java:** 11  
- **Build Tool:** Maven (`jmeter-maven-plugin`)  
- **API Testing:** Apache JMeter  
- **Scripting:** Groovy (JSR223 PreProcessors & Assertions)  
- **Browser Automation:** Selenium WebDriver (Chrome headless)  

## ⚙️ Setup

### Prerequisites
- **Java 11** (`java -version`)
- **Maven 3.9+** (`mvn -v`)
- **Google Chrome** installed

### Installation 
```bash
# Clone repository
git clone <repo-url>
cd reqres-jmeter-project
```
### Running the tests
```bash
mvn clean verify
mvn clean verify -Djmx.includes=reqres.jmx
mvn clean verify -Djmx.includes=data_driven.jmx
```

The project supports data-driven testing using a CSV file located at:
```bash
src/test/resources/reqres_test_cases_detailed.csv
```

### 📊 Output Files
After mvn clean verify, outputs are under target/jmeter/:
```
target/jmeter/
├─ testFiles/          # JMX test plan(s)
├─ results/            # Raw CSV/JSON results
├─ logs/               # JMeter run logs
├─ reports/            # HTML reports 

```



