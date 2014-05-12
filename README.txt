This archive contains:
	1) silk
	2) silk.xml
	3) README.txt


Deployment steps for LWS 2.7.x (additional steps required for 2.6.x and earlier):

1)Copy the silk directory to $LWS_HOME/app/webapps/silk

2) Place "silk.xml" in $LWS_HOME/conf/jetty/lwe-ui/contexts/
  

You will now have a SiLK Icon on your LucidWorks Start Page, and clicking on it should take you to a dashboard (which may or may not connect to a live Solr server depending on your settings).

At present, Saving Dashboards to Solr does not work on LWS. Using a proxy is one way to make this work. It also works on Safari.

To save dashboards:

1) Click on Save Icon at the top and Export to File. Save it as a .json file on your desktop, giving it some meaningful name

2) To load the dashboard from your filesystem, click the Load icon at the top and Browse to previously saved dashboard layout

3) To load from the webserver, save the JSON file to $LWS_HOME/app/webapps/silk/app/dashboards/.

4) The dashboard is then accessible as http://localhost:8989/silk/#/dashboard/file/<filename>.json

5) Copy one of your your newly created dashboards into $LWS_HOME/app/webapps/silk/app/dashaboards/default.json (after backing up the existing one). This will load up when you click on the SILK icon.

REMEMBER TO FREQUENTLY SAVE DASHBOARDS THAT YOU ARE WORKING ON TO YOUR LOCAL FILESYSTEM. IF YOU HIT REFRESH, YOU COULD LOSE YOUR WORK.