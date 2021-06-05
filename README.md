# selenium-grid-notes
Selenium Grid 

Download the Selenium Server from the SeleniumHQ
Open the command prompt and go into the server path 
“Cd path”

To Start the hub

=>=   java -jar selenium-server-standalone-2.46.0.jar -role hub
To Start the nodes
=>=  java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://localhost:4444/grid/register
Using grid to run tests
DesiredCapabilities capability = DesiredCapabilities.firefox();
WebDriver driver = new RemoteWebDriver(new URL("http://localhost:4444/wd/hub"), capability);
capability.setBrowserName();
capability.setPlatform();
capability.setVersion()
capability.setCapability(,);

Configuring the nodes for IE
java -jar selenium-server-standalone-2.46.0.jar -role webdriver -hub http://192.168.20.239:4444/grid/register -port 5559 -browser "browserName=internet explorer,version=10,maxinstances=1" -Dwebdriver.ie.driver=\IEDriverServer.exe
Configuring the nodes for Firefox
=>= java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://localhost:4444/grid/register  -browser browserName=firefox -port 5556
Configuring the nodes for IE & Firefox in Windows VM
=>= java -jar selenium-server-standalone-2.46.0.jar -role node -port 5556 -hub http://192.168.20.239:4444/grid/register - maxSession 10 -browser “browserName=internet explorer,version=10,Platform=WINDOWS” -browser browserName=firefox,platform=WINDOWS -browser browserName=chrome,Platform=LINUX

java -jar selenium-server-standalone-2.46.0.jar -role node -port 5556 -hub http://192.168.20.239:4444/grid/register  -browser browserName=internet explorer, version=10, platform=WINDOWS, maxinstances=1 -webdriver.ie.driver="C:\Users\IEUser\Downloads\IEDriverServer.exe"




Configuring the nodes for Safari
java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://localhost:4444/grid/register - maxSession 10 -browser browserName=safari ,Platform=WINDOWS -port 5557
Configuring the nodes for Chrome
=>= java -jar selenium-server-standalone-2.46.0.jar -role webdriver -hub http://localhost:4444/grid/register  -browser browserName=chrome,maxInstances=5 -port 5557
java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://localhost:4444/grid/register - maxSession 10 -browser browserName=safari ,Platform=WINDOWS -port 5556

java -Dwebdriver.chrome.driver=”users\documents\chromedriver” -jar selenium-server-standalone-2.46.0.jar -role node -hub http://localhost:4444/grid/register - maxSession 10 -browser “browserName=chrome ,Platform=WINDOWS” -port 5556

java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://192.168.20.239:4444/grid/register - maxSession 10 -browser browserName=internet explorer ,version=11 ,Platform=WINDOWS -port 5556

java -jar selenium-server-standalone-2.46.0.jar -role node -hub http://192.168.20.239:4444/grid/register - maxSession 10 -browser “browserName=internet explorer ,version=10 ,Platform=WINDOWS”
In a VM Chrome
java -jar selenium-server-standalone-2.46.0.jar -role webdriver -hub http://192.168.20.239:4444/grid/register -port 5558 -browser browserName="chrome",version=ANY,platform=WINDOWS,maxInstances=5 -Dwebdriver.chrome.driver=\chromedriver.exe
C:\Users\IEUser\Downloads\chromedriver.exe

IE

java -jar selenium-server-standalone-2.46.0.jar -role webdriver -hub http://192.168.20.239:4444/grid/register -port 5559 -browser "browserName=internet explorer,version=10,maxinstances=1" -Dwebdriver.ie.driver=\IEDriverServer.exe


java -jar selenium-server-standalone-2.39.0.jar -role node -hub http://10.0.2.2:4444/grid/register -browser "browserName=internet explorer,version=8,maxinstances=1" -Dwebdriver.ie.driver="D:\tools\IEDriverServer.exe"
