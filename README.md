<html>
<head>
</head>
<body>
	<h1>Cheap Events ATL Mini-Project</h1>
	<p>A cloud-based data pipeline that fetches the latest event and cheapest events from Ticketmaster and SeatGeek APIs and delivers it straight to your inbox.</p>
	<h2>Overview</h2>
	<p>This repository contains code for an Airflow DAG that fetches data from two APIs (Ticketmaster and SeatGeek) and stores the data in a MySQL database. The DAG is scheduled to run once per day. It also includes a MySQL trigger that updates a cheap_events table whenever a new row is inserted or an existing row is updated in the main events table, ensuring that the cheap_events table always contains up-to-date data.</p>
	<h2>Requirements</h2>
	<p>To use this code, you will need:</p>
	<ul>
		<li>API keys for Ticketmaster and SeatGeek</li>
		<li>An Outlook email account for sending the CSV file</li>
		<li>An AWS RDS MySQL server to store the data</li>
		<li>Python 3.6 or higher</li>
		<li>The following Python packages (requirements.txt):</li>
	</ul>
	<h2>Installation</h2>
	<p>To set up the pipeline, follow these steps:</p>
	<ol>
		<li>Clone this repository to your local machine.</li>
		<li>Install the required Python packages using pip install -r requirements.txt.</li>
		<li>Set up the MySQL trigger on the events table using the following SQL query located here: </li>
		<li>Update the MySQL connection parameters (table, database, password, port) in the Python script to match your database configuration.</li>
		<li>Update the email addresses and API keys in the Python script to match your configuration.</li>
		<li>Install and configure Apache Airflow, and copy the DAG file to the DAGs folder.</li>
		<li>Start the Airflow webserver and scheduler using the airflow webserver and airflow scheduler commands, respectively.</li>
	</ol>
	<p>Once the pipeline is running, it will fetch data from the two APIs once per day and store it in the MySQL database. It will also send an email with a CSV file containing the data in the cheap_events table.</p>
</body>
</html>


