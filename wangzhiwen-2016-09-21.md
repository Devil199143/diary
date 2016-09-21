# 2016-09-21工作日志
===================

1. 已完成的工作内容

    继承与里氏替换原则的学习

2. 工作成果

	    package com.feicui.java09202;
	
    	public class Dog extends Pet{
		    public void catchingFlyDisc(){
			    super.health=super.health-10;
          super.love=super.love+5;
    	    System.out.println("我的健康值是："+super.health+"我与主人的亲密程度是："+super.love);
			
			
		    }
	    }


    package com.feicui.java09202;

    public class Penguin extends Pet{
    	public void swimming(){
	    	super.health=super.health-10;
	    	super.love=super.love+5;
	    	System.out.println("我的健康值是："+super.health+"我与主人的亲密程度是："+super.love);
		
    	}

    }


    package com.feicui.java09202;

    public class People {
	    public void play(Pet pet){
	    	if(pet instanceof Dog){
		    	((Dog) pet).catchingFlyDisc();
	    	}else if(pet instanceof Penguin){
		    	((Penguin) pet).swimming();
		    }
	    }
    }


    package com.feicui.java09202;

    public class Pet {
    	String name;
    	int health;
	    int love;
	
    	public String getName() {
	    	return name;
    	}

	    public void setName(String name) {
	    	this.name = name;
	    }

    	public int getHealth() {
    		return health;
    	}

    		this.health = health;
    	}

    	public int getLove() {
	    	return love;
     }

    	public void setLove(int love) {
    		this.love = love;
    
	    public void say(){
	    	System.out.println("我的健康值是："+health+"我与主人的亲密程度是："+love);
    	}

     }


    package com.feicui.java09202;

    import java.util.Scanner;

    public class Text {
	

    		System.out.println("欢迎来到这里");
	    	System.out.println("请选择您要跟哪个宠物玩耍");
	    	Scanner input=new Scanner(System.in);
		    String name=input.next();
		    System.out.println("请选择你要玩耍的宠物类型：（1.狗狗2.企鹅）");
		    int type=input.nextInt();
	    	People people=new People();
	    	if(type==1){
	    		people.play();
		    }else if(type==2){
		    	people.play();
	    	}
		
    	}

    }
3. 未完成工作

    无 
4. 未完成原因

    无

5. 遇到的问题及解决方案

    请教老师，多看ppt

