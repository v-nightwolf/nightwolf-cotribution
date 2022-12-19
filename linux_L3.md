# Advanced Linux Interview Questions for Experienced Linux Admins - Solved
<br>
    We have prepared a set of questions to help Experienced Linux Admins in their preparations for Interview.
    This list includes Google interview questions for Infrastructure specialist position, Amazon's Cloud Support Engineer - II position and other reputed firm's interviews as well.   

  Most of these are scenario based Linux interview questions for Experienced Linux Admins.
    You will find these questions very helpful in your Linux Admins interviews. Prepare well and All the very best.
<br>

   All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.
 
---

 {!inpage-ads.md!}


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
 ---

         Hint =>
            Above error is kernel dump due to kmalloc buffer exhaustion. The system is out of memory and cannot 
            satisfy the allocation request at all. This is more likely to happen on swap-less systems that are 
            unable to purge application pages to free up memory.
            The system may have sufficient free pages in total but not enough that are physically contiguous to 
            satisfy the allocation request. This is referred to as memory fragmentation.

              - The phrase "page allocation failure" - this defines the error that should be used for error search.
              - The process name "find" - often page allocation failures are related to code that gets executed by
                specific threads, try searching KCS with and without this term. If the allocation request was
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
          What can be difference in both ? 

25. Please explain few types of kernel errors? 

26. How to troubleshoot the system performance if any Linux system is facing slowness? 

27. How to troubleshoot high memory usageissue on Linux system. 

28. What is CPU load ? How to calculate the load average on the system? 

29. What the Zombie and Orphan process? How to kill zombie process?

30. What could be the impacts on the system if there are many zombie process are available? 

31. What is affinity in Linux? 

                1. Binding a process with a CPU core.
                2.  # taskset < command > 

32. What is paging and swapping in Linux? Please explain Page fault ? 

33. What is difference between cache and buffer? 

34. Explain what is NUMA. You may know this as "Node Interleaving”. Give an example where NUMA is beneficial, and another where it's detrimental.

          Hints =>
             a). NUMA: Non Uniform Memory Access (NUMA) is a design where the memory is split into groups by CPU,
                 making the memory access faster for each CPU to their memory group.
             b). Beneficial: Multiple processes with smaller memory footprints. Good for applications that fork
                 processes, like Apache.
                 Detrimental: Monolithic, memory-heavy, single processes. May be threaded, example MySQL, Redis,
                 Java-everything, Memcached.

             Follow-Up Q. - what if there's only a single physical proc.

35. Customer complains that their CPUs aren't running as fast as they're rated. How would you Troubleshoot ?

          Hints => 
             a). Could be heat damage - check /proc/cpuinfo for "cpu MHz".
             b). Could be the wrong CPUs installed. Check the CPU specs in /proc/cpuinfo. OR dmidecode.
             c). Change system profile to MaximumPerformance with omconfig, then reboot.

36. Can we check System logs on Hardware layer from OS ?How ?

          Hints =>
             a). Yes, in dmesg logs or kern.log
             b). By using respective Hardware CLI commands.
             c). Specific answers
                      hpasmcli -s "show iml"  ==> For HP servers
                      omreport system [alertlog | esmlog]   ==> For Dell Servers

37. What can be done to improve the performance of an I/O-heavy system?

          Hints =>
             a). Check RAID Level, if server using any.
             b). Partition aligned, i.e. starting a partition on sector 2048.
             c). Mount Options like: noatime - (covers norelatime/nodiratime) Can be enabled only via fstab.
             d). RAID Controller settings - read/write policy, e.g. write-through(good to ensure data has been 
                 changed on disk. write-back(relys on cache, battery).
             e). nobarrier - depends on whether or not the PERC Controller is making use of a battery or not.
             f). Adjust the filesystem journaling method - the default mount option is in the middle, data=ordered. 
                 This indicates the data is written out to the filesystem before the metadata in the journal is
                 updated. The filesystem can be mounted with data=writeback which allows data to be written to
                 the journal and disk at the same time, with the risk of some data possibly being written to the
                 disk after the metadata that cannot be recovered after a crash. Additionally, the journal can be
                 placed on an external device with another mount option, allowing separation of the writes to 
                 increase throughput performance for each write operation.

             g). discard - For SSDs. Also called fs TRIM. Extends life and improves performance of SSD drives. 
                 TRIM enables the controller to cache the expected SSD write cycles to collapse them into a "do only
                 only" mechanism to prevent burning out the SSD cells, which can only be written to once with voltage.
                 Note: For LVM, set issue_discards=1 in lvm.conf.
                 Note: On Dell, TRIM/discard is only available on RAID controllers >= PERC H710

             h). For SSD, you do not want controller caching for performance reasons. By default HPs turn caching
                 off.

                 Dell: Cut-through IO (CTIO) is an IO accelerator for SSD arrays that boosts the throughput of 
                 devices connected to the PERC Controller. It is enabled through disabling the write-back cache 
                 (enable writethrough cache) and disabling Read Ahead.

                 HP: On servers with SSD drives, write caching appears to be disabled by default for performance 
                     reasons (there is no need for write caching on SSD drives which are fast enough). Writes to SSD
                     drives will not be acknowledged until the data is actually written to disk:

             i). On HP, HP SSD Smart Path - this is enabled by default by the RAID creation process in the HP RAID
                 controller itself, and can be checked with the standard commands using hpssacli to view controller
                 details and RAID logical device details. The theory is this special method of SSD writing replaces
                 traditional caching techniques with a special HP invented method for improving SSD performance and 
                 longevity.

             j). Disk IO Scheduler
                 deadline (recommended for DBs)
                 noop (recommended for VMs)


