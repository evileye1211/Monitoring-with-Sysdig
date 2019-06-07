---

copyright:
  years:  2018, 2019
lastupdated: "2019-05-09"

keywords: Sysdig, IBM Cloud, monitoring,  predefined dashboards

subcollection: Sysdig

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}


# 预定义仪表板
{: #default_dashboards}
您可以选择以下任一预定义仪表板来监视基础架构：
{:shortdesc}


## 应用程序
{: #default_dashboards_applications}

下表列出的预定义仪表板可选择用于监视应用程序和基础架构组件：

|仪表板名称|描述|用途|
|-----------------------|------------------------------------------------------------------------|-------------------|
| `HTTP 概述`         |使用此仪表板可监视 Web 服务器的运行状况。它可显示服务器上的负载及其及时处理请求的能力。|使用“请求数”和`平均/最长请求时间`面板可测量服务器的总体繁忙程度。</br>查找 URL 之间的相关性，以找到增强性能的机会。</br>使用“状态码”度量值可监视 4xx 和 5xx 错误代码。|  
| `排名靠前的 HTTP 请求`  |使用此仪表板可监视向 Web 服务器请求次数最多的 URL。例如，请求总数、平均和最长请求处理时间，以及请求和响应中包含的流量。|   |
| `MongoDB`  |使用此仪表板可监视 MongoDB 服务的繁忙程度、需求最高的集合以及性能最低的集合。|查找可受益于查询和索引性能调整的集合。|
| `MySQL/PostgreSQL`  |使用此仪表板可监视 SQL 数据库事务的总体负载和性能状态。了解请求数以及处理请求的速度。|提高性能。例如，监视最慢查询的响应时间，并识别对查询或表上的索引所做的更改。|
| `MySQL/PostgreSQL 排名靠前的查询`  |使用此仪表板可监视请求次数最多的 SQL 查询。查看接收的查询数以及为查询发送和接收的流量。|查找最慢的查询、运行次数最多的查询以及流量高的查询。|
| `Nginx`  |使用此仪表板可监视主机资源、HTTP 连接数、最慢的 URL 以及主机响应代码。|通过监视以下度量值来识别负载均衡调整：写入连接数、读取连接数、等待连接数、按机器列出的 CPU 负载、网络字节活动和每秒请求数</br>查找可以通过查看“最慢的 URL”度量值进行优化的页面。</br>通过查看“响应代码”来查找问题。|
{: caption="表 1. 应用程序和基础架构组件预定义仪表板的列表" caption-side="top"} 


## 主机和容器仪表板
{: #default_dashboards_host_container}

下表列出的预定义仪表板可用于监视主机和容器中的资源利用率和系统活动：


|仪表板名称|描述|用途|
|-----------------------|------------------------------------------------------------------------|-------------------|
|`容器限制`|使用此仪表板可查看相对于分配给每个容器的主机资源的 CPU 和内存度量值。| |
|`文件系统`|使用此仪表板可查看安装在实例上的文件系统的目录安装点、文件系统设备以及容量和使用情况信息。</br>缺省情况下，未列出远程安装的文件系统。要查看这些文件系统的数据，请将 **remotefs.enabled = true** 条目添加到每个实例上的 */opt/draios/bin/dragent.properties* 文件。</br>选择组时，度量值是类似文件系统安装点的平均值。|查找哪些文件系统即将变满，哪些文件系统未得到充分利用。按 *fs.bytes.used* 排序。|
|`概述（按容器）`|使用此仪表板可查看在所选组或实例上运行的容器的资源使用情况统计信息，例如 CPU 百分比、内存使用百分比、网络字节总数和文件字节总数。</br>在此视图中使用具有*比较*功能的*时间旅行*功能可查看历史信息。根据数据，验证进程是在按预期运行、行为不正常还是需要更多资源。|了解哪些容器正在消耗大量资源。</br>使用此信息可确定是否应该将应用程序移至其他主机。|
|`概述（按容器映像）`|使用此仪表板可获取容器映像中所定义服务的大小、性能和限制的概述。| |
| `概述（按主机）` |使用此仪表板可查看主机的常规资源使用情况统计信息，例如 CPU 百分比、内存使用百分比以及网络字节总数。</br>您还可以使用此仪表板来监视一组实例。</br>在此视图中使用具有*比较*功能的*时间旅行*功能可查看历史信息。根据数据，验证进程是在按预期运行、行为不正常还是需要更多资源。|了解在一组具有类似作业功能的主机中，哪些主机未使用，哪些过度使用。| 
| `概述（按进程）` |使用此仪表板可查看主机上主要进程的常规资源使用情况统计信息，例如 CPU 百分比、内存使用百分比以及网络字节总数。</br>您还可以使用此仪表板来监视一组实例。</br>在此视图中使用具有*比较*功能的*时间旅行*功能可查看历史信息。根据数据，验证进程是在按预期运行、行为不正常还是需要更多资源。|了解哪些进程正在消耗大量资源。</br>使用此信息可确定是否应该将应用程序移至其他主机。|
| `Sysdig 代理程序摘要` |使用此仪表板可查看环境中部署的 Sysdig 代理程序数及其版本。|  | 
| `排名靠前的文件` |使用此仪表板可查看主要文件的列表。可以查看文件名、文件字节总数、文件 I/O 所用时间以及文件错误计数。|按大小排序时可查找排名靠前的磁盘使用者。</br>按 I/O 排序时查找最繁忙的文件。</br>通过监视*文件错误计数*列中的数据来识别潜在错误。|
| `排名靠前的进程` |使用此仪表板可查看在一个主机或一组主机中运行的主要进程的列表。可以查看进程名称、其路径和所有自变量。</br>使用过滤功能可限制列出的进程。|在多次衍生同一进程的环境中，查找哪些进程是主要消耗者。|
| `排名靠前的服务器进程` |使用此仪表板可查看识别为仅面向服务器的进程（httpd、java、ntpd 等）的资源使用情况. |查找服务器进程的资源使用情况。|
{: caption="表 2. 主机和容器预定义仪表板的列表" caption-side="top"} 

## 网络
{: #default_dashboards_network}

下表列出的预定义仪表板可选择用于监视网络连接和活动：

|仪表板名称|描述|用途|
|-----------------------|------------------------------------------------------------------------|-------------------|
| `连接表`     |使用此仪表板可查看实例和远程节点之间的连接。监视每个连接的流量。|查找在网络上使用最多网络流量的主要用量者。|
| `概述`              |使用此仪表板可按方向、应用程序、进程和主机来查看随时间变化的总网络利用率。|识别哪些资源对响应性能的影响最大。|
| `响应时间与资源使用情况` |使用此仪表板可查看相对于主机处理网络请求的响应时间，随时间变化的主机资源度量值。|  |
| `排名靠前的端口`             |使用此仪表板可查看每个端口的入局字节数、出局字节数和字节总数，还可显示每个端口号的连接数。|  |
{: caption="表 3. 网络预定义仪表板的列表" caption-side="top"} 



## 服务
{: #default_dashboards_service}


下表列出的预定义仪表板可用于监视服务的性能，即使这些服务部署在编排的容器中：

|仪表板名称|描述| 
|-----------------------|------------------------------------------------------------------------|
| `概述（按服务）`   |使用此仪表板可查看在同一容器映像中运行的服务的大小、性能和限制。| 
| `服务概述`      |使用此仪表板可查看单个服务的资源利用率和响应时间。| 
{: caption="表 4. 服务预定义仪表板的列表" caption-side="top"} 



## 拓扑
{: #default_dashboards_topology}

下表列出的预定义仪表板可用于监视应用程序层的逻辑依赖关系：

|仪表板名称|描述| 
|-----------------------|------------------------------------------------------------------------|
| `CPU 使用率`             |使用此仪表板可监视主机与基础架构中其他部分之间的交互。| 
|`网络流量`       |使用此仪表板可监视所选实例的本地进程与远程节点上进程之间的带宽使用情况。|
| `响应时间`        |使用此仪表板可监视所选主机上所有进程之间的通信和网络响应度量值。</br>响应计数和时间显示为平均值，精确到秒。|
{: caption="表 5. 拓扑预定义仪表板的列表" caption-side="top"} 

**注：**对于未安装 Sysdig 代理程序但检测到其通信的实例，上述任何仪表板都会显示虚线和灰色框。














