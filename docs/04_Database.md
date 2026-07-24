# MoneyManager Database Design

## Purpose

The database is the brain of MoneyManager.

It stores all financial information safely so the user can access it anytime, even while offline.

---

# User Model

MoneyManager is designed for one person per app installation.

Each installation represents one complete financial world.

Security is prioritised using local PIN protection.

---

# Main Data Structure

The application stores the following information.

---

## User Settings

Stores:

- Main currency
- Theme
- Security PIN
- Notification preferences
- Language

---

## Accounts

Users create their own accounts.

Each account contains:

- Account Name
- Account Type
- Currency
- Opening Balance
- Current Balance
- Include in Available Spending Money (Yes/No)

Examples:

- Cash Wallet
- QNB Salary Card
- M-Pesa
- Emergency Savings
- Etica Wallet
- Crypto Wallet

---

## Transactions

Each transaction stores:

- Income or Expense
- Amount
- Category
- Account
- Date
- Time
- Note
- Description
- Receipt Image (optional)

Transactions can be edited.

Deleting a transaction requires user confirmation.

---

## Categories

Default examples:

- Food
- Transport
- Shopping
- Salary
- Rent
- Entertainment
- Healthcare
- Education
- Other

Users may create their own categories.

---

## Savings Goals

Stores:

- Goal Name
- Target Amount
- Current Progress
- Deadline
- Status

Examples:

- New Phone
- Emergency Fund
- Vacation

---

## IOUs

Tracks money borrowed or lent.

Stores:

- Person Name
- Amount
- Date
- Due Date
- Status
- Notes

---

## Subscriptions

Stores recurring payments.

Examples:

- Netflix
- Spotify
- Gym
- Mobile Data

Each subscription stores:

- Amount
- Frequency
- Next Payment Date
- Reminder

---

## Currency System

The user selects one main currency.

Examples:

QAR
KES
USD
EUR

Other account currencies are automatically converted for display.

The original currency value is always preserved.

---

## Financial Forecast

Future calculations include:

- Upcoming bills
- Subscriptions
- Planned expenses
- Savings goals

The app calculates:

Safe-to-Spend Amount

---

# Privacy

Sensitive information is protected.

Examples:

- Total Wealth hidden by default.
- PIN required to reveal protected balances.

---

# Future Expansion

The database is designed to support:

- AI Financial Coach
- Smart reminders
- Receipt scanning
- Cloud backup
- Multi-device synchronisation (future)