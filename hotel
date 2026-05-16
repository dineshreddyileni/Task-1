import java.util.ArrayList;
public class HotelReservationSystem {
    static class Room {
        int roomId;
        String category;
        double price;
        boolean available;
        Room(int roomId, String category, double price) {
            this.roomId = roomId;
            this.category = category;
            this.price = price;
            this.available = true;
        }
    }
    static class User {
        int userId;
        String name;
        User(int userId, String name) {
            this.userId = userId;
            this.name = name;
        }
    }
    static class Reservation {
        int reservationId;
        User user;
        Room room;
        String status;
        Reservation(int reservationId, User user, Room room) {
            this.reservationId = reservationId;
            this.user = user;
            this.room = room;
            this.status = "Booked";
        }
    }
    public static void main(String[] args) {
        ArrayList<Room> rooms = new ArrayList<>();
        rooms.add(new Room(101, "Standard", 1000));
        rooms.add(new Room(102, "Deluxe", 2000));
        rooms.add(new Room(103, "Suite", 3000));
        User user = new User(1, "Dinesh");
        ArrayList<Reservation> reservations = new ArrayList<>();
        System.out.println("Available Deluxe Rooms:");
        for (Room room : rooms) {
            if (room.category.equals("Deluxe") && room.available) {
                System.out.println("Room ID: " + room.roomId);
            }
        }
        for (Room room : rooms) {
            if (room.roomId == 102 && room.available) {
                System.out.println("\nProcessing payment of ₹" + room.price);
                System.out.println("Payment Successful");
                room.available = false;
                Reservation reservation =
                        new Reservation(1, user, room);
                reservations.add(reservation);
                System.out.println("Booking Successful");
            }
        }
        System.out.println("\nBooking Details:");
        for (Reservation r : reservations) {
            System.out.println(
                    "Reservation ID: " + r.reservationId +
                    ", User: " + r.user.name +
                    ", Room: " + r.room.roomId +
                    ", Status: " + r.status
            );
        }
        if (!reservations.isEmpty()) {
            Reservation r = reservations.get(0);
            r.status = "Cancelled";
            r.room.available = true;
            System.out.println("\nReservation Cancelled");
        }
        System.out.println("\nUpdated Booking Details:");
        for (Reservation r : reservations) {
            System.out.println(
                    "Reservation ID: " + r.reservationId +
                    ", User: " + r.user.name +
                    ", Room: " + r.room.roomId +
                    ", Status: " + r.status
            );
        }
    }
}
