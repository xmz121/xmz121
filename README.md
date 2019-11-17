＃xmz121               字符串文件
首先让用户输入古诗，定义scaner，之后对文字进行处理用insert在字符之间添加符号，之后让用户输入一个字符，用indexof方法统计出古诗中这个词出现了几次
核心代码
用户输入部分：
Scanner in = new Scanner(System.in);// 定义scanner，等待输入
			System.out.println("请输入古诗:");
			String gushi = in.nextLine();
对字符中间添加符号并打印出来
                        
			StringBuffer s = new StringBuffer(gushi);  

			for (int i = 7; i < s.length(); i = i + 15) {
				s.insert(i, ",");
			}
			for (int i = 15; i < s.length() + 1; i = i + 16) {
				s.insert(i, "。");
			}
			for (int i = 16; i < s.length(); i = i + 17) {
				s.insert(i, "\n");
			}
			System.out.println(s);
 统计出古诗中这个词出现了几次
 int indexStart = 0;
			int count = 0;
			while (true) {
				int tm = a.indexOf(wenzi, indexStart);
				if (tm >= 0) {
					count++;
					indexStart = tm + wenzi.length();
				} else {
					break;
				}
			}
			if (count == 0) {
				System.out.println("这个字在文中没有出现");
			} else {
			
				System.out.println("这个文字共出现了" + count + "次");
			}
 异常处理部分：
 try{
 ………………
 
 }
 catch (Exception e) {
			System.err.println("发生异常" + e.toString());
		}

 
