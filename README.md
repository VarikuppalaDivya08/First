def find_class(branch, year, section):
    # Mini database of classroom details
    class_info = {
        ("CSE", 1, "A"): "South Block - Room G0 (Gnd Floor)",
        ("CSE", 1, "B"): "South Block - Room 106 (1st Floor)",
        ("ECE", 1, "A"): "North Block  - Room 111 (1st Floor)",
        ("ECE", 1, "B"): "North Block - Room 211 (2nd Floor)",
        ("EEE", 1,"A"): "North Block - Room G12 (Gnd Floor)",
        ("IT", 1, "A"): " South Block - Room 205 (2nd Floor)",
        ("IT", 1, "B"): "South Block - Room 305 (3rd Floor)",
        ("CSM", 1, "A"): "North Block  - Room 311 (3rd Floor)"
    }

    key = (branch.upper(), year, section.upper())
    return class_info.get(key, "No data found! Please contact admin.")

def main():
    print("🎓 Welcome to Campus Helper System 🎓")
    branch = input("Enter your Branch (CSE/ECE/EEE/IT): ")
    year = int(input("Enter your Year (1/2/3/4): "))
    section = input("Enter your Section (A/B/C): ")

    location = find_class(branch, year, section)
    print(f"\n👉 Your class is in: {location}")

if __name__ == "__main__":
    main()