# Megaline Plan Revenue Analysis

## Project Overview
You are an analyst for Megaline, a telecom operator with two prepaid plans: Surf and Ultimate. The goal is to identify which plan generates more revenue so the marketing team can allocate budget more effectively.

The dataset includes 500 users and their 2018 usage activity (calls, messages, and internet sessions), along with plan and user profile information.

## Billing Rules
- Call duration is rounded up per call to the next full minute.
- Internet traffic is summed per month, then rounded up to full gigabytes.
- 1 GB = 1024 MB.

## Plan Details
### Surf
- Monthly fee: $20
- Included: 500 minutes, 50 messages, 15 GB
- Overage:
	- $0.03 per extra minute
	- $0.03 per extra message
	- $10 per extra GB

### Ultimate
- Monthly fee: $70
- Included: 3000 minutes, 1000 messages, 30 GB
- Overage:
	- $0.01 per extra minute
	- $0.01 per extra message
	- $7 per extra GB

## Project Tasks
1. Study the data and check general structure and quality.
2. Prepare the data:
	 - Convert columns to correct data types.
	 - Identify and fix data issues.
	 - Build monthly user-level metrics:
		 - number of calls and total minutes
		 - number of text messages
		 - total internet usage
		 - monthly revenue per user
3. Analyze user behavior by plan:
	 - Compare usage patterns (minutes, messages, data).
	 - Calculate mean, variance, and standard deviation.
	 - Plot and interpret distributions.
4. Test hypotheses:
	 - Average revenue differs between Surf and Ultimate users.
	 - Average revenue differs between NY-NJ users and users from other regions.
	 - Choose and justify significance level ($\alpha$), hypotheses, and test method.
5. Write an overall conclusion.

## Notebook Format
Complete the work in a Jupyter notebook:
- Use code cells for analysis.
- Use markdown cells for explanations.
- Add clear section headings and readable formatting.

## Data Dictionary
### users
- user_id: unique user identifier
- first_name: first name
- last_name: last name
- age: age in years
- reg_date: subscription date
- churn_date: cancellation date (missing means active at extraction time)
- city: city of residence
- plan: plan name

### calls
- id: unique call identifier
- call_date: call date
- duration: call duration (minutes)
- user_id: user identifier

### messages
- id: unique message identifier
- message_date: message date
- user_id: user identifier

### internet
- id: unique session identifier
- mb_used: internet usage per session (MB)
- session_date: session date
- user_id: user identifier

### plans
- plan_name: plan name
- usd_monthly_fee: monthly fee (USD)
- minutes_included: included minutes
- messages_included: included messages
- mb_per_month_included: included internet data (MB)
- usd_per_minute: cost per extra minute
- usd_per_message: cost per extra message
- usd_per_gb: cost per extra GB