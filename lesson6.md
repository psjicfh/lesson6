#lesson6笔记

    #include<stdio.h>
	int main(void)
	{
		printf("hello world\n");
		return 0;
	}
	akaedu@akaedu-desktop:~$ cd work/lesson6
	akaedu@akaedu-desktop:~/work/lesson6$ ls
	lesson6  lesson6.c  lesson6.md
	akaedu@akaedu-desktop:~/work/lesson6$ vim lesson6.c
	akaedu@akaedu-desktop:~/work/lesson6$ gcc -wall lesson6.c
	gcc: unrecognized option '-wall'
	akaedu@akaedu-desktop:~/work/lesson6$ ls
	a.out  lesson6  lesson6.c  lesson6.md
	akaedu@akaedu-desktop:~/work/lesson6$ ./a.out
	hello world
	akaedu@akaedu-desktop:~/work/lesson6$ gcc -wall -o lesson6 lesson6.c
	gcc: unrecognized option '-wall'  //注意W要大写
	akaedu@akaedu-desktop:~/work/lesson6$ ls
	lesson6  lesson6.c  lesson6.md
	akaedu@akaedu-desktop:~/work/lesson6$ 
	akaedu@akaedu-desktop:~/work/lesson6$ echo $? //查看返回值
	0   //系统定义返回值为0系统执行成功，否则失败
	akaedu@akaedu-desktop:~/work/lesson6$ vim lesson6.c
	akaedu@akaedu-desktop:~/work/lesson6$
###要用 git push
 	akaedu@akaedu-desktop:~/work/lesson6$ vim lesson6.md
	akaedu@akaedu-desktop:~/work/lesson6$ git commit -a -m "lesson6_2"
	[master 4e4761e] lesson6_2
	 1 files changed, 1 insertions(+), 0 deletions(-)
	akaedu@akaedu-desktop:~/work/lesson6$ git push //注：此时用git push即可
	Counting objects: 5, done.
	Delta compression using up to 2 threads.
	Compressing objects: 100% (2/2), done.
	Writing objects: 100% (3/3), 285 bytes, done.
	Total 3 (delta 1), reused 0 (delta 0)
	To git@github.com:psjicfh/lesson6.git
	   4e69560..4e4761e  master -> master
	akaedu@akaedu-desktop:~/work/lesson6$ 
	
	history 10 //显示最近10行历史命令
  	history >h.md  //把终端上的命令打印到文件h.md 里面

###不退出vim 在vim 基础上新打开一个bash
	例如：vim lesson6.c
              做修改后在普通模式下“:w” 保存
	      ":sh"：在vim上打开一个新bash 编译若发现错误
	      “exit”或“ctrl+d”返回vim  在普通模式下“u”：撤销 ctrl+r:前进
###例如：
	#include<stdio.h>
	int main(int argc, const char *argvc[])
	{
	    int i = 1;
	    if (i != 1)
	    {
	        printf("hello world\n");
	        return 1;
	    }
	    else
	    return 0;
	}
	akaedu@akaedu-desktop:~/work/lesson6$ gcc lesson6.c
	akaedu@akaedu-desktop:~/work/lesson6$ echo $?
	0   //返回0表示执行正确

	#include<stdio.h>
	int main(int argc, const char *argvc[])
	{
	    int i = 3;
	    if (i != 1)
	    {
	        printf("hello world\n");
	        return 1;
	    }
	    else
		return 0;
	}
        akaedu@akaedu-desktop:~/work/lesson6$ gcc lesson6.c
	akaedu@akaedu-desktop:~/work/lesson6$ ls
	a.out  h.md  lesson6  lesson6.c  lesson6.html  lesson6.md  push
	akaedu@akaedu-desktop:~/work/lesson6$ ./a.out
	hello world
	akaedu@akaedu-desktop:~/work/lesson6$ echo $?
	1   //返回1表示执行错误

###生成汇编文件
	kaedu@akaedu-desktop:~/work/lesson6$ gcc -S lesson6.c //生成汇编文件
	akaedu@akaedu-desktop:~/work/lesson6$ ls
	a.out  h.md  lesson6  lesson6.c  lesson6.html  lesson6.md  lesson6.s  pu	sh
	akaedu@akaedu-desktop:~/work/lesson6$ file lesson6.s //查看文件属性
	lesson6.s: ASCII assembler program text
	akaedu@akaedu-desktop:~/work/lesson6$ vim lesson6.s //看看汇编吓死你 哈
		      
	

