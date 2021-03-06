# 9.1.2.公有云虚拟磁盘管理

云盘是阿里云为云服务器ECS提供的数据块级别的块存储产品，具有低时延、高性能、持久性、高可靠等特点。云盘采用分布式三副本机制，为ECS实例提供数据可靠性保证。支持在可用区内自动复制数据，防止意外硬件故障导致的数据不可用。

用户能够通过云平台纳管阿里云账号现有的虚拟磁盘资源，也可以对虚拟磁盘进行创建、挂载、卸载等操作。

在“资源管理”菜单下选择左侧”虚拟资源管理”的导航菜单，之后点击”虚拟磁盘”的子菜单，即可看到虚拟磁盘的管理界面：



虚拟磁盘可以为虚拟机提供存储功能，可分为“系统盘”和“数据盘”：

- 系统盘：虚拟机的系统磁盘，用于支撑虚拟机的系统运行；
- 数据盘：虚拟机使用的数据磁盘，用于拓展虚拟机的存储。

## 相关操作

HYPERX云管理平台支持用户对虚拟磁盘进行管理，支持的功能如下：

### 特色操作

- 全局搜索：用户可以根据虚拟磁盘的名称、?、？等字段全局搜索虚拟磁盘；
- 自定义表头：用户可以从“列选择器”中自定义虚拟磁盘管理界面列表显示的表头(如磁盘容量、磁盘类型、状态等)；
- 高级筛选：用户可以从表头右侧根据磁盘类型、状态、关联虚拟机等字段筛选出符合条件的虚拟磁盘；

### 磁盘操作

- 创建虚拟磁盘：在云平台中创建一块阿里云虚拟磁盘；
- 挂载虚拟磁盘：将选定的虚拟磁盘挂载到选定的虚拟机中；
- 卸载虚拟磁盘：将选定的虚拟磁盘从选定的虚拟机上卸载；
- 同步磁盘状态：将阿里云中虚拟磁盘的状态手动同步至云平台，支持批量操作；
- 虚拟磁盘扩容：为选定的虚拟磁盘执行扩容操作；
- 查看操作日志：查看选定虚拟磁盘的操作审计；
- 删除虚拟磁盘：将选定的虚拟磁盘从云平台中删除，支持批量操作；

### 磁盘快照操作

- 创建磁盘快照：为选定的虚拟磁盘创建快照；
- 回滚磁盘快照：将选定的快照文件回滚至虚拟磁盘；
- 同步快照状态：将阿里云中磁盘快照的状态手动同步至云平台；
- 删除磁盘快照：将选定的磁盘快照从云平台中删除。

### 操作审计

- 查看日志：支持查看选定虚拟磁盘的操作审计。

操作入口如下：

- 资源管理→虚拟资源管理→虚拟磁盘

## 操作说明

### 磁盘操作

#### 创建虚拟磁盘

① 在公有云虚拟磁盘管理界面中，点击“创建虚拟磁盘”按钮：



② 将会进入“创建虚拟磁盘”的页面，可以填写虚拟磁盘的所属组织、关联云账号、可用区等相关信息，填写相关信息后，点击“确定”按钮，即可创建虚拟磁盘：



> [!NOTE]
>
> - 虚拟磁盘的名称需要以字母开头、数字、字母大小写和"-"组合，长度在2-128字符以内；
> - 虚拟磁盘的类型和地域、可用区有关联性，不同地域支持的磁盘类型不同；
> - 创建磁盘时所选择的云账号余额需要超过100元，否则会创建出故障的磁盘。

#### 挂载虚拟磁盘

① 在公有云虚拟磁盘管理界面中，选择需要挂载到虚拟机的磁盘，点击操作列的“挂载”按钮：



② 将会弹出"挂载"的操作提示框，选择需要挂载的虚拟机后，点击“确定”按钮，即可将选定的虚拟磁盘挂载至虚拟机：



> [!NOTE]
>
> - 虚拟磁盘可挂载的虚拟机需要和虚拟磁盘在同一个可用区域；
> - 虚拟磁盘可挂载的虚拟机需要和虚拟磁盘在同一个组织下。

#### 卸载虚拟磁盘

① 在公有云虚拟磁盘管理界面中，选择需要从虚拟机上卸载的磁盘，点击操作列的“卸载”按钮：



