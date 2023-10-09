- Sub-systems need to exchange data
	- Central database
	- Each sub-system maintain its own database and interchange data by passing messages

## When to use
- Large amount of data needs to be shared

## Advantages
- Efficient way to share large amounts of data
	- Central data repository store and manage data
		- Allow efficient data sharing as all subsystems access data from a single source
		- Data updates immediately available for all users
		- Reduced data duplication and redundancy
- Sub-systems need not to be concerned with how data is produced
	- Data production is abstracted away from the subsystems
	- Sub-systems only interact with data through specific interfaces
	- Allow greater modularity and encapsulation in system architecture
- Centralised management
	- Allow management tasks to be handled more effectively, efficiently and consistently
		- Backup
		- Security
		- Access control
		- Maintain data quality
- Sharing model is published as the repository schema
	- Based on well defined schema
		- Specifies how data structured
		- Act as data contract
		- Documents data entities, relationships and supported operations
	- Provide clear and standardised way for sub-system to interact with data
		- Ensures consistency
		- Facilitates seamless data integration

## Disadvantages
- Sub-systems must agree on a repository data model
	- They must agree on a standardised data model that represents stored data structure and format to ensure interoperability and smooth process of data exchange between different components
- Data evolution is difficult and expensive
	- All modification to data must be carefully managed
		- To ensure current data remain compatible
		- To ensure affected sub-system can adapt to the change without problem
	- All changes to data models needs multiple update, extensive testing and coordination
- No scope specific management policies
	- Repository model enforce standardised approach, sub-systems cannot have unique requirements
- Difficult to distribute efficiently
	- Sub-systems will face increased latency and performance issue for geographically distributed systems with high data volume
