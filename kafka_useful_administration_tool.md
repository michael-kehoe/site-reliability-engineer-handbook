# Kafka useful administration tool


## Kafka Tools

This repository is a collection of tools for working with Apache Kafka.
The Site Reliability team for Kafka at LinkedIn has built these over time in order to make managing Kafka a little bit easier. Our intention is to add to this repository as more tools are developed.
We welcome additions and modifications that make managing Kafka better for all!
https://github.com/linkedin/kafka-tools
```bash
$ kafka-assigner
usage: kafka-assigner [-h] -z ZOOKEEPER [-l] [-g] [-e] [-m MOVES]
                      [--sizer {ssh}] [-s] [-d DATADIR] [--skip-ple]
                      [--ple-size PLE_SIZE] [--ple-wait PLE_WAIT]
                      [--tools-path TOOLS_PATH]
                      {trim,elect,set-replication-factor,clone,remove,balance,reorder}
                      ...
```


## kafkat

Simplified command-line administration for Kafka brokers.
https://github.com/airbnb/kafkat
```bash
$ kafkat
kafkat 0.0.10: Simplified command-line administration for Kafka brokers
usage: kafkat [command] [options]

Here's a list of supported commands:

  brokers                                                             Print available brokers from Zookeeper.
  clean-indexes                                                       Delete untruncated Kafka log indexes from the filesystem.
  controller                                                          Print the current controller.
  elect-leaders [topic]                                               Begin election of the preferred leaders.
  partitions [topic]                                                  Print partitions by topic.
  partitions [topic] --under-replicated                               Print partitions by topic (only under-replicated).
  partitions [topic] --unavailable                                    Print partitions by topic (only unavailable).
  reassign [topic] [--brokers <ids>] [--replicas <n>]                 Begin reassignment of partitions.
  resign-rewrite <broker id>                                          Forcibly rewrite leaderships to exclude a broker.
  resign-rewrite <broker id> --force                                  Same as above but proceed if there are no available ISRs.
  set-replication-factor [topic] [--newrf <n>] [--brokers id[,id]]    Set the replication factor of
  shutdown <broker id>                                                Gracefully remove leaderships from a broker (requires JMX).
  topics                                                              Print all topics.
  drain <broker id> [--topic <t>] [--brokers <ids>]                   Reassign partitions from a specific broker to other brokers.
```

