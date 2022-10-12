# SSN CNC Tutorial - tutorial creds @paroot1337 and @tcpsyn

Thank you for your trust in SSN, you will not regret it.

Customer Information:
User: ``
license: ``
Compiled: ``
Version: ``

# Suggested specs and details

Operating System: `Ubuntu 20.04`
Ram: `1 Gb`
CPU: `1 core` @ `1 Ghz`
Storage: `3 Gb`

# How To Setup SSN CNC

SSN CNC uses a MySQL database so you need to setup a database.

*   Upload the "CNC" folder that you received in the "SSNCNC.zip" onto your server.

1. `sudo apt-get update -y && sudo apt-get upgrade -y`
2. `sudo apt-get install screen phpmyadmin mysql-server mysql-client -y`
	* On the first screen, click the enter key with the first option selected "apache2"
	* On the second screen, click the enter key with the first option selected "<Yes>"
	* On the third screen, input a 32 character varchar password ending in "!?" such as	"4guWEDLGS67PJhXm2sD7xQks7PF8PzuQ!"
3. `sudo mysql`

*   When setting up the database replace the variables. 

	Example variables:

	{DB_TABLE} -> SSNCNC
	{DB_USERNAME} -> cooluserlol
	{DB_PASSWORD} -> 32 character varchar password ending in "!?" such as "BcfNUYVgThVtwHVgVk96wPaYP6efQ9K8!?"

	Note: For "{DB_FILEPATH}", enter the path to where your "database.sql" is located.

	{DB_FILEPATH} -> /root/CNC/assets/database.sql
	
		CREATE DATABASE {DB_TABLE};
		CREATE USER '{DB_USERNAME}'@'localhost' IDENTIFIED BY '{DB_PASSWORD}';
		GRANT ALL PRIVILEGES ON * . * TO '{DB_USERNAME}'@'localhost';
		FLUSH PRIVILEGES;
		use {DB_TABLE};
		source {DB_FILEPATH}; 
		exit

		Filled Example:

			CREATE DATABASE datatable;
			CREATE USER 'niceusername'@'localhost' IDENTIFIED BY 	'4guWBDLGS67PJhXm2sD7xQks7PF8PzuQ!?';
			GRANT ALL PRIVILEGES ON * . * TO 'niceusername'@'localhost';
			FLUSH PRIVILEGES;
			use datatable;
			source /root/CNC/assets/database.sql; 
			exit

*  Navigate into the directory that the "assets" folder is in by using: `cd "your directory"`.

4. `chmod 777 *`

# How to run SSN CNC

5. `screen -S CNC ./SSN`

# How to screen SSN CNC

6. `screen -S CNC ./SSN`

# How to deattach from the screen

7. Press keys: `CTRL` + `A` + `D` to detach from screen.

# How to reattach back into the screen

8. `screen -r CNC`

# How to login to SSN CNC

1. Run or screen SSN CNC
2. Open KiTTY or PuTTY or Termius.
3. On the main page:
   1. Set the host field to your server IP.
   2. Set the port field to `9900`.
   3. Set the connection type to `SSH`.
   4. Click connect.
   5. Username: root & Password: changeme (CHANGE IT WHEN YOU LOG IN)

# If you still require assistance, please contact https://t.me/tcpsyn