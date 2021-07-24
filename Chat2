package sql;

import java.awt.EventQueue;  
import javax.swing.JFrame;   
import javax.swing.JPanel;  
import javax.swing.border.EmptyBorder;
import javax.swing.JTextArea;
import javax.swing.DefaultComboBoxModel;  
import javax.swing.JButton;   
import javax.swing.JLabel;   
import javax.swing.JOptionPane;  
import java.awt.event.ActionListener;   
import java.sql.Connection;   
import java.sql.DriverManager;   
import java.sql.ResultSet;   
import java.sql.Statement;   
import java.awt.event.ActionEvent;   
import java.awt.Color;
import java.awt.Font;   
import java.awt.SystemColor;
import javax.swing.JTextField;  
import javax.swing.JComboBox;   
import javax.swing.JTable;   
import javax.swing.border.EtchedBorder;   
import javax.swing.table.DefaultTableModel;  
import javax.swing.SwingConstants;   




public class Chat2 extends JFrame {

    private final String user = "postgres";
    private final String password = "masterkey";
	
	static String username2;
	private JPanel contentPane;

	void presentar() {
		DefaultTableModel modelo = new DefaultTableModel();
		modelo.addColumn("id");
		modelo.addColumn("name");
		modelo.addColumn("division");
		modelo.addColumn("color");
		modelo.addColumn("phylum");
		modelo.addColumn("duration");
		modelo.addColumn("type");
		
		table_2.setModel(modelo);
		
		String datos[] = new String[7];
		Statement at = null;
		String url = "jdbc:postgresql://localhost:5432/test";
		
		try {
			
			
			Connection base = DriverManager.getConnection(url, user, password);
			at = base.createStatement();
			ResultSet rs = at.executeQuery("SELECT * FROM plant2");
			while (rs.next()) {
				datos[0] = rs.getString("id");
				datos[1] = rs.getString("name");
				datos[2] = rs.getString("division");
				datos[3] = rs.getString("color");
				datos[4] = rs.getString("phylum");
				datos[5] = rs.getString("duration");
				datos[6] = rs.getString("type");
				modelo.addRow(datos);
				
				
			}
			
			rs.close();
			at.close();
			
		} catch (Exception e) {
			JOptionPane.showMessageDialog(null, e);
		}
	}
	
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Chat1 frame = new Chat1();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	
	public Chat2() {

		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 775, 480);
		contentPane = new JPanel();
		contentPane.setForeground(new Color(255, 228, 225));
		contentPane.setBackground(new Color(255, 228, 225));
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		 chat2 = new JTextArea();
		 chat2.setBackground(SystemColor.activeCaption);
		chat2.setBounds(546, 70, 196, 263);
		contentPane.add(chat2);
		
		 text2 = new JTextArea();
		text2.setBounds(546, 343, 203, 40);
		contentPane.add(text2);
		
		 send2 = new JButton("SEND");
		 send2.setBackground(SystemColor.activeCaption);
		 send2.setForeground(new Color(0, 0, 0));
		 send2.setFont(new Font("Sitka Small", Font.PLAIN, 13));
		send2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				
				String s = text2.getText();
				if(s.equals("")) {
					return;
					
				}if(s.equals("/plant")) {
					DefaultTableModel modelo = new DefaultTableModel();
					modelo.addColumn("id");
					modelo.addColumn("name");
					modelo.addColumn("division");
					modelo.addColumn("color");
					modelo.addColumn("phylum");
					modelo.addColumn("duration");
					modelo.addColumn("type");
					
					table_2.setModel(modelo);
					
					
					String datos[] = new String[7];
					Statement at = null;
					String url = "jdbc:postgresql://localhost:5432/test";
					
					try {
						
						Connection base = DriverManager.getConnection(url, user, password);
						at = base.createStatement();
						
						ResultSet rs = at.executeQuery("SELECT * FROM plant2");
						while (rs.next()) {
							datos[0] = rs.getString("id");
							datos[1] = rs.getString("name");
							datos[2] = rs.getString("division");
							datos[3] = rs.getString("color");
							datos[4] = rs.getString("phylum");
							datos[5] = rs.getString("duration");
							datos[6] = rs.getString("type");
							modelo.addRow(datos);
						}
						
						rs.close();
						at.close();
						
					} catch (Exception e) {
						JOptionPane.showMessageDialog(null, e);
					}
				}
				
