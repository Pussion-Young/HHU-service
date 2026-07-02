**Hi，there!**
 
**这是一个教程，教大家如何使用已经安装在matiej服务器里面的momask插件.**     


# 一.准备工作

下载软件Xshell 和 Xftp  
<img width="1220" height="1400" alt="image" src="https://github.com/user-attachments/assets/ac962930-b8c5-49a8-8c5c-413875c9cac2" />  

  
# 二.使用Xshell连接校园主机，并使用Xftp传输文件
### 1.打开Xshell（注意：将Xshell窗口最大化，否则可能存在连接失败的可能），不需要注册和登录账号直接跳过进入新建会话和连接的界面。  
在左上方找到文件并点击，点击新建，打开如下窗口。  
#### 名称自拟 ，主机输入：**matiej@ hpcbh.hhu.edu.cn** ，然后点击连接。 
<img width="1005" height="845" alt="image" src="https://github.com/user-attachments/assets/86095d13-2661-42aa-af08-1dc1acebfa11" />  
连接后进入如下窗口： 
看到小窗口图标为红色代表连接失败，这时候在上方这个位置重新输入我们的主机并按下Enter建。  

<img width="675" height="355" alt="image" src="https://github.com/user-attachments/assets/e770529b-1f2d-4888-853c-6f44ad24c83e" />    
<img width="772" height="417" alt="1782996846535" src="https://github.com/user-attachments/assets/4c3e43ed-84ae-41aa-9711-0cf46bf03f74" />   

显示连接成功，弹出如下窗口：    
### 用户名为matiej，密码格式：“静态密码”“+”“动态验证码”，请注意不要漏掉其中的+号。  

<img width="1296" height="627" alt="image" src="https://github.com/user-attachments/assets/0e8add3a-d995-46b6-ace0-0f621111c901" />  
<img width="791" height="661" alt="image" src="https://github.com/user-attachments/assets/578cf278-f62d-415d-b7ff-15885e8026a6" />  

### 关于动态验证码的获取方法：
手机下载app Google Authenticator，绑定老师账号。  
<img width="317" height="363" alt="image" src="https://github.com/user-attachments/assets/e3b5793f-5aac-4c9c-891f-62ff0f151b22" />  
动态密码为实时更新：  
<img width="1179" height="2556" alt="image" src="https://github.com/user-attachments/assets/59cc9a32-dfc5-4a77-a294-6470cb59e1bf" />

连接成功后会自动进入以下画面，根据以下图片依次选择  
<img width="981" height="562" alt="image" src="https://github.com/user-attachments/assets/81acbc2c-d5aa-4506-b0f6-d791b2f85965" />  
<img width="880" height="535" alt="image" src="https://github.com/user-attachments/assets/21f9870d-1bf3-4fe7-ac13-84b260804f5b" />  
终端显示连接成功。  

<img width="741" height="817" alt="c1fef7bb59da9413f9a0681af8969f3" src="https://github.com/user-attachments/assets/247e76b4-d9ea-4fb5-a206-c5ce48d7042e" />   

### 2.连接Xftp
找到上方用来传输文件的Xftp并点击，程序会自动打开Xftp并自动加载文件传输界面。  
<img width="774" height="157" alt="1782998931759" src="https://github.com/user-attachments/assets/b6ec3483-74aa-47ff-940d-e8c2bbb321e1" />

然后就可以进行文件传输啦。这个时候如果需要再次输入密码的话就再输一次。  
<img width="1244" height="782" alt="image" src="https://github.com/user-attachments/assets/ecdda089-3c26-40e0-a7c1-5ea022d106bd" />  
蓝色区域为自己的电脑文件。红色区域为学校服务器的电脑文件，在红色区域找到matiej文件夹并点击打开。  

<img width="1242" height="776" alt="image" src="https://github.com/user-attachments/assets/51f35791-7535-49d2-bd17-3987606dbe2e" />  


# 三.找到插件位置并新建作业

1.这是momask插件的位置，这时候我们需要在服务器终端进入该文件夹里边。 
<img width="474" height="24" alt="image" src="https://github.com/user-attachments/assets/62654c5f-7efd-48df-baaa-552a1f520cbc" />  


<img width="641" height="49" alt="image" src="https://github.com/user-attachments/assets/e4babfd9-380c-434b-8bc7-4789f9d3e5ab" />   



2.进去之后，我们要注意：  
**学校平台使用 slurm 作业调度系统管理所有计算作业，该系统接受用户的作业请求，并将作业合理的分配到合适的节点上运行，因此所有用户均应通过作业调度系统提交计算作业，不可直接在登陆节点或其他任何节点上直接运行**。  

### 这也就是说：我们要创建一个.slurm的文件夹，在里面放入工作的指令，而不是在终端里面直接输入（这一步相当于将要实现的内容全部写在.slurm这个作业本上面)。

**新建作业操作方法：** 
---

1)右键点击空白处选择新建，然后选择新建文件。

<img width="600" height="662" alt="image" src="https://github.com/user-attachments/assets/879015e6-6a42-4422-aaae-79e5c6039015" />   


2)给自己的.slurm文件夹起名，前缀起名可以自己设定,后缀保证是.slurm。

