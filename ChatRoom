package sql;

public class ChatRoom {
	static Chat1 ct1;
	static Chat2 ct2;
	static Server srvr;
	
	public ChatRoom() {
		srvr = new Server();
		srvr.setLocationRelativeTo(null);
		srvr.setVisible(true);
	}

	
		public static void createRoom() {
			ct1 = new Chat1();
			ct2 = new Chat2();
			ct1.setLocation(500, 200);
			ct2.setLocation(900, 200);
			ct1.setVisible(true);
			ct2.setVisible(true);
			srvr.setVisible(false);
		}
		
		
		public static void main(String[] args) {
			ChatRoom ChatRoom = new ChatRoom();
		}
}

