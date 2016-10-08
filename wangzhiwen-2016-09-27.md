# 2016-09-27工作日志
===================

1. 已完成的工作内容

    集合框架

2. 工作成果

    集合框架包含的内容
    
    ArrayList和LinkedList的使用
    
    HashSet和TreeSet使用
    
    HashMap的使用
    
    Iterator的使用
    
    泛型集合的使用
    
    public class Test1 {
    
	    public static void main(String[] args) {
      
		    Dog ououDog = new Dog("欧欧", "雪娜瑞");
        
		    Dog yayaDog = new Dog("亚亚", "拉布拉多");
        
		    Dog meimeiDog = new Dog("美美", "雪娜瑞");
        
		    Dog feifeiDog = new Dog("菲菲", "拉布拉多");		
        
		    List dogs = new ArrayList();
        
	    	dogs.add(ououDog);
        
		    dogs.add(yayaDog);
        
	    	dogs.add(meimeiDog);
        
		    dogs.add(2, feifeiDog); // 添加feifeiDog到指定位置		
        
		    System.out.println("共计有" + dogs.size() + "条狗狗。");
        
    public class VectorDemo {
    
	    public static void main(String[] args) {
      
	    	List<String> allList = null ;		// 声明List对象
        
	    	allList = new Vector<String>(); 	// 实例化List对象，只能是String类型
        
		    allList.add("Hello"); 			// 增加元素
        
	    	allList.add(0, "World");			// 增加元素
        
	    	allList.add("MLDN");			// 增加元素
        
		    or (int i = 0; i < allList.size(); i++) {	// 循环输出
        
		    	System.out.print(allList.get(i) + "、");// 通过get()取出每一个元素
          
		    }
        
	    }
      
    }
		
	    
3. 未完成工作

    无 
4. 未完成原因

    无

5. 遇到的问题及解决方案

    请教老师，多看ppt

