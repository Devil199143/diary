# 2016-09-26工作日志
===================

1. 已完成的工作内容

    常用类（Math等，String和StringBuffer）的学习。
    
    Math类的常用方法
    
    Random类的常用方法
    
    Arrays类的常用方法
    
    System类的常用方法
    
    Date类的常用方法
    
    Calendar类的常用方法


2. 工作成果

    package edu.feicui.demo.math;

    public class Math_Round {

	    /**
      
	     * 四舍五入
       
	     * 
       
	     * @param args
       
	     */
       
    	public static void main(String[] args) {
      
		    System.out.println(Math.round(123.556));
        
	    }
      
    }
    
    package edu.feicui.demo.random;

    import java.util.Random;

    public class RandomExercise {
    
	    public static void main(String[] args) {
      
		    Random r = new Random();// 创建Random对象
        
		    / /打印出不大于18的整数
        
	    	System.out.println(r.nextInt(18));
        
	    }
      
    }
    
    package edu.feicui.demo.Date;

    import java.util.Date;

    public class Millisecond {
    
	    public static void main(String[] args) {
      
	    	Date date = new Date();
        
		    long nowTime = date.getTime();// 返回的是当前的毫秒值
        
	     	System.out.println("nowTime:" + nowTime);
        
	    }
      
    }
    
    package edu.feicui.demo.calendar;

    import java.util.Calendar;

    public class PresentTime {
	    public static void main(String[] args) {
	    	// TODO Auto-generated method stub

	    	Calendar c = Calendar.getInstance();
	    	String str = "";
		    int year = c.get(c.YEAR);
		    int month = c.get(c.MONTH) + 1;
		    int day = c.get(c.DATE);
		    int hour = c.get(c.HOUR);
		    int minute = c.get(c.MINUTE);
		    int second = c.get(c.SECOND);
		    int week = c.get(c.DAY_OF_WEEK);
		    switch (week) {
		    case Calendar.SUNDAY:
			    str = "星期日";
		    	break;
		    case Calendar.MONDAY:
			    str = "星期一";
			    break;
	      case Calendar.TUESDAY:
			    str = "星期二";
			    break;
		    case Calendar.WEDNESDAY:
			    str = "星期三";
		    	break;
		    case Calendar.THURSDAY:
			    str = "星期四";
			    break;
	    	case Calendar.FRIDAY:
			    str = "星期五";
			    break;
		    case Calendar.SATURDAY:
			    str = "星期六";
			    break;
	    	}
		    String time = year + "-" + month + "-" + day + "	" + hour + ":"
			    	+ minute + ":" + second + "		" + str;
	    	System.out.println(time);

	    }
    }

    package edu.feicui.demo.string;

    import java.util.Scanner;

    public class Login {
	    public static void main(String[] args) {
	    	Scanner input = new Scanner(System.in);
	    	String uname, pwd;
	    	System.out.print("请输入用户名： ");
		    uname = input.next();
		    System.out.print("请输入密码： ");
	    	pwd = input.next();
	    	if (uname.equals("TOM") && pwd.equals("1234567")) {
		    	System.out.print("登录成功！ ");
	    	} else {
		    	System.out.print("用户名或密码不匹配，登录失败！");
	    	}

	    	/**
		     * 第二种
		     */
	     if (uname.equals("tom") && pwd.equals("abcd")) {
		    	System.out.print("登录成功！ ");
	    	} else {
		    	System.out.print("用户名或密码不匹配，登录失败！");
	    	}

	    }
    }



	    
3. 未完成工作

    无 
4. 未完成原因

    无

5. 遇到的问题及解决方案

    请教老师，多看ppt

