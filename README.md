# ParkingLot

# Design a Parking Lot
- The parking lot should have multiple floors where customers can park their cars.

- The parking lot should have multiple entry and exit points.

- Customers can collect a parking ticket from the entry points and can pay the parking fee at the exit points on their way out.

- Customers can pay the tickets at the automated exit panel or to the parking attendant.

- Customers can pay via both cash and credit cards.

- Customers should also be able to pay the parking fee at the customer’s info portal on each floor. If the customer has paid at the info portal, they don’t have to pay at the exit.

- The system should not allow more vehicles than the maximum capacity of the parking lot. If the parking is full, the system should be able to show a message at the entrance panel and on the parking display board on the ground floor.

- Each parking floor will have many parking spots. The system should support multiple types of parking spots such as Compact, Large, Handicapped, Motorcycle, etc.

- The Parking lot should have some parking spots specified for electric cars. These spots should have an electric panel through which customers can pay and charge their vehicles.

- The system should support parking for different types of vehicles like car, truck, van, motorcycle, etc.

- Each parking floor should have a display board showing any free parking spot for each spot type.

- The system should support a per-hour parking fee model. For example, customers have to pay $4 for the first hour, $3.5 for the second and third hours, and $2.5 for all the remaining hours.

# Classes
- *ParkingLot:* It has attributes like ‘Name’ to distinguish it from any other parking lots and ‘Address’ to define its location. It will have a list of parking floor instances as one of its members. It also a Parking Rate associated with it.

- *ParkingFloor:* The parking lot will have multiple parking floors.

- *ParkingSpot:* Each parking floor will have many parking spots. Different parking spots are defined in the enumeration ParkingSportType.

- *Account:* We will have two types of accounts in the system: one for an Admin, and the other for a parking attendant. Admin can add parking floors, parking spots, etc.. Parking Attendant can scan tickets, process payments, etc..

- *Parking ticket:* The parking lot has the class Parking Ticket in it.

- *Vehicle:* Vehicles will be parked in the parking spots. In other words, the parking spot class will have an object of type vehicle.

- *EntranceGate and ExitGate:* EntranceGate will print tickets, and ExitPanel will process payment of the ticket fee.

- *PaymentCalculation:* This class will be responsible for making payments. The system will support credit card and cash transactions. Also, for charging the electric vehicle, payment will be made from here.

- *ParkingRate:* This class will keep track of the hourly parking rates.

- *ParkingDisplayBoard:* Each parking floor will have a display board to show available parking spots for each spot type. This class will be responsible for displaying the latest availability of free parking spots to the customers.

- *ParkingAttendantPortal:* This class will encapsulate all the operations that an attendant can perform, like scanning tickets and processing payments.

- *CustomerInfoPortal:* This class will encapsulate the info portal that customers use to pay for the parking ticket. Once paid, the info portal will update the ticket to keep track of the payment.

- *ElectricPanel:* Customers will use the electric panels to pay and charge their electric vehicles. They will have the PaymentCalculation class call for paying the charges for charging their vehicle.

# Class Diagram
![ParkingLot](https://user-images.githubusercontent.com/25343984/132120521-24702e5e-f4f4-499c-8d23-fd46110e8204.png)
