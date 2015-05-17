Group Messenger 1
=======

This project builds on the Simple Messenger. Group Messenger 1 is an Android app that can send (multicast) a message to multiple AVDs (devices) and store them in a permanent key-value storage.

Some of the app features are:

1. Multicast user-entered message to app instances on all AVDs (devices), including the sender.

2. Send/Receive messages multiple times.

3. Handle concurrent messages.

The app assigns a sequence number (starting from 0 and incrementing by 1 for each message) to each message it receives.
Each message and its sequence number are stored as a <key, value> pair in a SQLite database (key: sequence number, value: message).
If a new value is inserted using an existing key, then only the most recent value is stored. The history of values under the same key is not preserved.