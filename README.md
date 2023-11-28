def calculate_bmi(weight, height):
    # BMI formula: weight (kg) / (height (m) * height (m))
    bmi = weight / (height ** 2)
    return bmi

def interpret_bmi(bmi):
    if bmi < 18.5:
        return "Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Normal Weight"
    elif 25 <= bmi < 29.9:
        return "Overweight"
    else:
        return "Obese"

# Get user input for weight and height
weight = float(input("Enter your weight in kilograms: "))
height = float(input("Enter your height in meters: "))

# Calculate BMI
bmi = calculate_bmi(weight, height)

# Interpret and display the result
interpretation = interpret_bmi(bmi)
print(f"Your BMI is: {bmi:.2f}")
print(f"Interpretation: {interpretation}")
