# Stan or Scam? 🚨

A ticket scam checker that protects Megan Thee Stallion and Beyoncé fans.

## Project Overview

Stan or Scam? is a Python app that helps fans figure out if a ticket seller is real before they send any money. A fan pastes in a seller's post, comment, or DM, and the app scans it for scam red flags, gives it a risk score, and explains in plain language why it might be a scam and what to do next.

I came up with this idea because every big tour brings ticket scammers with it. In February 2025, Ticketmaster warned Beyoncé fans that scammers were already selling "tickets" to the Cowboy Carter Tour before tickets had even gone on sale ([FOX 5 Atlanta](https://www.fox5atlanta.com/news/beyonce-ticket-scam-fans-cowboy-carter-alert-ticketmaster)). Fans are so excited to see their favorite artist that they miss the warning signs, and money sent through payment apps can be very hard to get back.

## Planned Features

- **Paste and check.** The fan pastes in the seller's message and the asking price.
- **Red flag scanner.** The app searches the message for warning signs like "Cash App or Zelle only," "friends and family payment," "act fast," PDF or screenshot tickets, "selling for a friend," or asking to move the chat to another app.
- **"Too early" tour check.** The app stores official on-sale dates for upcoming tours, starting with Megan Thee Stallion and Beyoncé, and flags anyone selling tickets before they were actually released.
- **Risk score and verdict.** Each red flag adds points, and the app gives a final verdict: **Stan** (low risk), **Suspicious**, or **Scam** (likely scam).
- **Plain-language explanation.** The app shows which phrases raised a red flag and why, then gives next steps, like buying through official resale and reporting scammers at [ReportFraud.ftc.gov](https://reportfraud.ftc.gov/).
- **Scam log.** Checked messages are saved so fans can look back at known scam wording.

## Example

A fan sees this post on X: *"2 Beyoncé floor seats $80 each!! Cash App only, first come first serve, DM me fast"*. They paste it into Stan or Scam?. The app flags "Cash App only," "first come first serve," and a price far below face value, gives it a **Scam** verdict, and tells the fan to buy through official resale instead.

## Technology

- Python 3
- String methods, lists, loops, if/elif statements, and functions to scan messages and add up the risk score
- Text files to store the red-flag phrases and tour on-sale dates
- Tkinter or Flask for the interface
- GitHub for version control

## Project Goals

The first version will be a text-based checker: paste in a message, and the program prints a risk score, a Stan / Suspicious / Scam verdict, and the red flags it found. After that, I'll add the "too early" tour date check, build the interface, and add the scam log. If time allows, I'll let users add their own red flags and artists.

**Disclaimer:** Stan or Scam? gives warnings, not guarantees. A low score does not mean a seller is safe, so fans should still buy through official sellers whenever they can.

## Project Developer

Christian Greene
Individual project for Application Development I (IS 3020), Kennesaw State University