				chat2.append(username2 + ":" + s + "\n");
				Chat1.sendText();
				text2.setText("");
				
			}
		});
		send2.setBounds(653, 398, 89, 29);
		getContentPane().add(send2);
		
		
		 label2 = new JLabel("Chat Window for : " + Chat1.username1);
		 label2.setForeground(SystemColor.activeCaption);
		 label2.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 18));
		label2.setBounds(546, 33, 210, 22);
		contentPane.add(label2);
		
		JButton clear = new JButton("CLEAR");
		clear.setFont(new Font("Sitka Small", Font.PLAIN, 13));
		clear.setBackground(SystemColor.activeCaption);
		clear.setForeground(new Color(0, 0, 0));
		clear.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				chat2.setText("");
			}
		});
		
		clear.setBounds(556, 397, 89, 30);
		getContentPane().add(clear);
		
		
		
		lblNewLabel = new JLabel("Plantas");
		lblNewLabel.setHorizontalAlignment(SwingConstants.CENTER);
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD | Font.ITALIC, 18));
		lblNewLabel.setBounds(-217, 0, 756, 49);
		contentPane.add(lblNewLabel);
		
		lblNewLabel_1 = new JLabel("Id");
		lblNewLabel_1.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_1.setBounds(358, 61, 60, 14);
		contentPane.add(lblNewLabel_1);
		
		lblNewLabel_2 = new JLabel("Name");
		lblNewLabel_2.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_2.setBounds(358, 96, 60, 14);
		contentPane.add(lblNewLabel_2);
		
		lblNewLabel_3 = new JLabel("Division");
		lblNewLabel_3.setFont(new Font("Tahoma", Font.PLAIN, 15));
		lblNewLabel_3.setBounds(358, 140, 60, 14);
		contentPane.add(lblNewLabel_3);
		
		lblNewLabel_4 = new JLabel("Color");
		lblNewLabel_4.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_4.setBounds(358, 186, 60, 14);
		contentPane.add(lblNewLabel_4);
		
		lblNewLabel_5 = new JLabel("Phylum");
		lblNewLabel_5.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_5.setBounds(358, 226, 60, 14);
		contentPane.add(lblNewLabel_5);
		
		lblNewLabel_6 = new JLabel("Duration");
		lblNewLabel_6.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_6.setBounds(358, 266, 60, 14);
		contentPane.add(lblNewLabel_6);
		
				
		lblNewLabel_7 = new JLabel("Type");
		lblNewLabel_7.setFont(new Font("Tahoma", Font.PLAIN, 14));
		lblNewLabel_7.setBounds(358, 311, 60, 14);
		contentPane.add(lblNewLabel_7);
		
		
		id = new JTextField();
		id.setColumns(10);
		id.setBounds(428, 59, 86, 20);
		contentPane.add(id);
		
		Tname = new JTextField();
		Tname.setColumns(10);
		Tname.setBounds(428, 96, 86, 20);
		contentPane.add(Tname);
		
		Tcolor = new JTextField();
		Tcolor.setColumns(10);
		Tcolor.setBounds(428, 186, 86, 20);
		contentPane.add(Tcolor);
		
		TPhylum = new JTextField();
		TPhylum.setColumns(10);
		TPhylum.setBounds(428, 226, 86, 20);
		contentPane.add(TPhylum);

		Cdivision = new JComboBox();
		Cdivision.setModel(new DefaultComboBoxModel(new String[] {"", "Briofito", "Pteridofita", "Angiosperma", "Gimnosperma"}));
		Cdivision.setBounds(428, 138, 86, 22);
		contentPane.add(Cdivision);
		
		Cduration = new JComboBox();
		Cduration.setModel(new DefaultComboBoxModel(new String[] {"", "Perennes", "Binuales", "Anuales"}));
		Cduration.setBounds(428, 264, 86, 22);
		contentPane.add(Cduration);
		
		Ctype = new JComboBox();
		Ctype.setModel(new DefaultComboBoxModel(new String[] {"", "Algas", "Musgo", "Hierbas", "Helechos", "Coniferas", "Arboles", "Arbustos", "Trepadoras", "Suculentas"}));
		Ctype.setBounds(428, 314, 86, 22);
		contentPane.add(Ctype);
		


		
		
		btnAgregar = new JButton("Agregar");
		btnAgregar.setFont(new Font("Tahoma", Font.BOLD | Font.ITALIC, 10));
		btnAgregar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				Connection con = null;
				String urlDatabase = "jdbc:postgresql://localhost:5432/test";
				
				try {
					Class.forName("org.postgresql.Driver");
					con = DriverManager.getConnection(urlDatabase, user, password);
					Statement st = con.createStatement();
					String sql = "INSERT INTO plant2(id, name, division, color, phylum, duration, type)"
							+ "VALUES ('" + id.getText() + "', '" + Tname.getText() + "', '" + Cdivision.getSelectedItem() + "', '" + Tcolor.getText() + "', '" + TPhylum.getText() + "', '" + Cduration.getSelectedItem() + "', '" + Ctype.getSelectedItem() + "')";
					
					st.executeQuery(sql);
					con.close();
					st.close();
					
				} catch (Exception e1) {
					JOptionPane.showMessageDialog(null, e1);
				}
				
				presentar();

			}});
		
		btnAgregar.setBounds(10, 368, 146, 23);
		getContentPane().add(btnAgregar);
		
		
		
		btnModificar = new JButton("Modificar");
		btnModificar.setFont(new Font("Tahoma", Font.BOLD | Font.ITALIC, 10));
		btnModificar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				Connection con = null;
				String urlDatabase = "jdbc:postgresql://localhost:5432/test";
				
				try {
					
					Class.forName("org.postgresql.Driver");
					con = DriverManager.getConnection(urlDatabase, user, password);
					Statement st = con.createStatement();
					String sql = "UPDATE plant1 SET"
							+ " id='" + id.getText() + "', name='" + Tname.getText() + "', division='" + Cdivision.getSelectedItem() + "', color='" + Tcolor.getText() + "', phylum='" + TPhylum.getText() + "', duration='" + Cduration.getSelectedItem()  + "', type='" +  Ctype.getSelectedItem() + "' WHERE id='" + id.getText() + "'";
					
					ResultSet result = st.executeQuery(sql);
					con.close();
					st.close();
					
				} catch (Exception e1) {
					JOptionPane.showMessageDialog(null, e1);
				}
				
				presentar();
				
			}
		});
		
		btnModificar.setBounds(179, 368, 146, 23);
		getContentPane().add(btnModificar);
		
		
		
		
		btnEliminar = new JButton("Eliminar");
		btnEliminar.setFont(new Font("Tahoma", Font.BOLD | Font.ITALIC, 10));
		btnEliminar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				Connection con = null;
				String urlDatabase = "jdbc:postgresql://localhost:5432/test";
				
				try {
					
					Class.forName("org.postgresql.Driver");
					con = DriverManager.getConnection(urlDatabase, user, password);
					Statement st = con.createStatement();
					String sql = "DELETE FROM plant1 WHERE id='" + id.getText() + "'";
					ResultSet result = st.executeQuery(sql);
					con.close();
					st.close();
					
				} catch (Exception e1) {
					JOptionPane.showMessageDialog(null, e1);
				}
				
				presentar();
				
			}
		});
		
		btnEliminar.setBounds(179, 404, 146, 23);
		getContentPane().add(btnEliminar);
		
		
		
		btnPresentar = new JButton("Presentar");
		btnPresentar.setFont(new Font("Tahoma", Font.BOLD | Font.ITALIC, 10));
		
		btnPresentar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				presentar();

			}
		});
		
		btnPresentar.setBounds(10, 404, 146, 23);
		getContentPane().add(btnPresentar);
	
		
		

	table_2 = new JTable();
	table_2.setSurrendersFocusOnKeystroke(true);
	table_2.setEnabled(false);
	table_2.setModel(new DefaultTableModel(
			
			new Object[][] {
			},
			new String[] {
			}
		));
	
	
	table_2.setBorder(new EtchedBorder(EtchedBorder.LOWERED, null, null));
	table_2.setBounds(10, 54, 315, 287);
	contentPane.add(table_2);
	
	}
	
	
	public static void sendText() {
    	String s= Chat1.text1.getText();
    	if (s.equals("")) {
    		return;
    	}
    	chat2.append(Chat1.username1 + ":" + s + "\n");
    }
	
	
	private javax.swing.JLabel label2;
    private static javax.swing.JTextArea chat2;
    private javax.swing.JButton send2;
    public static javax.swing.JTextArea text2;
    private JLabel lblNewLabel;
    private JLabel lblNewLabel_1;
    private JLabel lblNewLabel_2;
    private JLabel lblNewLabel_3;
    private JLabel lblNewLabel_4;
    private JLabel lblNewLabel_5;
    private JLabel lblNewLabel_6;
    private JTextField id;
    private JTextField Tname;
    private JTextField Tcolor;
    private JTextField TPhylum;
    private JLabel lblNewLabel_7;
    private JComboBox Cdivision;
    private JComboBox Cduration;
    private JComboBox Ctype;
    private JTable table_2;
    private JButton btnAgregar;
    private JButton btnModificar;
    private JButton btnEliminar;
    private JButton btnPresentar;
    

}
