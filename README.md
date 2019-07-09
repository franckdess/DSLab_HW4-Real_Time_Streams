# DSLab_HW4-Real_Time_Streams

For this homework, we were working with the real-time stream of the NS, the train company of the Netherlands. 
You can see an example webpage that uses this same stream to display the train information on a map:
https://spoorkaart.mwnn.nl/ . 

To help and avoid having too many connections to the NS streaming servers, we have setup a service that collects the streams and pushes them to our Kafka instance.

The related topics are:

  - `ndovloketnl-arrivals` : For each arrival of a train in a station, describe the previous and next station, time of arrival (planned and actual), track number,...

  - `ndovloketnl-departures`: For each departure of a train from a station, describe the previous and next station, time of departure (planned and actual), track number,...

  - `ndovloketnl-gps`: For each train, describe the current location, speed, bearing.

The events are serialized in json (actually converted from xml), with properties in their original language. Google translate could help understand all of them.
