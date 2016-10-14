# 2016-10-13工作日志
===================

1.已完成的工作

日报系统的实现以及java连接数据库

2.工作成果

/**
 * Created by 王志文 on 2016/10/13.
 */
public class RibaoController {
    private Scanner scanner;
    RibaoService ribaoService = new RibaoService();
    public RibaoController(Scanner scanner) {
        this.scanner = scanner;
    }
    int id;
    String ribaoname;
    String shouldwork;
    String finishwork;
    String nowork;
    String reason;
    String shouildo;

    public void register() {

        // 新增
        System.out.println("请输入日报id");
        id=scanner.nextInt();

        System.out.println("请输入日报名称");
         ribaoname = scanner.next();

        System.out.println("请输入应该完成的工作");
        shouldwork = scanner.next();

        System.out.println("请输入已经完成的工作");
        finishwork = scanner.next();

        System.out.println("请输入未完成的工作");
        nowork = scanner.next();

        System.out.println("请输入未完成的原因");
        reason = scanner.next();

        System.out.println("请输入怎么解决的");
        shouildo = scanner.next();
    }



    List<Map<String, Object>> list = ribaoService.getAllribao();
    StringBuffer sb=new StringBuffer();

    public void getList() {
        //查询
        System.out.println("目前系统所有的日报清单如下：");
        for (Map<String, Object> map : list) {
            for (Map.Entry<String, Object> entry : map.entrySet()) {
                String key = entry.getKey();
                Object value = entry.getValue();
                System.out.println(key + ":" + value + ",");
            }
        }

    }
    public void addList(){

        //获取日期
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        String date = sdf.format(new Date());

        //新增
        sb.append(" insert into daily_ (id,name,create_date,should_finished_work,have_finished_work,unfinished_work_reason," +
                "question_and_answer,next_day_plain) values ( \"");
        sb.append(id + "\",\"");
        sb.append(ribaoname + " \",\"");
        sb.append(date + "\",\"");
        sb.append(shouldwork + "\",\"");
        sb.append(finishwork + "\",\"");
        sb.append(nowork + "\",\"");
        sb.append(reason + "\",\"");
        sb.append(shouildo + "\" ) ");
        DBUtils.modifyTable(sb.toString());
    }

}



import com.feicuiedu.daily.controller.RibaoController;
import com.feicuiedu.daily.controller.UserController;

import java.util.*;

/**
 * Created by chenyan on 2016/10/10.
 */
public class Main {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        UserController userController = new UserController(scanner);

        RibaoController ribaoController=new RibaoController(scanner);

        String filePath = "F:\\gongzuowenjian\\wwwww\\java_demo\\daily\\src\\main\\resources";

        String fileName = "welcome.txt";

        userController.showSelectItem(filePath, fileName);

        int selected = userController.selectedItem();

        boolean loginResult = false;

        if (1 == selected) {

            // 登录
            loginResult = userController.login();
        }
        else {

            // 注册
            userController.register();
        }

        // 登录成功后的操作
        if (loginResult) {

            fileName = "operate_item.txt";

            userController.showSelectItem(filePath, fileName);

            selected = userController.selectedItem();
        }
        else {

        }
        switch (selected){
            case 1:
                // 查看日报
                ribaoController.getList();
                break;
            case 2:
                // 新增日报
                ribaoController.register();
                ribaoController.addList();
                System.out.println("日报已存入");
                break;
            case 3:
                // 退出
                System.out.println("再见");
                break;
            default:
                System.out.println("系统错误");
                System.exit(-1);
        }
    }
}

3.未完成的工作

无

4.未完成的原因

无

5.遇到的问题及解决方案

请教老师和同学，翻看教材ppt
