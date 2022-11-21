# OOP-classDiagram

# Class - Object - Abstract - Encapsulation - Inheritance - Polymorphase

               - Class 
                        A blueprint/template of object. All the objects share the same attributes + function/methods
               - Object 
                        Real entities and an instance of a class. Has certain attributes + methods
               - Abstract 
                        hide
               - Encapsulation 
                        Wrap all the coding + data together into a single unit, hide from developers, so developers can focus more on the coding. 
                        Not direct access to the method inside
                        Reduce the repitition.
               - Inheritance 
                        Build a new class by using the same attributes or methods of existing class.(extends)
               - Polymorphase
                        Use the same function/methods by through different forms.
                        
        OOP   面对对象编程。
              其实就是看这个软件会影响哪些实体对象（object），然后实体对象归一个类（class），然后用编程展示它们的关系，变成coding
              
        常见Design：
                Case Diagram:
                        实际就是看涉及哪些实体对象，以及他们的行为。
                        常见对象：clients， admin，system + front desk。
                                clients：register/login，search， order/booking， checkout-payment，cancel，seats，numbers of clients， cities， from -  to， date
                                admin：modify time， modify flight/movie， availability， cancel
                                system：notifications- payment， updates，discount，booking， cancel
                                front desk： = clients （）
                        
                Class Diagram：
                        常见class如下，而相应的代码则见最下面的code
                        Account：
                        Payment：
                        Booking：
                        Notification：
                        
                Sequence Diagram
                Activities Diagram


Code

        class FlightStatus(Enum):
          ACTIVE, SCHEDULED, DELAYED, DEPARTED, LANDED, IN_AIR, ARRIVED, CANCELLED, DIVERTED, UNKNOWN = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10


        class PaymentStatus(Enum):
          UNPAID, PENDING, COMPLETED, FILLED, DECLINED, CANCELLED, ABANDONED, SETTLING, SETTLED, REFUNDED = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10


        class ReservationStatus(Enum):
          REQUESTED, PENDING, CONFIRMED, CHECKED_IN, CANCELLED, ABANDONED = 1, 2, 3, 4, 5, 6


        class SeatClass(Enum):
          ECONOMY, ECONOMY_PLUS, PREFERRED_ECONOMY, BUSINESS, FIRST_CLASS = 1, 2, 3, 4, 5


        class SeatType(Enum):
          REGULAR, ACCESSIBLE, EMERGENCY_EXIT, EXTRA_LEG_ROOM = 1, 2, 3, 4, 5


        class AccountStatus(Enum):
          ACTIVE, CLOSED, CANCELED, BLACKLISTED, BLOCKED = 1, 2, 3, 4, 5, 6


        class Address:
          def __init__(self, street, city, state, zip_code, country):
            self.__street_address = street
            self.__city = city
            self.__state = state
            self.__zip_code = zip_code
            self.__country = country
