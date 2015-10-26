
If the application server is deployed at 9090 port the we will construct our url "http://localhost:9090/". Change the port as per your deployment port.


1.) GET Request with http://localhost:9090/service will return the output in text format like 
	status :Server is running 
	time : Wed Oct 24 15:55:31 IST 2012

2.) GET Request with http://localhost:9090/service/json will return the object EmployeeModel in Json format like
	{
		name: "randomb808",
		age: 90
	}
	We are generating the random name and age in the service.

3.) GET Request with http://localhost:9090/service/xml will return the object EmployeeModel in XML format like

	<Employee>
		<name>random2874</name>
		<age>44</age>
	</Employee>
	
	We are generating the random name and age in the service.

4.) POST EmployeeModel object to Service using URL http://localhost:9090/service/json/object
    We have used Postman Rest client to send the JSON request to service
	The response will be send back as XML format, in step 3. This is example of consuming JSON as Object.

5.) POST Request to send String parameter to Service using http://localhost:9090/service/json/anyString
    The service will send the response like 
	Jersey Says :anyString

	