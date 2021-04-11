# INDOOR LOCALIZATION AND NAVIGATION IN SMART BUILDINGS

# ABSTRACT 

Buildings like offices, schools, factories or hospitals all over the world are becoming larger, whether on the basis of area or number of floors. Due to this increase in size and number of inhabitants residing in these buildings, they by themselves contribute to form a microcosm. These microcosms are required to be monitored to provide a safe and smart living space. Through a network of wireless nodes connected together by IoT techniques, real-time monitoring of the location of these inhabitants in these microcosms would be possible. 

GPS lacks the ability to provide accurate indoor position information. Through the use of the multi-node sensor network and measuring the RSSI(Received Signal strength indicator) value of a wireless signal emitter like a smartphone or RF beacon, localization, and navigation services inside a building can be provided. Through indoor localizations, a plethora of intelligent services can be deployed like indoor navigation for new places, movement monitoring in homes to observe health routines, asset tracking in factory floors, intelligent space allotment in shopping centers based on footfall and many more.


# PROBLEM STATEMENT

Infrastructure in the modern world is expanding in size, footfall and intelligence. With trends like Industry 4.0 and Smart City development and population growth in urban cities. These large structures like office complexes, schools and shopping centers they by themselves become micro-environments. For intelligent use of space and management of crowd and convenience for the denizen services like indoor navigation and localization are required.


# OBJECTIVES OF THE PROJECT

The project aims to create a Multi-Node Network that can be scalable to be retrofitted into any architecture of the infrastructure that is actively aware of the registered user’s location to provide intelligent services like position information and navigation in places where GPS may not provide unsatisfactory results. 

# OPERATION METHODOLOGY

The multi-node RSSI scanners detect the registered user's smartphone in the vicinity and obtain the RSSI value from the transmitted WiFi signal. The RSSI values are indexes and timestamped and sent as a JSON data payload to AWS IoT Cloud service through MQTT protocol. 
MQTT or Message Query Transport Telemetry protocol is a lightweight protocol used for IoT applications as the data payload is small and does not require large data buffers and IoT applications desire a protocol which can provide low latency which MQTT protocol does. 

AWS IoT Cloud service aides in setting up a pipeline to store the data payload in a NoSQL database where we can further use the data to process in algorithms that provide us with location algorithm. The data is appropriately stored to separate table and columns according to the scanner node's floor and location. 
This data is then accessed by Serverless event-driven computation platform called AWS Lambda where the Localisation and code for VUI exists. Here we use a basic triangulation algorithm using three nodes at a time to find the location of the user. 

Our project uses a Voice User Interface(VUI) to enable users to interact with service to find their current location or navigate to another room. This VUI is powered by Amazon's Alexa where an application called My Locator is run to access location data to be relayed through Alexa.



# REFERENCES 

1. Cant, V. and Calveras, A. (2017). “with Channel Diversity , Weighted Trilateration and. 
2. Gaur, A., Scotney, B., Parr, G., and McClean, S. (2015). “Smart city architecture and its applications based on IoT.” Procedia Computer Science, 52(1), 1089–1094. 
3. Jrger, T., Höflinger, F., Gamm, G. U., and Reindl, L. M. “Wireless distance estimation with low-power standard components in wireless sensor nodes. 
4. Khullar, R. and Dong, Z. (2017). “Indoor Localization Framework with WiFi Finger printing. 
5. Liu, Y. and Wang, Y. (2012). “A Position System of Multi-APs Based on RSSI.” 1565– 1568. 
6. Mahajan, A. (2012). “Wi-Fi Localization using RSSI in Indoor Environment via a smartphone.” 1(2). 
7. Mazuelas, S., Bahillo, A., Lorenzo, R. M., Fernandez, P., Lago, F. A., Garcia, E., Blas, J., and Abril, E. J. (2009). “Robust Indoor Positioning Provided by Real-Time RSSI Values in Unmodified WLAN Networks.” (November). 
8. Ozyer, T. (2014). “IEEE 802 . 11 WLAN Based Real Time Indoor Positioning : Liter ature Survey and Experimental Investigations.” 34, 157–164. 
9. Palaskar, P., Palkar, R., and Tawari, M. (2014). “Wi-Fi Indoor Positioning System Based on RSSI Measurements from Wi-Fi Access Points ÃsA Tri-lateration Approach.” 5(4), ´ 1234–1238. 
10. Sadowski, S. and Member, S. (2018). “RSSI-Based Indoor Localization With the Inter net of Things.” IEEE Access, 6, 30149–30161. 
11. Shang, F., Su, W., Wang, Q., Gao, H., and Fu, Q. (2014). “A Location Estimation Algorithm Based on RSSI Vector Similarity Degree.” 2014. 
12. Tembekar, S. and Saxena, P. A. (2013). “Gathering Information from Wireless Sensor Network to Cloud and Accessing it Using Smart Phone Application.” 2(12), 2712–2718. 
13. Turgut, Z., Zeynep, G., Aydin, G., and Sertbas, A. (2016). “Indoor Localization Techniques for Smart Building Environment.” Procedia - Procedia Computer Science, 83(Ant), 1176–1181. 
14. Yang, J., Wang, Z., and Zhang, X. (2015). “An iBeacon-based Indoor Positioning Systems for Hospitals.” 9(7), 161–168. 
15. Zanella, a., Bui, N., Castellani, a., Vangelista, L., and Zorzi, M. (2014). “Internet of Things for Smart Cities.” IEEE Internet of Things Journal, 1(1), 22–32. 

