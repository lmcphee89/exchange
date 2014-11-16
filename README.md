ness Requirements Document for the FXExchange project.

Developers: 0 Recruitment Consultants: 0 Men who love women easily and passionately: 2

Overview: The purpose of the project is to build a low-latency exchange for FX. Ideally, the project will employ the LMAX Disrutor pattern to achieve high performance and will be able to scale both vertically and horizontally - with several processes capable of being run, potentially to provide resilliency or an increase in performance. If the project is successful then the framework will be applied to other securities - so some element of generality will be appreciated.

Functional Requirements:

Exchange must be able to accept messages (format TBD, though likely FIX), verify action and carry out corresponding action.

Exchange must be able to keep track of all trades currently on the order book.

Exchange must be capable of resuming from previous position in the case of an crash.

Exchange must be able to process both limit and market orders.

Exchange must be able to keep track of day prices including: current average price, day average price, last buy price, day high price, day low price, last trade price, last trade volume, and day trade volume.

Exchange must be able to handle clients buying, selling, cancelling orders and amending orders.

Exchange must persist all historical trades - in case of regulator request.

Non-functional requirements:

Latency: The time taken between an order being received at the system input to the response being returned to the client must be less than 5 ms for 99.9% of trades. This includes situations where the order is matched with an order currently on the market, submitted to the market, amended or cancelled.

Throughput: The system must be able to process 30000 trades per second - though this may be reviewed given the hardware the system shall run on.

Throughput will be measured in terms of average throughput per second for every 1000 messages from the clients. Once more, 99.9% of throughput figures should meet the requirement.

