## Top 100 Linux Interview Questions and Answers - Solved:
`We have prepared a set of questions to help Freshers and Experienced Linux Admins in their preparations for Interview.  This list includes Google interview questions for Linux (Technical Solutions Specialist - Infrastructure), Amazon interview questions for Linux (Cloud Support Engineer - II) and other reputed firms as well.  Most of these are scenario based Linux interview questions for Experienced Linux Admins. You will find these questions very helpful in your Linux Admins interviews. Prepare well and All the very best.`
<br>

 All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

{!inpage-ads.md!}

---

	1. Explain the below error: 

		-------------------------------------------------------------------------------------------
		find: page allocation failure. order:5, mode:0x0
		Pid: 22938, comm: find Not tainted 2.6.32-279.el6.i686 #1
		Call Trace:
	 	[<c04f22bc>] ? __alloc_pages_nodemask+0x6bc/0x870
	 	[<c051f1bc>] ? cache_alloc_refill+0x2bc/0x510
	 	[<c083f035>] ? apic_timer_interrupt+0x31/0x38
	 	[<c051f552>] ? __kmalloc+0x142/0x180
	 	[<f7fdb1d6>] ? rpc_malloc+0x36/0x90 [sunrpc]
	 	[<f7fdb1d6>] ? rpc_malloc+0x36/0x90 [sunrpc]
	 	[<f7fdb2f0>] ? rpc_wait_bit_killable+0x0/0x80 [sunrpc] 
		-------------------------------------------------------------------------------------------

	   Hint =>
			Above error is kernel dump due to kmalloc buffer exhaustion. The system is out of memory and 
			cannot satisfy the allocation request at all. This is more likely to happen on swap-less systems
			that are unable to purge application pages to free up memory.
			The system may have sufficient free pages in total but not enough that are physically contiguous
			to satisfy the allocation request. This is referred to as memory fragmentation.

			- The phrase "page allocation failure" - this defines the error message that should be used in a 
			  KCS search.
			- The process name "find" - often page allocation failures are related to code that gets executed
			  by specific threads, try searching KCS with and without this term. If the allocation request was
			  performed by an interrupt service routine then the process name will be irrelevant.
			- The order of the allocation "order:5" and mode "mode:0x0" can often be the same for every instance
			  of a particular problem, try searching KCS with and without these terms.
			- The function requesting the memory allocation "rpc_malloc()" is likely to be the same for every 
			  instance of this particular problem so include that in the KCS search.
			- Do not search for the CPU number, the process id or function offsets since they will change and
			  may prevent finding a match.
	
		For more details https://access.redhat.com/articles/1360023

	2. What is order:5, mode:0x0 in above output.

	3. Difference between kernel panic due to Memory crunch and page allocation failure.

	4. Difference between VMalloc and KMalloc
	   Hint =>
			The kmalloc() & vmalloc() functions are a simple interface for obtaining kernel memory in byte-sized
			chunks.

			- The kmalloc() function guarantees that the pages are physically contiguous (and virtually contiguous).
			- The vmalloc() function works in a similar fashion to kmalloc(), except it allocates memory that is 
			  only virtually contiguous and not necessarily physically contiguous.

	5. How do you troubleshoot memory performance issue. Please explain the details.

	6. Which tools do you use to troubleshoot high Memory troubleshooting.

	7. What are zombie process and how to kill/reclaim them.

	8. What are system calls. 

	9. What is strace used for. 

	10. Difference between fork and exec in Linux.

	11. Explain the below error:
	
		-------------------------------------------------------------------------------------------
		 No filesystem could mount root, tried: 
		[    4.471120] Kernel panic - not syncing: VFS: Unable to mount root fs on unknown-block(0,0)
		-------------------------------------------------------------------------------------------
	
	12. Explain few examples of kernel panic. 

	13. How to blacklist a module.

	14. What are D-State processes and what causes these.

	15. If Disk is causing D-state processes, what you can check and can do to fix the issue.

	16. Explain blk_trace.

	17. If you are receiving "Connection reset by peer" when trying to connect a server, what can be root cause 
	    of this and how you can fix this.  

	18. How will you troubleshoot high load avg. Which tools will you use and why. Explain in details. 

	19. What can be reason of high load avg in kernel space i.e. %sy in top. 

	20. What is CPU affinity . How to check it. 

	21. How to check all cores stat in top. Hint: by pressing 1 or using mpstat

	22. What can be the reasons for server to stuck at boot prompt. and how to troubleshoot further ?

	23. What is backporting in Linux. Hint: its related to packages. 

	24. There are two systems and one is taking less booting time and other than taking more than booting time. 

	25. Please explain Linux booting processing? 

	26. How to check the loaded and unloaded modules 

	27. Please explain few types of kernel errors? 

	28. How to troubleshoot the system performance if any Linux system is facing slowness? 

	29. How to troubleshoot high memory usageissue on Linux system. 

	30. What is CPU load ? How to calculate the load average on the system? 

	31. What the Zombie and Orphan process? How to kill zombie process?

	32. What could be the impacts on the system if there are many zombie process are available? 

	33. What is affinity in Linux? 
		1. Binding a process with a CPU core.
		2.  # taskset < command > 

	34. What is paging and swapping in Linux? Please explain Page fault ? 

	35. What is difference between cache and buffer? 

	36. Explain the TOP, IOSTAT,VMSTAT,IOTOP commands. 

	37. Difference between RHEL6 and RHEL7 booting process. 

	38. Difference between systemd and initd 

	39. How to troubleshoot a issue where a client not able to access a server? 

	40. What are outputs when you execute the NATCAT (nc) command  and explain each ?
	    Hint =>
		- Connected 
		- Connection timeout 
		- Connection refused(if port / server is blocking by the firewall) 

