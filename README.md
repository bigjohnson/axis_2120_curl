# axis_2120_curl
Some curl lines for power relay on/off and reset the camera

Reset:
curl -X POST -d "do_reboot=yes&servermanager_do=set_variables" -u "root:password" "http://192.168.2.228/this_server/ServerManager.srv"

Relay closed:
curl -X POST -d "do_relay=off&servermanager_do=set_variables" -u "root:password" "http://192.168.2.228/this_server/ServerManager.srv"

Relay open:
curl -X POST -d "do_relay=on&servermanager_do=set_variables" -u "root:password" "http://192.168.2.228/this_server/ServerManager.srv"

This is really counterintuitive but work in I test it with a multimeter...

And a bonus ffplay view command:
ffplay.exe -f mjpeg -i "http://192.168.2.228/axis-cgi/mjpg/video.cgi?camera=&resolution=704x576"

Obviously change ip, username and password!
