#Midjourney_api 非官方的Midjourney API

##这是一个定制的Midjourney API，您可以使用它通过代码生成图像。使用Discord API进行工作。

###!!请记住，Midjourney的服务条款不允许任何自动化操作，所以这个项目仅限于研究目的！！

#包含内容：

##Sender：用于向Midjourney发送提示信息 Receiver：在终端中工作，将所有已完成的图像下载到本地文件夹 安装：

###创建Discord帐户并创建您的服务器（指南在这里：https://discord.com/blog/starting-your-first-discord-server） 创建Midjourney账户并将Midjourney Bot邀请到您的服务器（指南在这里：https://docs.midjourney.com/docs/invite-the-bot） 确保生成在您的服务器上正常工作 在Chrome浏览器中登录Discord，在您的服务器文本频道中，点击右上角的三个点，然后选择更多工具，再选择开发者工具。选择Network选项卡，您将看到页面的所有网络活动。 现在在您的文本频道中键入任何提示信息，按回车键发送带有提示信息的消息后，您将在网络活动中看到一个名为“interaction”的新行。点击它，选择Payload选项卡，您将看到payload_json - 这就是我们需要的！复制channelid、application_id、guild_id、session_id、version和id的值，稍后我们将需要它们。然后从Payload选项卡切换到Headers选项卡，找到“authorization”字段，也将其值复制。 克隆此存储库 打开“sender_params.json”文件，并将第5段中的所有值放入其中。还填写'flags'字段以指定提示信息的特殊标志 现在，您准备运行文件了： 要启动接收器脚本，请打开终端并输入：python /path/to/cloned/dir/receiver.py --params /path/to/cloned/dir/sender_params.json --local_path '/path/to/folder/for/downloading/images' 此脚本将显示所有的生成过程，并在准备好后立即下载图像 要发送提示信息进行生成，请打开另一个终端并输入：python //path/to/cloned/dir/sender.py --params /path/to/cloned/dir/sender_params.json --prompt 'your prompt here' 尽情享受吧 :) 请注意，控制并行请求的数量 - 正常和最快工作的数量不应超过3（在基础和标准计划中是3，在专业计划中是12）。

#项目说明：

##这是第一个简单版本的API，现在我正在开发下一个版本，其中包括：

##本地队列控制器 能够与任意数量的Midjourney账户同时使用，以获得更好和可扩展的性能 升采样脚本以发送升采样请求 以及其他很多功能 联系方式：








































# Midjourney_api
unofficial Midjourney API

This is custom Midjourney API. Using it you could generate images by code. Working on Discord API.

!! Don't forget Modjourney TOS doesn't allow any automation, so this project is research only purpose !!

Contains: 
- Sender: for sending prompts to Midjourney
- Receiver: works in terminal, download all the completed images to local folder

Installation:
1. Create Discord account and create your server(instruction here: https://discord.com/blog/starting-your-first-discord-server)
2. Create Midjourney account and invite Midjourney Bot to your server (instruction here: https://docs.midjourney.com/docs/invite-the-bot)
3. Make sure generation works from your server
4. Log in to Discord in Chrome browser, open your server's text channel, click on three points upper right corner, then More Tools and then Developer Tools.
Select Network tab, you'll see all the network activity of your page.
5. Now type any prompt to generate in your text channel, and after you press Enter to send message with prompt, you'll see in Network Activity new line named "interaction".
Press on it and choose Payload tab and you'll see payload_json - that's what we need!
Copy channelid, application_id, guild_id, session_id, version and id values, we'll need it a little bit later.
Then move from Payload tab to Headers tab and find "authorization" field, copy it's value too.
6. Clone this repo
7. Open "sender_params.json" file and put all the values from paragraph 5 to it. Also fill in 'flags' field to specify special flags to your prompts
8. Now you are ready to run files:
- To start receiver script open terminal and type:
python /path/to/cloned/dir/receiver.py --params /path/to/cloned/dir/sender_params.json --local_path '/path/to/folder/for/downloading/images'
This script will show you all the generating progress and download images as soon as it will be ready
- To send prompts for generation open another terminal and type:
python //path/to/cloned/dir/sender.py --params /path/to/cloned/dir/sender_params.json --prompt 'your prompt here'
9. Enjoy :)

Take care of controling number of parralel requests - for normal and fastest work it should be not bigger than 3(in Basic and Standard plan, and 12 in Pro plan).


Project comments:

This is the first simple API version, now I'm working on next one with:
- local queue controller
- ability to work with any number of Midjourney accounts in parralel to get much better and scalable performance
- Upsampling script to send upsample request
- And lots of other things.


Contacts:

For proposals and cooperation:

email: normalabnormalai@gmail.com

Discord: georgeb#0907