-----

	41. What are the inodes and how will you free up them? 

	42. How can we check the packet flow in our system? 

	43. what is the steal value in top command? 	

	44. Explain what is NUMA. You may know this as "Node Interleaving”. Give an example
	    where NUMA is beneficial, and another where it's detrimental.
	    Hints =>
		a). NUMA: Non Uniform Memory Access (NUMA) is a design where the memory is split into
		    groups by CPU, making the memory access faster for each CPU to their memory group.
		b). Beneficial: Multiple processes with smaller memory footprints. Good for applications that fork
		     processes, like Apache.
		    Detrimental: Monolithic, memory-heavy, single processes. May be threaded, example MySQL, Redis,
		    Java-everything, Memcached.
		Follow-Up Q. - what if there's only a single physical proc.

	45. Customer complains that their CPUs aren't running as fast as they're rated. How would you Troubleshoot ?
	    Hints => 
		a). Could be heat damage - check /proc/cpuinfo for "cpu MHz".
		b). Could be the wrong CPUs installed, for that matter. Check the CPU specs in /proc/cpuinfo. OR dmidecode.
		c). Get 'em to tell you how to fix it (Change system profile to MaximumPerformance with omconfig, then reboot)

	46. Can we check System logs on Hardware layer from OS ?How ?
	    Hints =>
		a). Yes, in dmesg logs or kern.log
		b). By using respective Hardware CLI commands.
		c). Specific answers
			hpasmcli -s "show iml"  ==> For HP servers
			omreport system [alertlog | esmlog]   ==> For Dell Servers

	47. What can be done to improve the performance of an I/O-heavy system?
	    Hints =>
		a). Check RAID Level, if server using any.
		b). Partition aligned, i.e. starting a partition on sector 2048.
		c). Mount Options like: noatime - (covers norelatime/nodiratime) Can be enabled only via fstab.
		d). RAID Controller settings - read/write policy, e.g. write-through(good to ensure data has been changed on disk.
		    write-back(relys on cache, battery).
		e). nobarrier - depends on whether or not the PERC Controller is making use of a battery or not.
		f). Adjust the filesystem journaling method - the default mount option is in the middle, data=ordered. 
		    This indicates the data is written out to the filesystem before the metadata in the journal is updated. 
		    The filesystem can be mounted with data=writeback which allows data to be written to the journal and 
		    disk at the same time, with the risk of some data possibly being written to the disk after the metadata 
		    that cannot be recovered after a crash. Additionally, the journal can be placed on an external device 
		    with another mount option, allowing separation of the writes to increase throughput performance for 
		    each write operation.
		g). discard - For SSDs. Also called fs TRIM. Extends life and improves performance of SSD drives. 
		    TRIM enables the controller to cache the expected SSD write cycles to collapse them into a "do only once" 
		    mechanism to prevent burning out the SSD cells, which can only be written to once with voltage.
			Note: For LVM, set issue_discards=1 in lvm.conf.
			Note: On Dell, TRIM/discard is only available on RAID controllers >= PERC H710
		h). For SSD, you don't want controller caching for performance reasons. By default HPs turn caching off.
		    Dell: Cut-through IO (CTIO) is an IO accelerator for SSD arrays that boosts the throughput of devices
		    connected to the PERC Controller. It is enabled through disabling the write-back cache (enable writethrough
		    cache) and disabling Read Ahead.
		    HP: On servers with SSD drives, write caching appears to be disabled by default for performance reasons 
		    (there is no need for write caching on SSD drives which are fast enough). Writes to SSD drives will not 
		    be acknowledged until the data is actually written to disk:
		i). On HP, HP SSD Smart Path - this is enabled by default by the RAID creation process in the HP RAID controller
		    itself, and can be checked with the standard commands using hpssacli to view controller details and RAID
		    logical device details. The theory is this special method of SSD writing replaces traditional caching 
		    techniques with a special HP invented method for improving SSD performance and longevity.
		j). Disk IO Scheduler
			deadline (recommended for DBs)
			noop (recommended for VMs)


	48. Why would I choose to use RAID-5 instead of RAID-10? Or vice versa?
	    Hints => 
		RAID-5:
			Pro: Space efficiency - you only sacrifice 1x HDD to redundancy.
			Pro: Possible with a minimum of 3x drives, as opposed to RAID-10's minimum-4.
			Con: Slow writes. Note: Reads are still quick though, so you'd be fine on a read-heavy application.
			Con: If two drives fail, you lose everything.
		RAID-10:
			Pro: Great performance with both reads and writes. Good for write-heavy applications.
			Pro: Less risk of a catastrophic failure, since more than 1 drive can fail safely (Note: Depends which
			     drives).
			Con: Too much wastage of Space. Only 50% capacity is uasable.

	49. How snapshots work ? Can you please explain. In terms of VMWare or LVM(in case someone asks).
	    Hints => 
		As soon as you create a snapshot, LVM creates a pool of blocks. This pool also contains a full copy of the
		LVM metadata of the volume. When writes happen to the main volume such as updating an inode, the block being 
		overwritten is copied to this new pool and the new block is written to the main volume. This is the 'copy-on-write'.
		Because of this, the more data that gets changed between when a snapshot was taken and the current state of 
		the main volume, the more space will get consumed by that snapshot pool.
		When you mount the snapshot, the meta-data written when the snapshot was taken allows the mapping of snapshot 
		pool blocks over changed blocks in the volume (or higher level snapshot). This way when an access comes for a
		specific block, LVM knows which block access. As far as the filesystem on that volume is concerned, there are
		no snapshots.

	50. In which scenario we need to use vgcfgrestore and vgcfgbackup commands ? When /etc/lvm/archive contents are 
	    written (when does backup happen ?)
	    Hints =>
			a). To restore VG configuration.
			b). Backup is taken whenever we make change to LVM (create/remove LV/VG) and we can use it to restore 
		    	to the prior state.

	51. What is default signal sent by KILL command ?
	    Hint =>
			a). singnal 15 (SIGTERM) is sent by default if you do not specify the signal type. 

	52. What is deadlock ? How to identify if process is in deadlock in Linux/Unix ?
	    Hint =>
			Deadlock is a situation where a set of processes are blocked because each process is holding a resource
			and waiting for another resource acquired by some other process

	53. How to load kernel module. any commands ?
	    Hint => 
			We can use "modprobe" or "insmod" commands to load kernel module.	

	54. Difference between insmod and modprobe commands in Linux ?


	55. Different types of file systems?
	    Hint =>
			ext2, ext3, ext4, xfs, vfat etc.

	56. Difference between ext4 and xfs?

	57. When v create user which files are referred?

	58. Differnce between passwd and shadow file?
	    Hint => 
			/etc/passwd contains User's detail like home directory, shell etc.
			/etc/shadow conatains User's password hashes. 

	59. What are the contents in passwd file?
	    Hint =>
			root:x:0:0:root:/root:/bin/bash

		       •   login name
		       •   optional encrypted password
		       •   numerical user ID
		       •   numerical group ID
		       •   user name or comment field
		       •   user home directory
		       •   optional user command interpreter

	60. List all users who are not given passwd? with cmd
	    Hint =>
			cat /etc/shadow| awk -F ":" '$2 ~ /[a-z]/ {print $1}'
	
	61. How to check what processess are running on which port?
	    Hint =>
			Using "netstat" and "ss" command we can relate processes with port. 

	62. How to extend partition in lvm? and indepth questions in lvm ?
	    Hint => 
			1. First attach extra storage/disk to server. 
			2. Create a new partition on the disk using 'fdisk' or 'parted' command. 
			3. Create a new Physical Volume(PV) on that new partition. e.g. 'pvcreate /dev/sdb1'		
			4. Exetend existing Volume Group(VG) using new PV. e.g. 'vgextend vg_name /dev/sdb1'
			5. Now extend the LV. e.g . 'lvextend -l 100%FREE /dev/mapper/vg_name-lv_name'
			6. now execute 'resize2fs' or 'xfs_growfs'.

	63. What is tcpwrappers?
	    Hint =>
			tcpwrappers is a host based Network Access Control List, by which we can allow or deny 
			a host or subnetwork IP addresses, 

	64. On which port dns works?
	    Hint =>
			DNS works on port 53. 

