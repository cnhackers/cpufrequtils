sudo apt install cpufrequtils

解决办法：

在/etc/default/grub中加入 GRUB_CMDLINE_LINUX_DEFAULT=“intel_pstate=disable”

命令行输入：sudo update-grub2

重启：sudo reboot

再次查看cpufreq-info，可以看到有更多的governors： available cpufreq governors: conservative, ondemand, userspace, powersave, performance, schedutil
