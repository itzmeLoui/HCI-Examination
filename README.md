def gps_tracker():
    # Starting position
    x, y = 0, 0
    print("Starting position: (0, 0)")

    while True:
        command = input("Enter direction (N/S/E/W) or STOP to end: ").strip().lower()

        if command == "stop":
            break
        elif command in ["n", "north"]:
            y += 1
        elif command in ["s", "south"]:
            y -= 1
        elif command in ["e", "east"]:
            x += 1
        elif command in ["w", "west"]:
            x -= 1
        else:
            print("Invalid input! Please enter N, S, E, W, or STOP.")
            continue

        print(f"Current position: ({x}, {y})")

    # Session ends
    print(f"\nFinal position: ({x}, {y})")
    if (x, y) == (0, 0):
        print("You returned to the origin (0, 0).")
    else:
        print("You did NOT return to the origin.")

# Run the GPS tracker
gps_tracker()
