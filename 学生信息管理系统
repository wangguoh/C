#include<stdio.h>
#include<stdlib.h>
struct Student
{
	int stuID;
	char stuName[20];
	int stuAge;
	char stuGen[2];
	struct Student * next;
}student[500];

int main()
{
	int x=0,a,b,c=0,i=0,j=0;//
	char y[100],d[100];
	struct Student *header;
	header=NULL;//当前的节点中指向下一个节点的指针变量值永远为NULL 
	struct Student *p;
	printf("欢迎来到学生信息管理系统\n");
	
	while(1)
	{
		printf("输入学生信息请按1\n");
		printf("查询学生信息请按2\n");
		printf("删除学生信息请按3\n");
		printf("打印所以信息请按4\n"); 
		printf("退出系统请按5\n");
		scanf("%d",&x) || scanf("%s",&y); //防止用户错误输入  
		if(x==1)
		{
			printf("请依次输入学生的学号，姓名，年龄，性别(用空格隔开)\n");
			scanf("%d %s %d %s",&student[i].stuID,&student[i].stuName,&student[i].stuAge,&student[i].stuGen); 
			switch(i)//生成链表 
			{
				case 0: header =&student[i];
						student[i].next=NULL;
						break;
				default : student[i-1].next=&student[i];
						  student[i].next=NULL;
						  break;
			}
			i++;
			system("CLS");//清理屏幕 ,隐藏输入的学生信息 
			printf("信息录入成功\n");
		}
		else if(x==2)
		{
			printf("请输入待查询的学生的学号:\n");
			scanf("%d",&a);
			p=header; 
			while(p!=NULL)
			{
				if((*p).stuID==a)
				{
					printf("姓名:%s 年龄:%d 性别:%s\n",(*p).stuName,(*p).stuAge,(*p).stuGen);
					break;
				}
				else
					p=p->next;
			}
		}
		else if(x==3)	
		{
			printf("请输入待删除学生的学号:\n");
			scanf("%d",&b);
			p=header;
			while(p!=NULL)
			{
				if(b==student[0].stuID)//删除的学生信息为第一个 
				{
					header=NULL;
					printf("删除成功\n");
					break;
				}
				else if(p->stuID==b)//删除的学生信息不为第一个 
				{
					student[j-1].next=student[j].next;
					student[j].next=NULL;
					printf("删除成功\n");
						break;
				}
				else
				{
					p=p->next;
					j++;
				}
			}
		}
		else if(x==4)
		{
			printf("是否选择清理屏幕所以显示?(1表示同意，其他任意键表示拒绝)\n");
			scanf("%d",&c) || scanf("%s",&d);
			if(c==1)
				system("CLS");
			p=header;
			while(p!=NULL)
			{
				printf("学号:%d 姓名:%s 年龄:%d 性别:%s\n",p->stuID,p->stuName,p->stuAge,p->stuGen);
				p=p->next;
			}
		}
		else if(x==5)
		{
			break;
		}
		else
		{
			printf("你的输入有误,请重新输入\n");
			continue;	
		}
	}
	return 0;
}
