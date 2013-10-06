Security-Map
============

项目计划
------------

### 1.漏洞信息数据的搜集（9月-10月）
具体工作：整合漏洞扫描的工具，网络扫描工具，对IT基础设施进行扫描，通过扫描得到各个系统、各个设备的信息，信息包括软件的配置，系统的版本号，系统的名称，系统的漏洞、网络的拓扑、开放的端口、正在提供的服务等。

具体方法：初步方法，采用脚本的方式将工具的功能自动化。

阶段性的结果：漏洞工具自动化实现及报告

需要的工具：nessus，Nikto，OpenVAS，FreeWAF，snort

### 2.数据的管理（10月-11月）
具体工作：将漏洞信息整合引入可进行数据管理的数据库系统。由于需要处理的数据量较大，可采用列存储的数据库。
阶段性的结果：漏洞信息引入数据库的自动化及报告

需要的工具：hbase或mongodb.


### 3.数据挖掘（11月-1月）
具体工作：根据需求采用相应的工具对数据库中的漏洞信息数据进行处理。
需要的工具：

1）若需要对数据进行批处理，则采用mapreduce。（可对扫描的系统做新漏洞的预测，非实时）

2）若需要对数据进行实时处理，则采用storm。（可对扫描的系统做实时新漏洞的行为预测）

阶段性的结果：对漏洞信息的数据挖掘自动化结果级报告

### 4.渗透测试检验结果（1-2月）

具体工作：通过渗透测试的方法对预测出的漏洞进行验证。

工具：metasploit



