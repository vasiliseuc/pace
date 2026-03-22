# Pace 🟢

**Pace** is a lightweight, purpose-built billing and workflow dashboard designed specifically for accounting, bookkeeping, and professional service firms. 

It allows non-technical staff to visually track monthly work progress and manually trigger pre-authorized client payments with a single click. No accounting jargon, no complex ledgers, and no chasing clients for credit card numbers—just a steady pace of work and cash flow.

## 📖 The Problem

Many accounting firms fall into a predictable cash flow trap: they complete the hard work for their clients on time, but collecting the payment is a disconnected, manual nightmare. 
* Sending invoices relies on the client actually opening the email and typing in their credit card details.
* Automatically charging clients on the 1st of the month causes friction if the accounting work was delayed because the client was late providing documents. 
* Standard accounting software is often cluttered with jargon ("Accounts Receivable," "Reconciliation") that non-technical staff find intimidating or confusing to navigate just to see who owes what.

## 💡 The Solution: "Bill on Completion"

Pace bridges the gap between doing the work and getting paid by introducing a strict **"Card on File" + "Manual Trigger"** workflow. 

It separates the *authorization* of the payment from the *actual charge*. Clients securely provide their payment info once during onboarding (via Stripe). Then, the accounting staff holds the trigger. They only push the button to collect the money when the specific month's work is actually finished.

### Core Features

* **The "Traffic Light" Board:** The UI is stripped of all spreadsheets and menus. Instead, it uses a visual, card-based grid. Each client has a timeline of the year (Jan - Dec). Staff simply manage the colors:
  * ⚪ **Grey (Not Started):** Work hasn't begun.
  * 🔵 **Blue (In Progress):** The accountant is actively working. This signals to the team that the month is spoken for, but cannot be billed yet.
  * 🟡 **Yellow (Ready to Bill):** The work is finished. This is the visual hook that draws the user's eye to unpaid, completed work. 
  * 🟢 **Green (Paid):** The card was successfully charged.
  * 🔴 **Red (Action Needed):** A payment failed (e.g., expired card) or the client is blocking progress.
* **Frictionless "One-Click" Collection:** When an accountant turns a month Yellow, they don't have to draft an invoice. They simply click the Yellow circle, add an optional internal note (e.g., *"Waiting on final bank statement"*), and click **"Charge Card on File."** Pace instantly communicates with Stripe to process the payment.
* **Zero Technical Overhead:** Built specifically for non-technical office staff. If an employee knows how to match colors, they know exactly how to manage the firm's cash flow.

## 🏗️ Technical Philosophy
Pace is built to be fast, portable, and incredibly cheap to host. It actively avoids heavy, complex frontend frameworks (like React or Angular) in favor of a classic, Server-Side Rendered (SSR) approach using Node.js, Express, and EJS. 

By utilizing a local SQLite database, the app requires zero external database provisioning, meaning you can clone this repository, run `npm install`, and have a fully functioning, secure billing portal running locally in seconds.
