# 2016-10-12工作日志
===================

1.已完成的工作

android studio布局的学习

网络协议的学习（通过ip地址或主机名，对网页信息进行解析）

2.工作成果

public class InetAddressDemo {

    public static void main(String[] args) throws
            UnknownHostException {

        InetAddress i = InetAddress.getLocalHost();
        // 获取到本机名和地址
        System.out.println(i.toString());
        // 获取ip
        System.out.println("address:" + i.getHostAddress());
        // 获取主机名
        System.out.println("name:" + i.getHostName());

        // 获取任意一台主机地址
        InetAddress ia = InetAddress.getByName("www.baidu.com");
        System.out.println("ia.getHostName()"+ia.getHostName());
        System.out.println("ia.getHostAddress()"+ia.getHostAddress());
        // 获取百度多个IP
        InetAddress[] allByName = InetAddress.getAllByName("www.baidu.com");
        for (int j = 0; j < allByName.length; j++) {
            System.out.println(allByName[j].getHostAddress());
        }
    }
}

public class NetTest {

    public static void main(String[] args) {

        try {

            String url = "http://118.244.212.82:9092/newsClient/news_list";
            String params = "ver=1&subid=1&dir=1&nid=1&stamp=20140321&cnt=20";


            URL strUrl = new URL(url);
            HttpURLConnection httpURLConnection = (HttpURLConnection) strUrl.openConnection();
            httpURLConnection.setConnectTimeout(5000);

            httpURLConnection.setDoOutput(true);
            httpURLConnection.setDoInput(true);

            httpURLConnection.setRequestMethod("POST");
            // httpURLConnection.setRequestMethod("POST");

            // 获取输出流
            OutputStream out = httpURLConnection.getOutputStream();
            out.write(params.getBytes());
            out.flush();

            if (httpURLConnection.getResponseCode() == 200) {

                InputStream is = httpURLConnection.getInputStream();

                byte[] data = read(is);
                String str = new String(data, "UTF-8");
                //System.out.println("str="+str);

                JSONObject jsonObject = new JSONObject(str);

                Map<String,Object> map = new HashMap<String,Object>();

                map.put("message",jsonObject.get("message"));
                map.put("status",jsonObject.get("status"));

                JSONArray jsonArray = jsonObject.getJSONArray("data");
                List<Map<String,Object>> tmpList = new ArrayList<Map<String,Object>>();

                for (int i = 0; i <jsonArray.length() ; i++) {
                    JSONObject tmpObject = jsonArray.getJSONObject(i);

                    Map<String,Object> tmpMap = new HashMap<String,Object>();
                    tmpMap.put("summary",tmpObject.get("summary"));
                    tmpMap.put("icon",tmpObject.get("icon"));
                    tmpMap.put("stamp",tmpObject.get("stamp"));
                    tmpMap.put("title",tmpObject.get("title"));
                    tmpMap.put("nid",tmpObject.get("nid"));
                    tmpMap.put("link",tmpObject.get("link"));
                    tmpMap.put("type",tmpObject.get("type"));

                    tmpList.add(tmpMap);
                }

                map.put("data",tmpList);

                System.out.println(map);
            }
            else {
                System.out.println("连接失败");
            }

        }
        catch (MalformedURLException e) {
            e.printStackTrace();
        }
        catch (IOException e) {
            e.printStackTrace();
        }
        catch (Exception e) {
            e.printStackTrace();
        }
    }

    // 从流中读取数据
    public static byte[] read(InputStream inStream) throws Exception {
        ByteArrayOutputStream outStream = new ByteArrayOutputStream();
        byte[] buffer = new byte[1024];
        int len = 0;
        while ((len = inStream.read(buffer)) != -1) {
            outStream.write(buffer, 0, len);
        }
        inStream.close();
        return outStream.toByteArray();
    }
}


3.未完成的工作

无

4.未完成的原因

无

5.遇到的问题及解决方案

请教老师和同学，翻看教材ppt
