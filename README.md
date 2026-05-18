# HHU-service
现在来教大家如何使用已经安装在matiej服务器里面的momask插件

<img width="474" height="24" alt="image" src="https://github.com/user-attachments/assets/62654c5f-7efd-48df-baaa-552a1f520cbc" />

这是组件的主要位置，那么这时候我们需要在服务器终端进入该位置。

<img width="641" height="49" alt="image" src="https://github.com/user-attachments/assets/e4babfd9-380c-434b-8bc7-4789f9d3e5ab" />

进去之后，现在我们可以开始直接开始调用，但是在这之前，我们要先注意：学校平台使用 slurm 作业调度系统管理所有计算作业，该系统接受用户的作业请求，并将作业合理的分配到合适的节点上运行，因此所有用户均应通过作业调度系统提交计算作业，不可直接在登陆节点或其他任何节点上直接运行。这也就是说。我们要创建一个.slurm的文件夹，在里面放入工作的指令，而不是在终端里面直接输入（这一步相当于用一个作业本将要做的东西全部写在上面）。
右键点击空白处选择新建，然后选择新建文件。

<img width="600" height="662" alt="image" src="https://github.com/user-attachments/assets/879015e6-6a42-4422-aaae-79e5c6039015" />

给自己的.slurm文件夹起名，前缀起名可以自己设定后缀保证是.slurm就可以。

<img width="475" height="417" alt="image" src="https://github.com/user-attachments/assets/d2597560-0b31-4426-a4e1-b41d5512fd34" />

这是我在文件夹里面创建好的momask.slurm文件，接下来，我们右键点击用记事本打开这个文件，在里面把我们的指令（也就是作业）写在上面

<img width="1471" height="511" alt="image" src="https://github.com/user-attachments/assets/997b054d-0d55-461a-a0d6-ee5dcc3e31c1" />

这是我验证过能够直接在服务器运行组建的一个作业的标准格式，我接下来给大家一行一行解读分别是什么意思
ff

