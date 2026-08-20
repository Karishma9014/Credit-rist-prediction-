# Credit-rist-prediction-
Credit Risk Prediction is a machine-learning system that predicts whether a loan applicant has low or high credit risk based on factors such as income, loan amount, credit history, and employment details. 
# Credit Risk Prediction

print("=== Credit Risk Prediction System ===")

income = float(input("Enter annual income: "))
loan_amount = float(input("Enter loan amount: "))
credit_score = int(input("Enter credit score: "))
employment_years = int(input("Enter years of employment: "))

# Simple risk calculation
risk_score = 0

if credit_score < 600:
    risk_score += 2
elif credit_score < 700:
    risk_score += 1

if loan_amount > income * 0.5:
    risk_score += 2
elif loan_amount > income * 0.3:
    risk_score += 1

if employment_years < 2:
    risk_score += 1

if risk_score >= 3:
    print("\nResult: HIGH CREDIT RISK")
    print("Loan approval is not recommended.")
else:
    print("\nResult: LOW CREDIT RISK")
    print("Loan approval may be considered.")
