# DC Generator Calculator Using Python

print("DC GENERATOR CALCULATOR")
print("-----------------------")

print("1. Calculate Generated EMF")
print("2. Calculate Electrical Power")
print("3. Calculate Efficiency")

choice = int(input("\nEnter your choice (1-3): "))

if choice == 1:
    P = float(input("Enter number of poles (P): "))
    Phi = float(input("Enter flux per pole (Wb): "))
    Z = float(input("Enter total armature conductors (Z): "))
    N = float(input("Enter speed (RPM): "))

    print("\n1. Lap winding")
    print("2. Wave winding")
    winding = int(input("Select winding type: "))

    if winding == 1:
        A = P
    elif winding == 2:
        A = 2
    else:
        print("Invalid winding type!")
        exit()

    Eg = (P * Phi * Z * N) / (60 * A)

    print("\nGenerated EMF =", round(Eg, 2), "V")

elif choice == 2:
    voltage = float(input("Enter terminal voltage (V): "))
    current = float(input("Enter load current (A): "))

    power = voltage * current

    print("\nElectrical# generators