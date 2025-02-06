##  Project: Kafka Streams using Python on IntelliJ IDEA
1. Download and Installation :
a. Download Apache Kafka
b. Extracted the zip file
c. Download and Install Python SDK
d. Install the IntelliJ IDEA ultimate edition
e. Install the Python plugin in the setting. File → Setting → Plugin

2. Creating a Python Project
a. File → New → Project
b. The dialog box will appear, set the paths and virtual environment

3. Start the Zookeeper and Kafka servers
a. Start the Zookeeper server
  i. bin\windows\zookeeper-server-start.bat config\zookeeper.properties
b. For multiple brokers, make changes to the server.properties files in the config folder. Change the broker_id, log_files, and port(optional), and then start the kafka broker.
  i. bin\windows\kafka-server-start.bat config\server.properties
  ii. bin\windows\kafka-server-start.bat config\server1.properties
  iii. bin\windows\kafka-server-start.bat config\server1.properties

4. pip install confluent-kafka for creating the streams using Python and importing the confluent-kafka library

5. Create the Producer and topic file in the .venv directory
a. For Producer and topic creation, use the Python code instead of running it directly from the terminal

6. Run the consumer console for consuming the published events.

Errors and how It was resolve
1. The log_file created for the first kafka_server had no more space
a. Deleted the contents of the log_file which resulted in the deletion of the previously stored messages (data).
2. Set the project setting using File → Project Settings → SDKs →  +  → Add Python SDKs from disk
