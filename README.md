# pipeline-demo
CICD pipeline demo using Jenkins, an angular app, and protractor.  You must have NodeJS installed on your system for this demo to work.

# Demo shows the ability to run SC locally and test on local website on SL

## Starting the Application
To start the application locally simply run:
1) `npm install`
2) `node server.js`


Echo “Tunnel 0”
Cd <yourSCdir>; ./sc -u $SAUCE_USERNAME -k $SAUCE_ACCESS_KEY -i SC_shared_demo --shared-tunnel --no-remove-colliding-tunnels --se-port 7226 --pidfile /tmp/sc_client-Test_shared_demo_0.pid --logfile sc-Test_shared_demo_0.log --scproxy-port 29998

Echo “Tunnel 1”
cd  <yourSCdir>;  ./sc -u $SAUCE_USERNAME -k $SAUCE_ACCESS_KEY -i SC_shared_demo --shared-tunnel --no-remove-colliding-tunnels --se-port 7225 --pidfile /tmp/sc_client-Test_shared_demo_1.pid --logfile sc-Test_shared_demo_1.log --scproxy-port 29999


----sauceconnect localhost demo-----

in one window
cd <yourprojectdir>; node server.js

in another window
echo "Starting LocalPage Demo"; echo "Running Test"
cd <yourprojectdir>; npm run protractor


