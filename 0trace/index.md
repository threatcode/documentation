---
Title: 0trace
Homepage: https://lcamtuf.coredump.cx
Repository: https://gitlab.com/kalilinux/packages/0trace
Architectures: any
Version: 0.01-3kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: images/0trace-logo.svg
PackagesInfo: |
 ### 0trace
 
  The package is traceroute tool that can be run within an existing, open TCP
  connection, therefore bypassing some types of stateful packet filters with
  ease.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install 0trace`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * tcpdump
 {{< /spoiler >}}
 
 ##### 0trace.sh
 
 
 ```
 root@kali:~# 0trace.sh -h
 Usage: /usr/bin/0trace.sh iface target_ip [ target_port ]
 ```
 
 - - -
 
 ##### sendprobe
 
 
 ```
 root@kali:~# sendprobe -h
 Usage: sendprobe src_ip dst_ip sport dport seq ack
 ```
 
 - - -
 
 ##### usleep
 
 Suspend execution for microsecond intervals
 
 ```
 root@kali:~# man usleep
 usleep(3)                  Library Functions Manual                  usleep(3)
 
 NAME
        usleep - suspend execution for microsecond intervals
 
 LIBRARY
        Standard C library (libc, -lc)
 
 SYNOPSIS
        #include <unistd.h>
 
        int usleep(useconds_t usec);
 
    Feature Test Macro Requirements for glibc (see feature_test_macros(7)):
 
        usleep():
            Since glibc 2.12:
                (_XOPEN_SOURCE >= 500) && ! (_POSIX_C_SOURCE >= 200809L)
                    || /* glibc >= 2.19: */ _DEFAULT_SOURCE
                    || /* glibc <= 2.19: */ _BSD_SOURCE
            Before glibc 2.12:
                _BSD_SOURCE || _XOPEN_SOURCE >= 500
 
 DESCRIPTION
        The  usleep() function suspends execution of the calling thread for (at
        least) usec microseconds.  The sleep may be lengthened slightly by  any
        system  activity  or  by  the  time spent processing the call or by the
        granularity of system timers.
 
 RETURN VALUE
        The usleep() function returns 0 on success.  On error, -1 is  returned,
        with errno set to indicate the error.
 
 ERRORS
        EINTR  Interrupted by a signal; see signal(7).
 
        EINVAL usec  is  greater  than  or equal to 1000000.  (On systems where
               that is considered an error.)
 
 ATTRIBUTES
        For an explanation of the terms  used  in  this  section,  see  attrib-
        utes(7).
        +-------------------------------------------+---------------+---------+
        | Interface                                 | Attribute     | Value   |
        +-------------------------------------------+---------------+---------+
        | usleep()                                  | Thread safety | MT-Safe |
        +-------------------------------------------+---------------+---------+
 
 STANDARDS
        4.3BSD,  POSIX.1-2001.   POSIX.1-2001  declares this function obsolete;
        use nanosleep(2) instead.  POSIX.1-2008 removes  the  specification  of
        usleep().
 
        On  the original BSD implementation, and before glibc 2.2.2, the return
        type of this function is void.  The POSIX version returns int, and this
        is also the prototype used since glibc 2.2.2.
 
        Only the EINVAL error return is documented by SUSv2 and POSIX.1-2001.
 
 NOTES
        The interaction of this function with the SIGALRM signal, and with oth-
        er  timer  functions  such   as   alarm(2),   sleep(3),   nanosleep(2),
        setitimer(2),  timer_create(2),  timer_delete(2),  timer_getoverrun(2),
        timer_gettime(2), timer_settime(2), ualarm(3) is unspecified.
 
 SEE ALSO
        alarm(2),   getitimer(2),   nanosleep(2),   select(2),    setitimer(2),
        sleep(3), ualarm(3), useconds_t(3type), time(7)
 
 Linux man-pages 6.03              2023-02-05                         usleep(3)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
