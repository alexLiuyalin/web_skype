
func main() {
	// Launcher (save login information) 启动器(保存登录信息)
	file, err := launcher.New().UserDataDir("./data").Launch()
	if err != nil {
		// return nil, err
		fmt.Println("file err: ",err)
	}
	// Connect to the browser and start controlling it 连接到浏览器并开始控制它
	err = rod.New().ControlURL(file).Connect()
	if err != nil {
		// return nil, err
		fmt.Println("浏览器 err: ",err)
	}

	page, err := rod.New().ControlURL(file).MustConnect().Page(proto.TargetCreateTarget{
		URL: strings.Join([]string{"https://web.skype.com/"}, "/")})
	if err != nil {
		// return nil, err
		fmt.Println("page err: ",err)
	}
	time.Sleep(time.Second * 8)
	// universal path 通用路径
	// element, err:=page.Element("body > div.app-container > div > div > div:nth-child(1) > div > div.css-1dbjc4n.r-13awgt0 > div > div > div:nth-child(1) > div ")
	e, err := page.Element(".css-1dbjc4n.r-13awgt0")
	if err != nil {
		// return nil, err
		fmt.Println("e err: ",err)
	}
	// chat 聊天
	group, err := e.Element(".scrollViewport.scrollViewportV")
	if err != nil {
		// return nil, err
		fmt.Println("group err: ",err)
	}
	// time.Sleep(time.Hour)
	// chat button 聊天按钮
	list, err := group.Elements(`[role="button"]`)
	if err != nil {
		fmt.Println("list err:  ", err)
	}
	// var t *rod.Element

	for _, v := range list {
		// Select contact 选择联系人
		t, err := v.Element(`[data-text-as-pseudo-element="t"]`)
		if err == nil {
			err = t.Click(proto.InputMouseButtonLeft, 1)
			if err != nil {
				// return nil, err
				fmt.Println("t click err: ",err)
			}
			break
		}
	}
	// Enter content 输入内容
	content, err := e.Element(`span`)
	if err != nil {
		// return nil, err
	}
	err = content.Input("aaa")
	if err != nil {
		// return nil, err
	}
	// send button 发送按钮
	b, err := e.Element(`[title="Send message"]`)
	if err != nil {
		// return nil, err
	}
	err = b.Click(proto.InputMouseButtonLeft, 1)
	if err != nil {
		// return nil, err
	}
  // end 结束
	fmt.Println("end")
	time.Sleep(time.Hour)
}
