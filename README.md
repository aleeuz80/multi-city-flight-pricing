# multi city flights: how to price a multi-stop itinerary without overpaying, and where the cashback layer actually stacks

A multi-city search fails in a very specific way. You type in three legs, hit search, and the total that comes back is either higher than three separate one-way fares or mysteriously lower, and nothing in the interface explains which one you're looking at. Same airports, same dates, two different answers depending on whether you searched them together or apart.

Most guides stop at "select multi-city instead of round-trip". That's the easy part. The part that actually costs money is what happens *after* you find the itinerary: which booking site you hand it to, whether the routing rules leave you room to fix a mistake, and whether the price you see is the price you're really paying.

So here's the working version — routing logic, carrier limits, the three things that break a multi-city booking after payment, and the layer almost nobody bothers to add.

## Multi-city is not one thing

Four ticket shapes get lumped together under the same label, and they behave differently when something goes wrong.

| Ticket type | What it is | Where it bites |
| --- | --- | --- |
| Multi-city | One reservation, multiple legs, one confirmation number | Carriers inside the booking can have different change and cancellation rules |
| Open jaw | Fly into city A, return home from city B | You arrange the middle yourself — ground transport or a separate ticket |
| Double open jaw | Different origin and destination in both directions | Two separate ground arrangements to plan |
| Separate one-ways | Independent tickets glued into a trip | No leg voids another, but you pay baggage and rebooking costs per ticket |

Stopovers sit alongside those as a separate mechanic rather than a ticket type. Booking.com's guide draws the line at 24 hours: anything under that is a layover, and anything longer counts as a stopover, with some airlines letting you stretch it to around ten days. Turning a six-hour connection into a two-day city break usually costs nothing extra on the fare itself — you're only paying for the hotel.

Open jaw is worth understanding because it's often the cheapest way to do a multi-city trip that doesn't need a flight in the middle. Fly into Dubrovnik, drive up the Croatian coast, fly home from Zagreb. Skyscanner's own guide notes that open-jaw tickets use the same fare codes as returns, which is why they can undercut two one-ways.

## How many legs each search engine will actually let you add

Leg limits vary more than people expect, and hitting the ceiling mid-plan is a bad moment. From the published limits:

| Where you search | Max legs |
| --- | --- |
| KAYAK | 7 |
| Skyscanner | 6 |
| Trip.com | 6 |
| United Airlines | 6 (across Star Alliance) |
| Lufthansa | 6 |
| Finnair | 6 |
| American Airlines | 4 |
| Cathay Pacific | 4 stops (Hong Kong transits under 12 hours don't count) |
| Emirates | No stated limit |

The practical reason to search on a meta-search engine rather than an airline's own site is coverage. Skyscanner points out that a multi-city search on a single carrier's website only returns that carrier's network, which is a real problem if the airline has no partner at one of your stops. A meta-search can mix a single carrier, an alliance, or carriers with no shared affiliation at all.

## Route shape decides the price more than date flexibility does

Airlines price multi-city itineraries off logical progressions. Finnair is unusually explicit about it: destinations should move forward from each other, and zigzagging — Helsinki to Paris to Berlin to Lisbon — is the thing to avoid. Booking.com's version of the same lesson uses a US example: flying Maine → San Francisco → New York → Arizona → Maine crosses the country twice for no reason. Maine → New York → Arizona → San Francisco → Maine does the same trip in a straight line.

There's a second, less obvious constraint on the Finnair model. Independent connections — legs you cover by train, bus, or a flight on a different booking — each consume one of your six available segments. So a route that looks like four flights on paper can eat your whole allowance once you factor in the overland hops.

Then there's the failure mode. Finnair states plainly that if one flight in the multi-city search isn't available from them or their partners, the entire booking can't be made. That's why the fix when a search returns nothing is almost always to change a city, switch to a nearby airport, or move a date — not to keep hitting search.

## The three things that break after you pay

### Baggage on mixed carriers

This is the quiet one. A multi-city booking can contain a full-service carrier, a codeshare, and a low-cost airline, and each treats bags differently. Trip.com's breakdown of the scenarios is the clearest version of the rules:

| Scenario | Extra baggage cost? |
| --- | --- |
| Same airline, one ticket | Usually no — standard allowance covers all legs |
| Different airlines, one booking | Maybe — the "most significant carrier" rule usually decides |
| Full-service plus budget mix (e.g. Qantas + Jetstar) | Likely — budget carriers charge per segment |
| Separate tickets per city | Yes — you pay on every segment |
| International plus domestic legs | Depends — domestic limits are often stricter |
| Carrier change mid-route | Recheck the limits for each airline in the chain |

### One missed leg can wipe the rest

Skyscanner flags this directly: if you miss one flight, the remainder of the itinerary can be voided. That's the argument for generous connection windows on a multi-city booking, even when a tighter one prices better. KAYAK's stopover-duration filter exists partly for this — you can deliberately look for longer connections rather than being handed 55-minute ones.

### Policy drift inside a single booking

A booking spanning three airlines has three sets of change and cancellation rules. Finnair notes that the ticket type you pick has to apply across every flight, and if your chosen fare isn't available on one leg, you get moved to the nearest alternative. You also check in separately for each flight rather than once for the trip.

The upside of a single reservation is worth stating: one confirmation number, checked baggage usually tagged through to your final destination, and — per Trip.com's guide — if your first flight is delayed, the airline is on the hook to rebook your connection. On separate one-way tickets, that protection doesn't exist.

## Where the booking site choice actually matters

Here's the part the route guides skip. Once the itinerary is set, the same flights are priced differently across online travel agencies on any given day, and the difference is invisible if you only look at one site. That's normal price dispersion, not a trick.

Which is where the cashback layer enters, and why it belongs in a conversation about multi-city flights specifically. Multi-city itineraries are expensive by definition — more legs, more fare — and cashback percentages that look trivial on a $60 purchase stop looking trivial on a $1,200 booking.

ShopBack is a cashback platform that launched in Singapore in 2014 and now operates across 13 markets including Australia, Singapore, Malaysia, Indonesia, the Philippines, Thailand, Taiwan, Vietnam, South Korea, and the US. Per its corporate figures, it has 20M+ active members, 20K brand partners, and has paid out over US$900M in cashback. Membership is free — there's no paid tier to buy. You click through from ShopBack to a participating merchant before you book, and a share of the merchant's affiliate commission comes back to you as cash.

For flights, the relevant surface is Travel Planner, which puts live OTA prices side by side and displays the cashback you'd earn next to each result, along with the effective price after cashback. There's also a paste-a-link check: if you've already found a fare somewhere, you can drop the URL in and see the cashback rate on that exact product without re-entering the search.

Three honest limits before you build a plan around it:

- **Complex multi-leg itineraries are not its strong suit.** Travel Planner is built around round-trip and one-way searches. ShopBack's own comparison against Google Flights concedes that for a genuinely complicated multi-leg trip, a dedicated flight search interface may be more straightforward. Use the flight search engine to *find* the routing; use the cashback layer to *book* it at the same OTA price plus cash back.
- **Award and miles redemptions don't earn cashback.** If you're spending points, this layer doesn't apply.
- **Rates move, and they differ by market.** Flight cashback runs lower than hotel cashback because of how OTA margins work on airfare. ShopBack's US figures put domestic flights at roughly 1.5–3% and international at 3–6% depending on the booking site, with Trip.com flights typically 1.5–5% for US members. Other markets have their own rate cards and their own flash promotions. Check the merchant page in your account on the day you book rather than trusting any percentage in an article, including this one. On a $1,200 fare, 3.5% is $42 — real, but it's a layer on top of a good booking, not a reason to accept a worse one.

👉 [Sign up free and check the current flight cashback rates in your market](https://bit.ly/ShopbacK)

## What the account actually gets you

There's no subscription, no tier ladder, no card to apply for. Here's the complete set of access options:

| Access option | What it covers | Cost | Notes |
| --- | --- | --- | --- |
| Free account (web + iOS/Android app) | Cashback across all partner merchants | Free | The only account type that exists |
| Travel Planner (flights, stays, activities, cars) | Side-by-side OTA pricing with cashback per result | Free | Launch date 14 July 2026; no membership or subscription required |
| Browser extension / in-app browser | Cashback activation and coupon reminders at checkout | Free | The most reliable way to avoid a broken tracking session |
| Paste-link cashback check | Cashback rate for an OTA product you already found | Free | Useful when you've done the research elsewhere |
| Referral programme | Bonus for you and the person you refer | Free | Both sides need to meet the conditions — see below |
| Withdrawal | PayPal or bank transfer | Free | Requires confirmed cashback and the market's minimum threshold |

👉 [Open the free account and find the travel merchants available where you live](https://bit.ly/ShopbacK)

### What you book through, per market

The integrated OTA set is not identical everywhere, and it changes. As of the September 2026 US update, Travel Planner's confirmed integrations for US members are Trip.com for flights and stays, Pelago for activities, and Dida for hotel inventory. Other markets in Asia-Pacific and Australia route through a broader set that includes Booking.com, Agoda, Klook, and Hotels.com via the individual merchant pages rather than the Planner. Either way, the mechanic is the same: a tracked click, the OTA's normal price, cashback on top.

## If you sign up through a referral link

A referral link carries a code with it, so the account gets attributed to whoever shared it. On the ShopBack side, the terms are specific: the referred account needs to sign up through the link or enter the code, make a valid purchase (the help documentation cites a $5 minimum spend), and add withdrawal details within 180 days of creating the account. Bonuses unlock once the cashback on that purchase moves to Confirmed, and both sides need their payout details set.

Two conditions worth knowing about in advance. The first purchase can't be stacked with other new-customer promotions. Self-referral is prohibited, and so is posting a referral link on a merchant's own page. Bonus amounts vary by market and campaign, so the figure you see at signup is the one that counts.

👉 [Use this link to start the account with the referral attached](https://bit.ly/ShopbacK)

## Routes worth pricing as one itinerary

These come from published route examples rather than anything invented:

- **San Francisco → London → Paris → Lisbon → San Francisco** — all forward-moving, no backtracking, one carrier mix.
- **New York → Tokyo → Hong Kong → New York** — a classic three-city Asia loop on a single booking.
- **Kuala Lumpur → Tokyo → New York → London → Kuala Lumpur** — five legs, inside the six-leg ceiling at most engines.
- **Las Vegas → Honolulu → San Francisco** — short-hop version for a US-only trip.
- **Maine → New York → Arizona → San Francisco → Maine** — the Booking.com example of what "logical route" means in practice.

Run each of these twice: once as a multi-city search, once as separate one-ways. Skyscanner's guide is upfront that the combined booking often wins, but not always — and the only way to know is to price both.

## Cashback on flights: what to expect and how to keep it

Booking timing is where most cashback on travel quietly dies. The chain is: tracked click, affiliate cookie, then a confirmation ping from the merchant when the booking completes. Break any link and the cashback doesn't appear.

Things that break it, per ShopBack's own documentation:

- Visiting another coupon or referral site between the click-through and checkout
- Applying a promo code from outside ShopBack — external codes can carry their own attribution and override the referral
- Ad blockers and strict tracking protection, which can block the cookie or the confirmation ping
- In-app browsers — the mini browser inside a social or messaging app often drops the cookie
- Leaving the tracked session and coming back later

Then the timeline. An order usually shows as Tracked within 48 hours. Pending means the merchant's return window is still open. Confirmed means the merchant has verified it — retail confirms in 30 to 90 days, while travel confirms after the trip. Flight cashback typically clears to Confirmed around 60 to 90 days after the travel date, which is normal across every affiliate cashback platform and not a sign that something went wrong.

If a qualifying booking hasn't appeared as Tracked within 48 hours, file a missing cashback claim with the order number, date, and amount rather than waiting on it.

## Questions that come up every time

**Is a multi-city ticket always cheaper than separate one-ways?**
No. It often is, which is why it's worth checking, but the price depends on your route and the carriers available. Price both before booking.

**How do I know the multi-city search will even work?**
If a search returns nothing, the cause is usually one unavailable leg rather than the whole route. Change a city, try a nearby airport, or shift a date, then search again.

**Is multi-city the same as open jaw?**
No. Multi-city includes every flight in one reservation. Open jaw skips the middle — you fly into one city and home from another, and arrange the space between yourself.

**Does cashback apply to multi-city bookings?**
The cashback is calculated on the OTA's commission, not on the route structure, so a multi-city booking through a participating OTA over a tracked link earns the same way a round-trip does. Merge two bookings that could be one, though, and you may split the commission across two smaller payouts — not a reason to avoid it, just don't expect the percentages to be identical on each half.

**Why didn't my flight cashback track?**
The usual causes are booking inside the merchant's app instead of via the tracked click, using an outside coupon code, clearing cookies mid-session, or running an ad blocker or privacy extension at checkout.

**Can I stack cashback with airline miles and card rewards?**
Yes, in most cases. Cashback comes out of the merchant's marketing budget at the affiliate layer, card rewards come from interchange at the issuer layer, and airline loyalty comes from the carrier. Three separate funding sources on one purchase.

## Before you hit book

Write the route out in order and delete any leg that moves backwards. Check how many segments your overland hops will consume. Search multi-city on a meta-search first, then price the same route as separate one-ways to see which wins. Look at the baggage rules for every carrier in the chain, not just the first one. Keep your connections loose enough that a delay doesn't void the rest of the trip.

Then, before you pay, route the booking through a tracked click on the OTA you've already decided on. Same price, same itinerary, and 2–5% of a multi-city fare back in your account after the trip.

👉 [Compare flight cashback rates and book the itinerary through ShopBack](https://bit.ly/ShopbacK)