② 将会弹出"卸载"的操作提示框，复核信息无误后，点击“确定”按钮，即可将虚拟磁盘从虚拟机上卸载：



> [!WARNING]
>
> - 由于虚拟机的系统磁盘用于安装操作系统，若卸载系统磁盘虚拟机将无法正常运行，所以平台不支持卸载系统磁盘；

#### 同步磁盘状态

① 在公有云虚拟磁盘管理界面中，选择需要从同步状态的磁盘，点击操作列的“同步状态”按钮，即可同步选定磁盘的状态信息：





> [!NOTE]
>
> - 从阿里云中对磁盘执行操作后，可能导致云平台的状态和阿里云的一致，可以通过此操作手动同步磁盘的状态信息。

#### 虚拟磁盘扩容

① 在公有云虚拟磁盘管理界面中，选择需要扩容的磁盘，点击操作列的“扩容”按钮：



② 将会弹出"扩容"的操作提示框，填写信息磁盘容量信息后，点击“确定”按钮，即可将虚拟磁盘扩容到指定容量：





> [!NOTE]
>
> - 为保障虚拟机运行的稳定性，目前云平台仅支持扩容操作，不支持缩容操作。

#### 查看操作日志

① 在公有云虚拟磁盘管理界面中，选择需要查看操作日志的磁盘，点击磁盘名称进入磁盘详情页：



② 在磁盘详情页中，点击"操作日志"选项卡，即可查看虚拟磁盘的操作审计信息：




#### 删除虚拟磁盘

① 在公有云虚拟磁盘管理界面中，选择需要查看删除的磁盘，点击操作列的“删除”按钮：



② 将会弹出“删除虚拟磁盘”的操作提示框，点击“确定”按钮，即可删除选定的虚拟磁盘：



> [!WARNING]
>
> - 仅支持删除未关联虚拟机的数据盘。

### 磁盘快照操作

#### 创建磁盘快照

① 在公有云虚拟磁盘管理界面中，选择需要从创建快照的磁盘，点击操作列的“创建快照”按钮：



② 将会弹出"新建快照"的操作提示框，填写快照名称信息后，点击“确定”按钮，即可为选定的磁盘创建快照：



> [!NOTE]
>
> - 磁盘快照的名称需要以字母开头、数字、字母大小写和"-"组合，长度在2-128字符以内。

#### 回滚磁盘快照

① 在公有云虚拟磁盘管理界面中，选择需要从回滚快照的磁盘，点击磁盘名称进入磁盘详情页：



② 在磁盘详情页中，点击"快照"选项卡，即可查看磁盘快照的列表：



③ 选择需要回滚的快照，点击操作列的“回滚磁盘”按钮：



④ 将会弹出"回滚硬盘"的操作提示框，复核信息无误后，点击“确定”按钮，即可将选定的磁盘快照回滚至磁盘：





> [!NOTE]
>
> - 回滚快照的磁盘如果关联虚拟机，所关联的虚拟机需要处于关机状态；
> - 如需回滚后自启虚拟机，请勾选"自动启动"按钮。

#### 同步快照状态

① 在公有云虚拟磁盘管理界面中，选择需要从同步快照状态的磁盘，点击磁盘名称进入磁盘详情页：



② 在磁盘详情页中，点击"快照"选项卡，即可查看磁盘快照的列表：



③ 选择需要同步状态的快照，点击操作列的“同步状态”按钮，即可同步选定磁盘快照的状态信息：



> [!NOTE]
>
> - 从阿里云中对磁盘快照执行操作后，可能导致云平台的状态和阿里云的一致，可以通过此操作手动同步磁盘快照的状态信息。

#### 删除磁盘快照

① 在公有云虚拟磁盘管理界面中，选择需要从删除快照的磁盘，点击磁盘名称进入磁盘详情页：



② 在磁盘详情页中，点击"快照"选项卡，即可查看磁盘快照的列表：



③ 选择需要删除的快照，点击操作列的“删除”按钮：



④ 将会弹出“删除”的操作提示框，点击“确定”按钮，即可删除选定的磁盘快照：



### 操作审计

#### 查看日志

① 在公有云虚拟磁盘管理界面中，选择需要查看日志的虚拟磁盘，点击虚拟磁盘名称进入虚拟机详情页面：



② 点击"操作日志"选项卡，进入操作日志的页面，即可查看选定虚拟磁盘的操作审计信息：

