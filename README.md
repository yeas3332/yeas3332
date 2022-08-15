- 👋 Hi, I’m @yeas3332
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
yeas3332/yeas3332 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
package hhu.yy.oo;

/**
 * @User; san zhi yang🐏
 * @DATE；2022/8/14
 * @Time; 9:29
 * @Description:
 */
import java.awt.BorderLayout;
import java.awt.Toolkit;
import java.awt.image.ImageObserver;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.JTextField;
public class MyFrame extends JFrame {
    private JLabel lab_name;
    private JLabel lab_number;
    private JLabel lab_amount;
    private JTextField jtf_name;
    private JTextField jtf_number;
    private JTextField jtf_amount;
    private JButton but_1;
    private JButton but_2;
    private JButton but_3;
    public MyFrame(){
        setSize(900, 600);
        setTitle("三只\uD83D\uDC0F");
        Toolkit tk = Toolkit.getDefaultToolkit();

        this.setLayout(null);
        lab_name = new JLabel("姓名");
        lab_number = new JLabel("性别");
        lab_amount = new JLabel("年龄");
        jtf_name = new JTextField(13);
        jtf_number = new JTextField(13);
        jtf_amount = new JTextField(13);
        JPanel jp_top = new JPanel();
        jp_top.setBounds(10, 100, 245, 100);

        jp_top.setLayout(new BorderLayout());
        JPanel jp_top_name = new JPanel();
        JPanel jp_top_number = new JPanel();
        JPanel jp_top_amount = new JPanel();
        jp_top_name.add(lab_name);
        jp_top_name.add(jtf_name);
        jp_top_number.add(lab_number);
        jp_top_number.add(jtf_number);
        jp_top_amount.add(lab_amount);
        jp_top_amount.add(jtf_amount);
        jp_top.add(jp_top_name,BorderLayout.NORTH);
        jp_top.add(jp_top_number,BorderLayout.CENTER);
        jp_top.add(jp_top_amount,BorderLayout.SOUTH);
        JPanel jp_bottom = new JPanel();
        jp_bottom.setBounds(-130,300, 550, 600);
        but_1 = new JButton("提交");
        but_2 = new JButton("取消");
        but_3 = new JButton("重写");
        jp_bottom.add(but_1);
        jp_bottom.add(but_2);
        jp_bottom.add(but_3);
        this.add(jp_top,BorderLayout.NORTH);
        this.add(jp_bottom,BorderLayout.CENTER);
        setVisible(true);

        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
    public static void main(String[] args) {
        new MyFrame();
    }
}
