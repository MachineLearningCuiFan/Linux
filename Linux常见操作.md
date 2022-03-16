### **Linux常见操作**

**1、ubantu挂载硬盘：**

```text
#首先查看当前电脑硬盘情况
sudo fdisk -l
```

```text
# 我们在 ~ 目录下创建一个 data 的目录，并将新分区挂载到这里
mkdir ~/data
sudo mount /dev/sdb1 ~/data
```

