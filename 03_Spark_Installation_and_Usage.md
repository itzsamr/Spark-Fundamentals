# **Spark Installation and Usage**

- **Platform Support**: Spark runs on **Windows** or **Unix-like systems**.
  
- **Master UI**: By default, the master UI is accessible on **port 8080**.

- **Programming Languages**: Spark jobs can be written in **Scala**, **Python**, or **Java**. Shells are available for **Scala** and **Python**.

- **Programming Compatibility**: Ensure a **compatible version** of the programming language is used when setting up Spark.

- **Spark's Core Language**: Spark is written in **Scala**, so it’s natural to use Scala for Spark applications. **Scala**, **Python**, and **Java** are covered in the course.

- **Java Support**: **Java 8** supports functional programming with **lambdas**, bridging the gap between Java and Scala. **Java 6 and 7** require additional work.

- **Scala Overview**: 
  - **Everything in Scala is an object**, including primitive types.
  - **Functions are objects**, and can be passed as arguments, stored as variables, and returned from other functions.

- **Anonymous Functions**: Common in Spark applications. Use them if the function is required only once, allowing concise function definitions.

- **Spark Shell**: A simple way to learn **Spark's API** and analyze data interactively.
  - **Scala Shell**: Execute `spark-shell`.
  - **Python Shell**: Execute `pyspark`.

- **RDD Creation**: Use the `textFile` method with the **SparkContext** (`sc`) to create an RDD from a text file in either shell.
