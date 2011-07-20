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

