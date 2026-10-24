# 9-1
9,,,,,,,,,,,,,,,1
import java.sql.*;

class JDBCExample {
    public static void main(String args[]) {
        try {
            // Load JDBC Driver
            Class.forName("com.mysql.cj.jdbc.Driver");

            // Connect to database
            Connection con = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/studentdb",
                "root",
                "password"
            );

            System.out.println("Database connected successfully!");

            // Close connection
            con.close();
        }
        catch(Exception e) {
            System.out.println(e);
        }
    }
}