38. Why would I choose to use RAID-5 instead of RAID-10? Or vice versa?

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


39. How snapshots work ? Can you please explain. In terms of VMWare or LVM(in case someone asks).

          Hints => 
             As soon as you create a snapshot, LVM creates a pool of blocks. This pool also contains a full copy of
             the LVM metadata of the volume. When writes happen to the main volume such as updating an inode, the
             block being overwritten is copied to this new pool and the new block is written to the main volume. 
             This is the "copy-on-write". Because of this, the more data that gets changed between when a snapshot
             was taken and the current state of the main volume, the more space will get consumed by that snapshot
             pool. When you mount the snapshot, the meta-data written when the snapshot was taken allows the mapping 
             of snapshot pool blocks over changed blocks in the volume (or higher level snapshot). This way when an
             access comes for a specific block, LVM knows which block access. As far as the filesystem on that volume
             is concerned, there are no snapshots.

40. In which scenario we need to use vgcfgrestore and vgcfgbackup commands ? When /etc/lvm/archive contents are written (when does backup happen ?)

          Hints =>
             a). To restore VG configuration.
             b). Backup is taken whenever we make change to LVM (create/remove LV/VG) and we can use it to restore to
                 the prior state.

41. What is default signal sent by KILL command ?

          Hint =>
             a). singnal 15 (SIGTERM) is sent by default if you do not specify the signal type. 

42. What is deadlock ? How to identify if process is in deadlock in Linux/Unix ?

          Hint =>
             Deadlock is a situation where a set of processes are blocked because each process is holding a resource
             and waiting for another resource acquired by some other process


43. Difference between insmod and modprobe commands in Linux ?

44. Difference between ext4 and xfs?

45. When we create user which files are referred?

46. What is the difference between a process and a thread? And parent and child processes after a fork system call?

47. What is the difference between exec and fork?

48. How can you limit process memory usage?

49. What is a tunnel and how you can bypass a http proxy?

50. What is the difference between IDS and IPS?

51. What shortcuts do you use on a regular basis?

52. What is the Linux Standard Base?

53. What is an atomic operation?

54. Your freshly configured http server is not running after a restart, what can you do?

55. What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?

56. I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?

57. Did you ever create RPM's, DEB's or solaris pkg's?

58. What does :(){ :|:& };: do on your system?

          Hint =>
              :(){ :|:& };: is shell fork bomb, If executed on a server, it will consume all the available resources
              on your system and eventually crash the system. Elaborated explaination is below:

              :() { :|:& }; :
               |    |       |-- Calling the funcation ":"
               |    |
               |    |-- Definition of function ":" in which funcation ":" is called and its output is passed to same
               |      funcation and process goes in backgrouond.
               |
               |-- Decalaring the funcation with name ":"

59. How do you catch a Linux signal on a script?

60. Can you catch a SIGKILL?

61. What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?

62. Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.

63. What's a chroot jail?

64. When trying to umount a directory it says it's busy, how to find out which PID holds the directory?

65. What's LD_PRELOAD and when it's used?

66. You ran a binary and nothing happened. How would you debug this?

67. What are cgroups? Can you specify a scenario where you could use them?

68. How can you remove/delete a file with file-name consisting of only non-printable/non-type-able characters?

69. How can you increase or decrease the priority of a process in Linux?

        
70. A running process gets EAGAIN: Resource temporarily unavailable on reading a socket. How can you close this bad socket/file descriptor without killing the process?

71. What do you control with swapiness?

72. How do you change TCP stack buffers? How do you calculate it?

73. What is Huge Tables? Why isn't it enabled by default? Why and when use it?

74. What is LUKS? How to use it?

75. When we execute below command, which binary is used ?

          [ -f test ] && echo "Found the file" || echo "create new file"

{!horizontal-ads.md!}

---
[<h1 style="text-align: center;font-family: cursive;"> Next Page </h1>](network.md)

---
<br>
{!footer.md!}
