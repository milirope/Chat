package sql;

import java.awt.BorderLayout;
import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import javax.swing.JLabel;
import javax.swing.JOptionPane;
import javax.swing.JTextField;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import java.awt.Font;
import javax.swing.SwingConstants;
import java.awt.Color;
import java.awt.SystemColor;

public class Server extends JFrame {

	private JPanel contentPane;
	private JTextField name1;
	private JTextField name2;
	private JLabel lblNewLabel_2;

	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Server frame = new Server();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	
	public Server() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 402, 291);
		contentPane = new JPanel();
		contentPane.setBackground(SystemColor.inactiveCaptionBorder);
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		JLabel lblNewLabel = new JLabel("First username");
		lblNewLabel.setHorizontalAlignment(SwingConstants.CENTER);
		lblNewLabel.setFont(new Font("Sitka Display", Font.PLAIN, 16));
		lblNewLabel.setBounds(3, 48, 176, 23);
		contentPane.add(lblNewLabel);
		
		JLabel lblNewLabel_1 = new JLabel("Second username");
		lblNewLabel_1.setHorizontalAlignment(SwingConstants.CENTER);
		lblNewLabel_1.setFont(new Font("Sitka Heading", Font.PLAIN, 16));
		lblNewLabel_1.setBounds(10, 96, 169, 23);
		contentPane.add(lblNewLabel_1);
		
		name1 = new JTextField();
		name1.setBackground(SystemColor.activeCaption);
		name1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				//code
				createRoom();
			}
		});
		name1.setBounds(189, 47, 169, 29);
		contentPane.add(name1);
		name1.setColumns(10);
		
		name2 = new JTextField();
		name2.setBackground(SystemColor.activeCaption);
		name2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				//code
				createRoom();
				
			}
		});
		name2.setBounds(189, 95, 169, 29);
		contentPane.add(name2);
		name2.setColumns(10);
		
		JButton btnNewButton = new JButton("Join Chat");
		btnNewButton.setBackground(SystemColor.info);
		btnNewButton.setForeground(SystemColor.desktop);
		btnNewButton.setFont(new Font("Sitka Subheading", Font.PLAIN, 19));
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				//code
				createRoom();
			}
		});
		btnNewButton.setBounds(77, 156, 238, 40);
		contentPane.add(btnNewButton);
		
		lblNewLabel_2 = new JLabel("Welcome");
		lblNewLabel_2.setBackground(SystemColor.inactiveCaption);
		lblNewLabel_2.setForeground(SystemColor.activeCaption);
		lblNewLabel_2.setFont(new Font("Shrikhand", Font.PLAIN, 19));
		lblNewLabel_2.setHorizontalAlignment(SwingConstants.CENTER);
		lblNewLabel_2.setBounds(132, 11, 105, 26);
		contentPane.add(lblNewLabel_2);
	}

	private void createRoom() {
		String p1,p2;
		p1 = name1.getText();
		p2 = name2.getText();
		
		if(p1.equals("") || p2.equals("")) {
			JOptionPane.showMessageDialog(null, "Please Enter a Valid Username");
			return;
		}
		
		Chat1.username1 = name1.getText();
		Chat2.username2 = name2.getText();
		ChatRoom.createRoom();
	}
}
