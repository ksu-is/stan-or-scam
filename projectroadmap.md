# Stan or Scam? Project Roadmap

Developer: Christian Greene (solo project)

## Sprint 1
- [x] Choose a project topic and turn in Exercise 6
- [x] Add the project to the Teams Projects spreadsheet
- [x] Join the ksu-is GitHub organization
- [x] Create the stan-or-scam repository with an open source license
- [x] Write README.md with the project overview, features, and goals
- [x] Find a related Python repository, read the code, and try running it (see Codebase Review below)

## Sprint 2 (Christian Greene)
- [ ] Create `red_flags.txt` with scam phrases and a point value for each one
- [ ] Write a `check_message()` function that searches a pasted message for each red flag (using `.lower()` and `in`) and adds up a risk score
- [ ] Print a Stan / Suspicious / Scam verdict along with the list of red flags that were found
- [ ] Add a price check that flags prices far below face value
- [ ] Write 10 sample seller posts (5 that sound legit, 5 scams) and test the checker on all of them

## Sprint 3 (Christian Greene)
- [ ] Create `tour_dates.txt` with official on-sale dates for Megan Thee Stallion and Beyoncé tours and add the "too early" check
- [ ] Build the interface (Tkinter window or Flask page) that shows the verdict and red flags
- [ ] Add next-step tips and the ReportFraud.ftc.gov link to every result
- [ ] Save each checked message and its verdict to a scam log file
- [ ] Update README.md with screenshots and instructions for running the app

## Sprint 1 Codebase Review

**Reference project**
[Ticket Resale Account Risk Screening Tool](https://github.com/Melinda111-F/ticket-resale-risk-screening) by Melinda111-F

**What it does**
A beginner-friendly Python project that screens accounts on a fictional ticket resale marketplace. It reads account activity and follower data from CSV files, flags accounts that behave unusually, and exports the results as CSV files for a Power BI report. It only uses the Python standard library, and all 12 accounts in its data are made up.

**What I reviewed**
- `create_accounts_dictionary()` in `ticket_account_risk.py` reads `data/accounts.csv` one line at a time with `.readline()`, `.strip()`, and `.split(",")`, which is the same file reading we practiced in the Python Fundamentals file module.
- `add_risk_candidate_groups()` is where the rules live. Each rule is one `if` statement, like "sends a lot of messages but has very few listings" or "brand-new account sending a lot of messages." When a rule matches, the rule's name is appended to that account's `risk_groups` list, so the program can explain *why* an account was flagged instead of just saying it is risky.
- `get_quantile()` decides what counts as "high" or "low" by comparing each account to the rest of the dataset (for example, the top 20% of message counts).
- The thresholds, like `P_HIGH_MESSAGES = 0.80` and `NEW_ACCOUNT_DATE`, are kept in a separate `constants.py` file, so the rules can be adjusted without rewriting the main code.
- The README is careful to say the results are "screening indicators," not proof of fraud.

**What happened when I tried to run it**
_Running results will be added here._

**What I plan to use**
- The "one rule = one `if` statement, append the matched rule to a list" design. Stan or Scam? will do the same thing with red-flag phrases, so every verdict comes with a list of reasons.
- Keeping the rules separate from the logic. Their thresholds live in `constants.py`, and my red-flag phrases and point values will live in `red_flags.txt`, so I can add new scam phrases without changing my code.
- The "warning, not proof" approach in their README, which I also included in mine.

**How my project is different**
This project looks at account behavior across a whole marketplace dataset. Stan or Scam? checks the actual text of one post or DM that a fan is about to answer, and it adds a check for tickets being sold before a tour's official on-sale date.
