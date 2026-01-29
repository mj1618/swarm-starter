We're makinga prediction market called Contrary Markets. Your goal is to write tasks to implement the whole prediction market and write the tasks to "todo/*.pending.md" and then exit immediately.

The tech stack is NextJS, Typescript, Tailwind and Convex.dev for the backend.

Import relevant information from the web to understand prediction markets better.

The features of the platform include:

## Main design decisions

There will be two currencies on the site - Contrary-Coins and Real Money.
The user can toggle between the two at the top of the screen.
The markets only every show one or the other, never a combination.
Don't implement real-money purchase/redemptions yet, that is coming later, but allow people to deposit however much fake money they like.
In a prediction market, "yes" and "no" shares always add up to $1.
Make the style look modern and it should have both light and dark mode with a toggle for the user.

## Main Page

- a main page where users can see all the markets
- filter down to what they market they're looking for

## Market page

- a page where you go into a market and see everything and trade.
- it has a graph of the change in price over time.
- the market has a description
- you can trade (buy/sell) using the following order methods: Market, Limit, Merge, Split
- show the order book for yes and no shares - show the current order book of all open trades for both sides of the market.
- comments from users and allow logged-in users to post new comments
- click through on the users to see their profile

## View user page

- you can view any other user by clicking on their profile
- you can see all the trades they made or are trying to make, and all trades that got cancelled

## sign in/up

- use convex-auth to allow sign ins and ups
- each user has their own wallet
- don't implement payments, simply allow the user to deposit any number of fake coins

## Leaderboard

- the leaderboard is also toggle-able between real and fake coins
- you can select: today, weekly, monthly, all time
- you can select: category
- you can select: top profit/loss or top volume traded
- it shows you profit/loss and volume traded
- pagination to see the rest of the users, only show 100 per page.