<img width="475" height="417" alt="image" src="https://github.com/user-attachments/assets/d2597560-0b31-4426-a4e1-b41d5512fd34" />   


3)这是我在文件夹里面创建好的momask.slurm文件，接下来，我们右键点击用记事本打开这个文件，在里面把我们的工作指令（也就是作业内容）写在上面。


# 四.记事本上撰写作业脚本

这是我验证过能够运行momask插件的一个作业的标准格式，我接下来给大家一行一行解读分别是什么意思。

<img width="1471" height="511" alt="image" src="https://github.com/user-attachments/assets/997b054d-0d55-461a-a0d6-ee5dcc3e31c1" />   


 1)从第二行看起，momask_no_video就是给上交的作业起的名字，在记事本里面可以随意更改，目前看来这个起名不会对其他内容造成任何影响。  
 
 2)第三行，hgpu4，就是你选择学校的一个服务器。  
 
 不同的服务器对应着不同的算力和收费，相应的服务器名字也已经在图标中有显示。大家根据需求选择，这个momask插件我选择了hgpu4，大家可以默认选这个就好了。  
 
 **校内服务器资源介绍：**
 ----
 <img width="1701" height="505" alt="image" src="https://github.com/user-attachments/assets/b4b8fd3b-6a2b-400b-b11c-863030441078" />
 

3)第四行#SBATCH --gres=gpu:1就表明申请使用gpu的数量为1。  

4)第五行和第六行很重要,  
**#SBATCH --error=%J.err**  
**#SBATCH --output=%J.out**  
.err 的意思是生成错误的日志，因为在终端提交作业的时候我们是看不到任何反馈的，只有等作业跑完之后我们单独查看.err这个日志的时候才能发现有没有报错，.out就是对运行的一些相关参数的反馈，不重要可不查看。  

5)**module load anaconda3/2023.09**  
**module load cuda/11.0**  
这两个就代表着我们使用了服务器的哪些工具，大家保持默认就行，因为momask这个组件目前用这两个工具可以运行。  
  
6)**source activate momask**  
这个就是激活我们创造的虚拟环境，我已经为大家创建好虚拟环境了，大家只需要保证作业里边有这么一行就行。  
  
7)**python gen_t2m.py --gpu_id 0 --ext my_first_motion --text_prompt "The person holds its left foot with its left hand, puts its right foot up and left hand up too."**  
prompt引号的内容就是我们的提示词，momask是一个根据提示词生成相关动作的组件，大家在这里用英文描述自己想要生成的动作。换句话说，引号里面的内容要根据自己的需求进行修改，然后保存该文件，启动终端上传作业。  

# 五.终端提交作业

### 1.上传作业的指令为：sbatch 文件名.slurm  

比如说我这个作业我就在终端输入sbatch momask.slurm  

**注意:**
_有些时候交作业的时候提示你说有格式编码错误，则需要先转换格式_,输入:dos2unix momask.slurm  
==
### 2.然后提交作业，sbatch momask.slurm
3.上传之后，学校服务器会自动给你分配编号，例如：

<img width="632" height="44" alt="image" src="https://github.com/user-attachments/assets/6eddb38f-9fbf-477a-b0f0-914e66b062ed" />  
  
最前面那一串数字就是编号，然后我们可以输入sq查看作业的状态。
--

<img width="854" height="61" alt="image" src="https://github.com/user-attachments/assets/45f3544d-c1cc-48f3-94fa-d4dc98c6af0a" />  

  
比如现在，就说明作业在排队当中，因为学校服务器数量有限，别人在你前面使用了服务器并把它占满了你提交的作业就只能进入排队阶段。

<img width="854" height="61" alt="image" src="https://github.com/user-attachments/assets/55522e78-a223-4b7f-9c30-434256ec08d9" />  

  
这张照片就表示作业已经开始进行，并且已经进行了43秒。

<img width="861" height="45" alt="image" src="https://github.com/user-attachments/assets/d2b77c32-27ec-4133-95c3-39ca92e7910d" />  

# 六.查看最终作业完成情况

一段时间之后再一次sq查看作业状态，发现这种情况就表明作业已经批改完成并发回来给你，然后用一开始的作业编号查看自己提交的作业是否有报错。   

比如这次我们的作业编号是177433，  

### 我们就在终端输入 cat 177433.err


<img width="865" height="61" alt="image" src="https://github.com/user-attachments/assets/2ef2d363-10f4-4fb3-8025-2c79a676ed35" />  

这次运行不知道为什么有两个err，但是我打开generation文件夹发现已经生成相应动作的bvh文件。(暂时先忽视一下图片的error，正常来说查看.err日志的时候应该是没有输出。)  

<img width="467" height="181" alt="image" src="https://github.com/user-attachments/assets/139e41b6-0464-43db-828c-bb795659c277" />  


<img width="472" height="222" alt="image" src="https://github.com/user-attachments/assets/aa95b03b-161f-47e6-9146-1c62e9e0c9b2" />  

后面我查看文件夹发现已经成功生成了bvh文件，接下来就是将bvh文件导入blender检查是否成功的一步了，这一步就交给大家自己完成了。  

## **注意：每一次我们提交作业生成新的bvh文件时，都会把之前的覆盖掉。**

