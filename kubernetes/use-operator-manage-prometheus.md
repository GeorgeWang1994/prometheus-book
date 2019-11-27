# 使用Opterator管理Prometheus

在本章前面的例子中，为了在Kubernetes能够方便的管理和部署Prometheus，我们使用ConfigMap了管理Prometheus配置文件。每次对Prometheus配置文件进行升级时，，我们需要手动移除已经运行的Pod实例，从而让Kubernetes可以使用最新的配置文件创建Prometheus。 而如果当应用实例的数量更多时，通过手动的方式部署和升级Prometheus过程繁琐并且效率低下。

为了能够自动化的处理这些复杂操作，CoreOS引入了Opterator。简单来说，Opterator就是通过扩展Kubernetes API，帮助用户部署，配置和管理复杂的有状态应用程序示例，通过软件定义的方式来管理运维操作。
