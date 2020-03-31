The aim of this project is to calculate several software metrices and to define correlation between them.

Professor: Jinqiu Yang
## Project Team
Niloofar Kaypour  - 40092034 

Farzad Shamrizi - 40084665

Shahryar Haghighifard - 40083869

Harraj Sandhu - 40081706

Hao Chen - 40083458

Yasaman Sarlati - 40054706

## We calculated following metrices.

1. **Statement Coverage:**
2. **Branch Coverage:** 
3. **Mutation Score:**
4. **Cyclomatic Complexity:** 
5. **Code Churn**
6. **Postrelease Defects**

## Selected Open-Source Systems

1. **Apache Commons CodeC** - [*project details*](http://commons.apache.org/proper/commons-codec/) , [*source-code*](https://github.com/apache/commons-codec)
2. **JFreeChart** - [*project details*](http://www.jfree.org/jfreechart/) , [*source-code*](https://github.com/jfree/jfreechart)
3. **Apache Commons Configuration** - [*project details*](https://commons.apache.org/proper/commons-configuration/) , [*source-code*](https://github.com/apache/commons-configuration) 
4. **Apache Commons Digester** - [*project details*](https://commons.apache.org/proper/commons-digester/) , [*source-code*](https://github.com/apache/commons-digester/tree/DIGESTER3_3_2) 
5. **Apache Commons JEXL** - [*project details*](https://commons.apache.org/proper/commons-jexl/) , [*source-code*](https://github.com/apache/commons-jexl) 

## Directory Structure                                 

    ├── Data                                   # Raw Data - CSV, HTML (All Metrics)
    ├── Unified Files for Mertics 1,2,3,4      # Unified Raw Data for each Project for Metric 1,2,3,4
    └── README.md
    
## Used tools for different metrices :
### Jacoco
Added Dependency Plugin in pom.xml as below

```
<plugin>
	<groupId>org.jacoco</groupId>
	<artifactId>jacoco-maven-plugin</artifactId>
	<version>${commons.jacoco.version}</version>
	<executions>
		<execution>
			<id>prepare-agent</id>
			<goals>
				<goal>prepare-agent</goal>
			</goals>
		</execution>
		<execution>
			<id>post-unit-test</id>
			<phase>test</phase>
			<goals>
				<goal>report</goal>
				</goals>
				<configuration>
					 <!--Sets the path to the file which contains the execution data.-->
					<dataFile>target/jacoco.exec</dataFile>
					 <!--Sets the output directory for the code coverage report.-->
					<outputDirectory>target/jacoco-ut</outputDirectory>
				</configuration>
		</execution>
	</executions>
</plugin>
```
### Mutation Score

### Cyclomatic Complexity

### Code Churn

### Postrelease Defects
