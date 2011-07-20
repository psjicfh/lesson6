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
 
