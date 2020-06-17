package Student;


import Book.Book;

import java.util.Scanner;

class Student{
    String name;
    int age;
    String major;

    public Student(String name, int age, String major){
        this.name = name;
        this.age = age;
        this.major = major;
    }

    public void printInfo() {
        System.out.println(name + "\t" + age + "\t" + major);
    }

}
class Manage{
    public static final int SIZE = 100; //图书库最大藏书量
    Student[] students; //学生库
    int count;		//当前学生库人数
    Scanner scan;

    public Manage() {
        students = new Student[SIZE];
        //初始化图书库，默认里面有5本书，信息如下
        students[0] = new Student("张三", 18, "英语");
        students[1] = new Student("李四", 19, "计算机");
        students[2] = new Student("王五", 18, "电子信息");


        count = 3;
        scan = new Scanner(System.in);
    }

    public void run(){

        int userChoice = 0;
        //循环处理，直到用户选择了“0...退出”
        do{
            displayMenu();

            //读取用户输入
            userChoice = scan.nextInt();

            switch(userChoice){
                case 0:
                    System.out.println("成功退出系统，欢迎再次使用！");
                    break;
                case 1:
                    //显示学生库
                    break;
                case 2:
                    //增加学生
                    break;
                case 3:
                    //删除学生
                    break;
                case 4:
                    //修改学生
                    break;
                case 5:
                    //查询学生
                    break;
                default:
                    System.out.println("输入非法,请重新输入！");

            }
        }while(userChoice != 0);
        scan.close();
    }

    void displayMenu(){

        //打印菜单
        System.out.println("---------------------");
        System.out.println("    学生管理系统     ");
        System.out.println("---------------------");
        System.out.println("|   0...退出系统	|");
        System.out.println("|   1...显示学生	|");
        System.out.println("|   2...增加学生	|");
        System.out.println("|   3...删除学生	|");
        System.out.println("|   4...修改学生	|");
        System.out.println("|   5...查询学生	|");
        System.out.println("---------------------");
        System.out.print("请输入选项：");
    }
    void printStudent(){//显示学生

    }
    void addStudent(){//增加学生

    }
    void deleteStudent(){//删除学生

    }
    void modifyStudent(){//修改学生

    }
    void findStudent(){//查询学生

    }

}
public class Text {

    public static void main(String args){
        Manage studentManage = new Manage();
        studentManage.run();
    }
}
