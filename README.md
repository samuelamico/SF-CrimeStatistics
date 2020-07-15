# SF-CrimeStatistics


## Beginning the Project
This project requires creating topics, starting Zookeeper and Kafka servers, and your Kafka bootstrap server. You’ll need to choose a port number (e.g., 9092, 9093..) for your Kafka topic, and come up with a Kafka topic name and modify the zookeeper.properties and server.properties appropriately.

### Local Environment
* Install requirements using ./start.sh if you use conda for Python. If you use pip rather than conda, then use pip install -r requirements.txt.

* Use the commands below to start the Zookeeper and Kafka servers. You can find the bin and config folder in the Kafka binary that you have downloaded and unzipped.

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

You can start the bootstrap server using this Python command: python producer_server.py.
Workspace Environment
Modify the zookeeper.properties and producer.properties given to suit your topic and port number of your choice. Start up these servers in the terminal using the commands:
/usr/bin/zookeeper-server-start zookeeper.properties
/usr/bin/kafka-server-start producer.properties
You’ll need to open up two terminal tabs to execute each command.

Install requirements using the provided ./start.sh script. This needs to be done every time you re-open the workspace, or anytime after you've refreshed, or woken up, or reset data, or used the "Get New Content" button in this workspace.

In the terminal, to install other packages that you think are necessary to complete the project, use conda install <package_name>. You may need to reinstall these packages every time you re-open the workspace, or anytime after you've refreshed, or woken up, or reset data, or used the "Get New Content" button in this workspace.

Step 1
The first step is to build a simple Kafka server.
Complete the code for the server in producer_server.py and kafka_server.py.
Local Environment
To see if you correctly implemented the server, use the command bin/kafka-console-consumer.sh --bootstrap-server localhost:<your-port-number> --topic <your-topic-name> --from-beginning to see your output.
Workspace Environment
To start kafka-consumer-console, use the command /usr/bin/kafka-consumer-console.