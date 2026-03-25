# Online Bus Ticket Booking System

buses = {
    1: {"route": "Chennai to Trichy", "price": 300, "seats": 10},
    2: {"route": "Madurai to Coimbatore", "price": 250, "seats": 8},
    3: {"route": "Salem to Chennai", "price": 200, "seats": 12}
}

print("---- Online Bus Ticket Booking ----")

name = input("Enter your name: ")

print("\nAvailable Buses:")
for key, value in buses.items():
    print(key, value["route"], "- Rs.", value["price"], "| Seats:", value["seats"])

choice = int(input("\nSelect bus number: "))

if choice in buses:
    bus = buses[choice]
    
    seats_needed = int(input("Enter number of seats: "))
    
    if seats_needed <= bus["seats"]:
        total = seats_needed * bus["price"]
        bus["seats"] -= seats_needed
        
        print("\n---- Booking Confirmed ----")
        print("Name:", name)
        print("Route:", bus["route"])
        print("Seats Booked:", seats_needed)
        print("Total Price:", total)
        print("Remaining Seats:", bus["seats"])
    else:
        print("Sorry! Not enough seats available 
    print("Invalid bus choice")

print("\nThank you for using online booking 😊")
