- A distributed system model that shows how data and processing is distributed across a range of components
	- Data centralisation on server side to ensure data consistency
	- Clients directly make request to certain service and requests are processed directly and returns relevant data to the client
- Consists of
	- Set of stand-alone servers that provides specific services like printing, data management etc.
	- Sets of clients which calls on these services
	- Network which allows clients to access the servers
 
## Advantages
- Distribution of data is straighforward
- Makes use of the network system and requires cheaper hardware
	- Handles task effectively via utilising the network
	- High load able to be handled concurrently
		- Client and server communicate over the network
		- Tasks are distributed to different servers
		- Processing load is distributed
- Easy to expand, by adding a new server or upgrading existing ones
	- Flexible and scalable
	- Allow system to grow without issues

## Disadvantages
- No shared data model -> sub-systems use different data organisation -> data interchange may be inefficient
	- Normally every server maintain their own data storage and organisation
	- Different server may use different data models or formats to store and manage data
	- Inefficient if want to translate between formats
- Redundant management in each server
	- There exists redundant tasks across multiple servers as they operate independently
		- Security
		- Backup
		- Access controls
	- Increases administrative overhead and complexity (especially for large systems)
- No central register of names and services
	- Hard to find out what servers and services are available
	- Without central register, clients have to use external methods or rely on broadcasting / multicasting mechanism to discover services dynamically
		- Less efficient and may miss service if unaware
	- Can be solved by implementing service discovery protocols or centralised service repositories