---

##Questions from Github  
A lot more Questions from <a href="https://github.com/v-nightwolf/nightwolf-cotribution/blob/main/linux_questionairs.md" target="_blank">nightwolf-cotribution github repo </a>


  # General Questions:

     1. What did you learn yesterday/this week?

     2. Talk about your preferred development/administration environment. (OS, Editor, Browsers, Tools etc.)

     3. Tell me about the last major Linux project you finished.

     4. Tell me about the biggest mistake you've made in [some recent time period] and how you would do it differently today. What did you learn from this experience?

     5. Why we must choose you?

     6. What function does DNS play on a network?

     7. What is HTTP?

     8. What is an HTTP proxy and how does it work?

     9. Describe briefly how HTTPS works.

    10. What is SMTP? Give the basic scenario of how a mail message is delivered via SMTP.

    11. What is RAID? What is RAID0, RAID1, RAID5, RAID10?

    12. What is a level 0 backup? What is an incremental backup?

    13. Describe the general file system hierarchy of a Linux system.

    14. Which difference have between public and private SSH key?

        

        
  # Simple Linux Questions:      

    15. What is the name and the UID of the administrator user?

    16. How to list all files, including hidden ones, in a directory?

    17. What is the Unix/Linux command to remove a directory and its contents?

    18. Which command will show you free/used memory? Does free memory exist on Linux?

    19. How to search for the string "my konfu is the best" in files of a directory recursively?

    20. How to connect to a remote server or what is SSH?

    21. How to get all environment variables and how can you use them?

    22. I get "command not found" when I run ifconfig -a. What can be wrong?

    23. What happens if I type TAB-TAB?

    24. What command will show the available disk space on the Unix/Linux system?

    25. What commands do you know that can be used to check DNS records?

    26. What Unix/Linux commands will alter a files ownership, files permissions?

    27. What does chmod +x FILENAME do?

    28. What does the permission 0750 on a file mean?

    29. What does the permission 0750 on a directory mean?

    30. How to add a new system user without login permissions?

    31. How to add/remove a group from a user?

    32. What is a bash alias?

    33. How do you set the mail address of the root/a user?

    34. What does CTRL-c do?

    35. What does CTRL-d do?

    36. What does CTRL-z do?

    37. What is in /etc/services?

    38. How to redirect STDOUT and STDERR in bash? (> /dev/null 2>&1)

    39. What is the difference between UNIX and Linux.

    40. What is the difference between Telnet and SSH?

    41. Explain the three load averages and what do they indicate. What command can be used to view the load averages?

    42. Can you name a lower-case letter that is not a valid option for GNU ls?

    43. What is a Linux kernel module?

    44. Walk me through the steps in booting into single user mode to troubleshoot a problem.

    45. Walk me through the steps you'd take to troubleshoot a 404 error on a web application you administer.

    46. What is ICMP protocol? Why do you need to use?

        

  
  # Medium Linux Questions:      

    47. What do the following commands do and how would you use them?
		tee
		awk
		tr
		cut
		tac
		curl
		wget
		watch
		head
		tail
		less
		cat
		touch
		sar
		netstat
		tcpdump
		lsof

    48. What does an & after a command do?

    49. What does & disown after a command do?

    50. What is a packet filter and how does it work?

    51. What is Virtual Memory?

    52. What is swap and what is it used for?

    53. What is an A record, an NS record, a PTR record, a CNAME record, an MX record?

    54. Are there any other RRs and what are they used for?

    55. What is a Split-Horizon DNS?

    56. What is the sticky bit?

    57. What does the immutable bit do to a file?

    58. What is the difference between hardlinks and symlinks? What happens when you remove the source to a symlink/hardlink?

    59. What is an inode and what fields are stored in an inode?

    60. How to force/trigger a file system check on next reboot?

    61. What is SNMP and what is it used for?

    62. What is a runlevel and how to get the current runlevel?

    63. What is SSH port forwarding?

    64. What is the difference between local and remote port forwarding?

    65. What are the steps to add a user to a system without using useradd/adduser?

    66. What is MAJOR and MINOR numbers of special files?

    67. Describe the mknod command and when you'd use it.

    68. Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.

    69. Describe a scenario when deleting a file, but 'df' not showing the space being freed.

    70. Describe how 'ps' works.

    71. What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?

    72. Explain briefly each one of the process states.

    73. How to know which process listens on a specific port?

    74. What is a zombie process and what could be the cause of it?

    75. You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?

    76. Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.

    77. Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com.

    78. Can you have several HTTPS virtual hosts sharing the same IP?

    79. What is a wildcard certificate?

    80. Which Linux file types do you know?

    81. What is the difference between a process and a thread? And parent and child processes after a fork system call?

    82. What is the difference between exec and fork?

    83. What is "nohup" used for?

    84. What is the difference between these two commands?  myvar=hello & export myvar=hello

    85. How many NTP servers would you configure in your local ntp.conf?

    86. What does the column 'reach' mean in ntpq -p output?

    87. You need to upgrade kernel at 100-1000 servers, how you would do this?

    88. How can you get Host, Channel, ID, LUN of SCSI disk?

    89. How can you limit process memory usage?

    90. What is bash quick substitution/caret replace(^x^y)?

    91. Do you know of any alternative shells? If so, have you used any?

    92. What is a tarpipe (or, how would you go about copying everything, including hardlinks and special files, from one server to another)?

    93. How can you tell if the httpd package was already installed?

    94. How can you list the contents of a package?

    95. How can you determine which package is better: openssh-server-5.3p1-118.1.el6_8.x86_64 or openssh-server-6.6p1-1.el6.x86_64 ?

    96. Can you explain to me the difference between block based, and object based storage?



  # Hard Linux Questions:      

    97. What is a tunnel and how you can bypass a http proxy?

    98. What is the difference between IDS and IPS?

    99. What shortcuts do you use on a regular basis?

    100. What is the Linux Standard Base?

    101. What is an atomic operation?

    102. Your freshly configured http server is not running after a restart, what can you do?

    103. What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?

    104. I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?

    105. Did you ever create RPM's, DEB's or solaris pkg's?

    106. What does :(){ :|:& };: do on your system?

    107. How do you catch a Linux signal on a script?

    108. Can you catch a SIGKILL?

    109. What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?

    110. Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.

    111. What's a chroot jail?

    112. When trying to umount a directory it says it's busy, how to find out which PID holds the directory?

    113. What's LD_PRELOAD and when it's used?

    114. You ran a binary and nothing happened. How would you debug this?

    115. What are cgroups? Can you specify a scenario where you could use them?

    116. How can you remove/delete a file with file-name consisting of only non-printable/non-type-able characters?

    117. How can you increase or decrease the priority of a process in Linux?

        
 # Expert Linux Questions:

    118. A running process gets EAGAIN: Resource temporarily unavailable on reading a socket. How can you close this bad socket/file descriptor without killing the process?

    119. What do you control with swapiness?

    120. How do you change TCP stack buffers? How do you calculate it?

    121. What is Huge Tables? Why isn't it enabled by default? Why and when use it?

    122. What is LUKS? How to use it?


---
<br>
<br>
{!footer.md!}
