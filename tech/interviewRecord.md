# IP 在第几层

第三层。

## IP 头有什么，尽量详细


# TCP 与 UDP 的区别


# Https 安全在哪儿



# Http 2.0 的内容


# NAT


# poll 与 epoll 的区别

https://www.cnblogs.com/aspirant/p/9166944.html

http://www.ulduzsoft.com/2014/01/select-poll-epoll-practical-difference-for-system-architects/

https://daniel.haxx.se/docs/poll-vs-select.html

https://stackoverflow.com/questions/4039832/select-vs-poll-vs-epoll

# 数组访问为什么更快

相比链表，数组在内存中是成块得存储，而链表是块式存储。应为空间局部性原理，在 CPU 去内存取数据时，会一次性取一块数据到一级缓存（...），访问数组下一元素，可能就在一级缓存中，减少访问内存的开销，所以更快。而采用链式存储，CPU 取数据时，成块得取数据，而链表的下一个节点并不一定在该块内，访问下一节点还得再访问内存。

# golang 中的 map 使用有什么需要注意的

Map 在并发环境下，只读是安全的，同时读写是不安全的。

使用 sync.Map

# golang slice 作为参数传入函数是传的引用还是值

是引用。函数的参数都是传入的值的复制，slice 传入的也是值，只是这个值是 slice 在原始数组中的起始地址。将地址复制，再进行修改，仍然可以修改源数据，所以相当于传的是引用。