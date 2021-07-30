## Basic Guide for Sniping (Beginners)
This is a guide for beginners on Minecraft name sniping, written by yours truly, unslow.

A name sniper is a program written in a computer language which attempts to "snipe" a name the instant it becomes freed up from the previous owner. Not to be confused with actual gun snipers. 

This guide covers the most essential and fundamental topics beginners should be know before / during sniping.

-------------------------------------------

## I. Name Changes

After a person changes their name, the API stores the exact time the user changed to a different username. For example:

```sh
JohnSmith2 7/30/2021 @ 3:24:19 PM
JohnSmith (First name)
```

The data is generally in unix time format. 3:24:19 PM would be stored as `1627683859`

So the Mojang API has the information when the person changed their name. Then, NameMC detects this change and automatically assumes the username will be available 37 days from the original name change. 30 days to account for the user's name change cooldown, and 7 days for the grace period the name is available for the previous owner only.

Most snipers locate the drop time for a name via NameMC's API. In some cases though, people in the community have their own APIs for the drop time. 

## II. Introduction

A sniper, or sniping program, sends "name change" requests as soon as the name is available.
These name change requests are the same things you send when you press the name change button on minecraft.net. The only difference is the bot does it much more precisely than a human can, sends 2 requests instead of one, and sends feedback (time stamps) when exactly the requests were received.

## III. Benefits

 Here are the advantages you gain from using an automated sniping program:

- Feedback on the time the requests were registered 
- Ability to send more requests in a shorter time span than was previously available (hand sniping)
- Ability to use more than 1 account per snipe, which provides you a ginormous advantage if supplied with great amounts
- Automation; the sniper will still snipe even if you aren't around, or even awake. You can rely on it doing the job for you so you don't have to wake up an 3 AM just to attempt a snipe.
## IV. Credibility
 
Snipers are created by other community members with expertise in coding languages. They are constantly updating the snipers, so errors and other complications minimize over time. You can trust their works as the source code is made public, so you're aware of every bit of the machine you're using. In addition, the sniping community has garnered thousands of people in its lifetime, all of which are able to prove the credibility of the sniper

## V. Types of snipers

Snipers can be paid or free. The two recommended free snipers, [Smart-Sniper](https://github.com/snipesmarter/smart-sniper) and [MCSniperPY](https://mcsniperpy.com), are amazing snipers to begin your journey with; a large supportive community, constant updates, and a consistent bot allowing you to perfect your delay. Once you are much more experienced at sniping, using larger amounts of accounts with a paid sniper will allow you to snipe highly sough-after names. 

Most experienced snipers use Minecraft giftcards (abbreviated as `GCs`) to snipe. `GCs` have the capability of sending 6 name change requests instead of 2 (which is the standard for any regular Mojang or Microsoft account.)
Because of this, 1 `GC` equates to 3 regular accounts. Experienced snipers then require less accounts for a greater chance of beating others. Furthermore, giftcards have their own endpoint, so their name change requests are priotized over Mojang and Microsoft accounts.*

**Subject to confirmation and revision*

## VI. Sniping as a User
 
So how does the sniper work, from a user's perspective? Well, you put in the account credentials to the account(s) you want to use, it fetches the authorization token, which allows it the permission to change your username. Then, you input the name you want to snipe, the delay (which will be covered later on) you want to use, and in some snipers, you are able to select what account type you are using (Mojang, Microsoft, Giftcard, etc.)
## VII. Factors in sniping
 
There are a few factors in sniping: accounts in use, your delay / timing, and luck. Usually suppling more accounts and bettering your timing will outweigh your luck, meaning you have a much higher chance at being successful. 
Number of accounts is self explanatory. More accounts, more requests, higher probability.

Delay is a system where you enter how many milliseconds off the droptime you want it to start sending requests. For example, someone has 0 ping so the requests (with 0 delay) would normally send at `xx:xx:xx.000000`. 
If we were to work off the example above with JohnSmith, the name becomes available at 3:24:19 PM. Your sniper would normally send requests are that exact time, `3:24:19.0000`. However, some names drop later than usual due to API lag and other factors. Because of this, you may miss the snipe (for being too early) if your delay is 0. 
Most snipers advise getting timestamps with `xx.095` - `xx.100` as they seem to have the greatest likelihood of success. 

## VIII. Delay

So if we want to dive into delay deeper, first I have to explain time stamps; the most fundamental mechanic of delay, as it is the foundation for what changes you make to your delay in order to perfect it.
Using the aforementioned example again, lets say your requests land at `3:24:19.230` and `3:24:19.300`
As you want to have them land at `3:24:19.095` and `3:24:19.100`, you will need to increase your delay here so the sniper shoots sooner.
First let's zoom up and disregard any numbers which aren't necessary for calculating the optimal delay change for this situation:
(The two requests sent) `...19.230` `...19.300`
You are **~130 milliseconds** off the best timestamp range with the first request. The second request is **~200 milliseconds** off. It may be best to change according to the second one, so your second request lands at `...19.100` with the first sometime before that.
Add `200` delay. If your delay before was, for example, `129`, adjust to `329` delay on your next snipe.
After that, analyze the results. Were they closer to the recommended timestamps? How far, if not precisely on it? Make more changes until your timestamps are on target, or, until you notice you successfully sniping names at another timestamp.

## IX. Time synchronization

Another way to make your timestamps accurate is by using a time synchronization program. This sets your computer's clock to the closest time possible to xx.000. If your time is always consistent, then your delay and timestamps will be consistent for every snipe you use it. What I mean is; normally if you use, say, 300 delay- sometimes you may get timestamps on xx.218 and other times on xx.113. This is because your computer's clock isn't the same every time you sniped with that delay. If you use a time synchronization program such as Dimension 4, your timestamps with 300 delay will usually if not always be the same... such as xx.113 (every time) in this example.

## X. Sniping jargon

In sniping there are terms and phrases which are usually shortened versions of their longer counterparts. Below are a few that you may run in to:
|What it means | What is usually said instead |
| -------------| ---------------------------|
|NFA | Non-full access|
|Semi-full access account| SFA |
| Full access account | FA |
| Mail full access account | MFA |
| Unmigrated full access account | UFA |
| Account with no name set, blank name, giftcard| GC|
| Little kids with no coding knowledge who steal other snipers, change it, and claim ownership of it. Basically, stupid. | Skid | 
| The time at which a username is available, after the 37 day period of waiting | Droptime |

Now I will explain what each of these is used for in particular.

**SFA** - Semi-full access account. The name comes from the amount of access you have to it; not very much. You only have the credentials for the Minecraft account, but no access to the email tied to the account. Because you require email access to change the email and add security questions, it's locked on the email which it's currently on.

SFAs are usually frowned upon as they are (usually) obtained from unorthodox methods, and are used solely for practicing / testing delay and other stuff. Typically, if they are used when trying to snipe a valuable name, the name goes to waste as the original owner of the account returns and likely changes off the name. 

## XI. Conclusion

As described throughout this introductory statement, snipers have many advantages when used in comparison to traditional hand-sniping. It may be complicated or daunting at first, but after a few weeks or months it becomes a lot easier to understand.
Don't hesitate to reach out to other server members in sniping servers. Some may be willing to help you.
If you don't want to commit yourself to sniping, there is no urgency to do so. You can try hand-sniping still, but I will warn you it will likely yield little results.
All in all I hope you have an amazing time sniping and wish you luck along your journey!
