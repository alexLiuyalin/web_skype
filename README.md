Need to add: Add the data directory to the same level directory, because your login information is stored in this file (the path and directory name can
Feel free to change it, but it must correspond to the path written in the test file, line 16)
Needs to be changed: Who to contact needs to be changed, and the content to be sent needs to be changed.
Can be changed: waiting time

a: You can start directly after seeing the results.
b: To see the effect, in the terminal of this file, enter: go run . -rod="show,slow=1s,trace"
If you do not log in after starting the project, follow the steps below
1. Set the time on line 34 of the file to be longer (waiting time)
2. Start the test file and log in to the account on the pop-up web page
3. After logging in to your account, click on Terminal and press Ctrl+C to close the project
4. Change the time back and restart the test file
Note: The reason for this time: it takes response time to open the web page. You can also not set the time, because it depends on the effect. I have set it here.

需要增加：在同级目录增加data目录,因为你登录后的信息存放在这个文件内(路径和目录名可以
随意更改，但是要和测试文件中所写路径对应，第16行)
需要改动：联系谁要改，发送内容要改
可以改动：等待时间

a:看结果可以直接启动
b:看效果，在本文件的终端，输入：go run . -rod="show,slow=1s,trace"
启动项目后如没有登录，按以下步骤
1.将文件第34行时间设长(等待时间)
2.启动测试文件，在弹出的网页进行登录账号
3.登录账号后，点击终端，按Ctrl+C 关闭项目
4.改回时间，重新启动测试文件
注：该时间的原因：打开网页需要反应时间，你也可以不设时间，因为要看效果所有我这里设了
