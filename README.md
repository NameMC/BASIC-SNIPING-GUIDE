```
███╗   ███╗ ██████╗    ███████╗███╗   ██╗██╗██████╗ ██╗███╗   ██╗ ██████╗ 
████╗ ████║██╔════╝    ██╔════╝████╗  ██║██║██╔══██╗██║████╗  ██║██╔════╝ 
██╔████╔██║██║         ███████╗██╔██╗ ██║██║██████╔╝██║██╔██╗ ██║██║  ███╗
██║╚██╔╝██║██║         ╚════██║██║╚██╗██║██║██╔═══╝ ██║██║╚██╗██║██║   ██║
██║ ╚═╝ ██║╚██████╗    ███████║██║ ╚████║██║██║     ██║██║ ╚████║╚██████╔╝
╚═╝     ╚═╝ ╚═════╝    ╚══════╝╚═╝  ╚═══╝╚═╝╚═╝     ╚═╝╚═╝  ╚═══╝ ╚═════╝ 
```


# **Basic Guide for Sniping (Beginners)**

This is a guide for beginners on Minecraft name sniping, written by yours truly, unslow.

A name sniper is a program written in a computer language which attempts to claim a name the instant it becomes freed up from the previous owner. 

This guide covers the most essential and fundamental topics beginners should know before / during sniping.

-------------------------------------------

# **I. Name Changes: Behind the Scenes**

After a person changes their name, the API stores the exact time the user changed to a different username. For example:

```sh
JohnSmith2 7/30/2021 @ 3:24:19 PM
-----------------------------------
JohnSmith (First name)
```

The data is generally in unix time format. `July 30th, 2021 @ 3:24:19 PM` would be stored as `1627683859`

The Mojang API has the exact time a person changes their name. NameMC then detects this change and automatically assumes the username will be available 37 days after the original name change. 30 days to account for the user's name change cooldown, then an additional 7 days for the owner to decide whether they want to reclaim the name or to discard it.

Most snipers locate the drop time for a name via NameMC's API. In some cases though, people in the community have their own APIs for the drop time which some snipers utilize.

# **II. Introduction**

A sniper, or sniping program, sends "name change" requests as soon as the name is available.
These name change requests match the ones you send when you change your name on [minecraft.net](https://www.minecraft.net/en-us). The only difference is the bot does it much more precisely than a human can, sends 2 requests instead of one, and sends feedback (timestamps) when exactly the requests were received by Mojang's servers.

# **III. Benefits**

 Here are the advantages you gain from using an automated sniping program:

- Timestamps of when the requests were received by Mojang's servers.
- Ability to send more requests in a shorter time span than other methods
- Allows you to use more than 1 account per snipe
- The sniper will continue to snipe even if you aren't around, or even awake. All that's necessary is keeping your device online.

# **IV. Credibility**
 
Snipers are created by Minecraft sniping community members with expertise in coding languages. They are constantly updating the snipers, so errors and other complications are decreasing over time. You can trust their works as the source code is made public, so you're aware of every bit of the machine you're using. In addition, the sniping community has garnered thousands of people in its lifetime, all of which are able to prove the credibility of the sniper and its creator. 

# **V. Types of Snipers**

Snipers can be paid or free. The two recommended free snipers, [MCSniperPY](https://mcsniperpy.com) and [Smart-Sniper](https://github.com/snipesmarter/smart-sniper), are wonderful snipers to begin with; a large supportive community, constant updates, and a consistent bot allowing you to perfect your delay. Once you're much more experienced at sniping, using a great amount of accounts with a paid sniper will allow you to snipe highly sought-after names. 

> If  you want to learn more about how to use a specific sniper listed here, the links above have instructions. 
> I do not take credit for any of the snipers listed here. I did not develop nor assist in the creation of them. All credits go to their rightful owners. I encourage you to check them out!

Most proficient snipers use Minecraft giftcards (hereinafter referred to as `GCs`) to snipe. `GCs` have the capability of sending 6 name change requests instead of 2, which is the standard for any regular Mojang or Microsoft account.
Because of this, 1 `GC` equates to 3 regular accounts. Experienced snipers using them require less accounts for a higher chance of beating others. Furthermore, giftcards have their own endpoint, so their name change requests are priotized over Mojang and Microsoft accounts.*

**Subject to confirmation and revision*

# **VI. Sniping**
 
So how does the sniper work, from a user's perspective? Well, you put in the account credentials to the account(s) you want to use, it fetches the authorization token allowing it the permission to change your username. Then, you input the name you want to snipe, the delay (which will be covered later on) you want to use, and in some snipers, you are able to select what account type you are using (Mojang, Microsoft, Giftcard, etc.)
The account credentials may be allocated in a supplied text file, or may otherwise be supplied by the user directly in the terminal.
# **VII. Factors in Sniping**
 
There are a few factors in sniping: accounts in use, your delay / timing, and luck. Usually supplying more accounts and improving your timing will override your luck, meaning you have a much higher chance at being successful. 
Number of accounts is self explanatory. More accounts, more requests, higher probability.

Delay is a system where you enter how many milliseconds off the droptime you want it to start sending requests. For example, someone has 0 ping so the requests (with 0 delay) would normally send at `xx:xx:xx.000000`. 
If we were to work off the example above with JohnSmith, the name becomes available at **3:24:19 PM**. Your sniper would normally send requests are that exact time, `3:24:19.0000`. However, some names drop later than usual due to API lag and other factors. Because of this, you may miss the snipe for being too early if your delay is 0. 
Most snipers advise getting timestamps with `xx.095` - `xx.100` as they seem to have the greatest likelihood of success. So if your requests do not match, procedures can be taken to adjust it until it does.

# **VIII. Delay**

Let me elaborate on what delay really is. First I have to explain timestamps; the most fundamental mechanic of delay, as it's the guide for what changes you should make to your delay in order to perfect it.

Using the aforementioned example again, lets say your requests land at `3:24:19.230` and `3:24:19.300`
As you want to have them land at `3:24:19.095` and `3:24:19.100`, you will need to increase your delay here so the sniper shoots sooner.
First let's disregard any numbers which aren't necessary for calculating the optimal delay change for this situation:
(The two requests sent) `.230` `.300`

You are **~130 milliseconds** off the advised timestamp with the first request. The second request is **~200 milliseconds** off. It may be best to change according to the second one, so your second request lands at `.100` with the first sometime before that.
Add **200** delay. If your delay before was (for example) **129**, adjust it to **329** delay on your next snipe.

Snipe again with your new delay.
After that, analyze the results. Were they closer to the recommended timestamps? How far, if not precisely on it? Make more changes until your timestamps are on target, or, until you notice you successfully sniping names at another timestamp.

Do note that names don't drop at the same time every time. Even if you successfully get a name on `.012` one time, the same results are not guaranteed on your next snipes.

# **IX. Time Synchronization**

Another way to make your timestamps more consistent is by using a time synchronization program. This sets your computer's clock to the closest to `.0000`. If your time is always the same, then your delay and timestamps will be consistent for every snipe you use it. 

Let me clarify what I mean here. In this example, let's say you use **300** delay: you got the timestamp `.218` on the first snipe, and on the second you got `.113`. This is because your computer's clock isn't the same every time you sniped with that delay. If you use a time synchronization program such as [Dimension 4](http://www.thinkman.com/dimension4/download.htm), your timestamps with **300** delay will **usually, if not always** be the same. For this example in particular, you would get `.113` nearly every time you use **300** delay. Moreover, API lag may effect the results very slightly each time, so your timestamps may not always correspond with the delay used.

# **X. Sniping with Multiple Accounts**

If you're starting to become a more serious sniper, using more than 1 account is essential for higher success rates. If you want to learn more about how to snipe with more than 1 account, be sure to read my [guide on how to snipe with more than 1 account](https://github.com/NameMC/MULTIPLE-ACCOUNT-SNIPING).
More accounts allow you to send more name change requests to the server. Your probability of success will be much higher.

# **XI. Sniping Jargon**

In sniping there are terms and phrases which are usually shortened versions of their longer counterparts. Below are a few that you will likely run into:
|EXPANDED | SHORTENED |
| -------------| ---------------------------|
|`**MORE INFORMATION BELOW**`| Snipe |
|`**MORE INFORMATION BELOW**`| Sniper |
|Non-full access | NFA|
|Semi-full access account| SFA |
| Full access account | FA |
| Mail full access account | MFA |
| Unmigrated full access account | UFA |
| Giftcard| GC|
| Microsoft account| MSA |
| The time at which a username is available, after the 37 day period of waiting | Droptime / Drop |
-------------

The following list gives an entire explanation of each term and includes examples.

-------------
### **Snipe** 
- To claim a (Minecraft) name as fast as you possibly can. Some people confuse this with claiming a name (that's available), so they would mistakenly say:
> I saw this available 4-character name so I sniped it

- Which is incorrect because the name was available; you were not competing for ownership of the name, you were not timing your requests, you weren't having to wait until it was available. The correct usage would entail the aforementioned conditions:
> I sniped "JohnSmith" using 10 MFAs. I got it on `.0865`

᲼᲼᲼᲼᲼᲼

-------------
### **Sniper** 
- One who snipes names, or could refer to the automated sniping bot used to snipe the name.

**Example 1:**
> I'm an MFA sniper because I dislike SFA sniping.

**Example 2:**
> I used my free sniper, MCSniperPY, to get the username "Example". I would recommend it, the sniper works amazing!

᲼᲼᲼᲼᲼᲼

-------------

### **NFA** 
```sh 
* Abbreviation - Non-full Access 
``` 
- These are useless for the most part; you have credentials to Minecraft account, **but** the account has security questions which prevent you from accessing the name change page on [minecraft.net](https://www.minecraft.net/en-us). You are only able to log in through the launcher, not the website. Therefore, you are unable to change the name on the account, so it's ineligible for sniping.

**Example:**
> I have 10 NFAs. One of them I've had for 10 days without any problems.

᲼᲼᲼᲼᲼᲼

-------------

### **SFA** 
```sh 
* Abbreviation - Semi-full Access 
``` 
- SFA accounts have more access than NFAs but less than MFAs. You only have the credentials for the Minecraft account, but no access to the email tied to the account. You require email access to add security questions. Since you need security questions enabled on your account to change the email, it's locked on the email that it's currently on. 

- SFAs are often frowned upon as they are (usually) obtained from unorthodox methods and used maliciously. They are mostly used for testing delay, but may sometimes be used in serious sniping. Some people use upwards of 15 SFAs each snipe, usually yielding success. The name is wasted as SFAs are usually stolen accounts, so the sniper isn't able to ensure the name stays on the account it was sniped on. The original owner often switches their name off the one which was sniped. 
- Sometimes SFAs aren't stolen, and are instead a result of poor management of credentials by a user. For example, you forgot the password to your email and are unable to recover it or prove your ownership. The only access you have is to your Minecraft account but not your email. In this situation you have an SFA which wasn't stolen.

**Example:**
> I used 30 SFAs to get that name.

᲼᲼᲼᲼᲼᲼

-------------

### **FA / MFA**
```sh 
* Abbreviation - Mail Full Access
``` 
- FA and MFA can be used interchangeably as it simply indicates you have full access to the account. Just a normal account, can be a Mojang account or Microsoft. MFAs can be acquired from unconventional places, or via the official [minecraft.net](https://www.minecraft.net/en-us) website. 

**Example:**
> I have 4 MFAs that I haven't changed the name on for months! Maybe I can snipe something on them soon.

᲼᲼᲼᲼᲼᲼

-------------

### **UFA** 
```sh 
* Abbreviation - Unmigrated Full Access
``` 
- These accounts are from long ago, as far back as perhaps **2009 - 2010**. In the first Minecraft migration (not the current one from Mojang to Microsoft) players were asked to migrate their Minecraft account to a Mojang account. Some of these old accounts haven't been migrated yet. Functions mostly like a normal MFA account.
> Do note I have little knowledge or experience about UFAs so this is subject to change if I learn more about them.

**Example:**
> This UFA doesn't have a TID, so I won't be able to recover it easily if it gets locked.

᲼᲼᲼᲼᲼᲼

-------------

### **GC** 
```sh 
* Abbreviation - Giftcard / Giftcard Account
``` 
- Nearly identical to an MFA. However, if we were to look at the characteristics of a giftcard account, they are slightly different from an MFA:

| | |
|----- | ------ |
 | |Undetermined name| 
 | |Can send 6 name change requests instead of 2| 
 | |Are always Microsoft; there are no Mojang GC accounts| 
 | |Have name change priority `* UNCONFIRMED`| 

**Example:**
>  I used 2 `GCs` to snipe the name "TissueBox"

᲼᲼᲼᲼᲼᲼

-------------

### **MSA**
```sh 
* Abbreviation - Microsoft account
``` 
- A Microsoft account with a redeemed copy of Minecraft and a username already established. Basically an MFA with more security, because Microsoft has 2FA availability.

**Example:**
> I'm hoping I can migrate my Mojang accounts to MSAs soon, I want to secure them with two-factor authentication.

᲼᲼᲼᲼᲼᲼

-------------

### **Droptime / Drop**
- The time when a username becomes available

**Example:**
> The name "wow" drops on `August 4th, 2021 @ 3:18:11 PM, PST`

᲼᲼᲼᲼᲼᲼

-------------

# **XII. Conclusion**

As described throughout this guide, snipers have many advantages when used in comparison to traditional hand-sniping. It may be complicated or daunting at first, but after a few weeks or months it becomes a lot easier to understand.
Don't hesitate to reach out to other server members in sniping servers, some may be willing to help you.
If you don't want to commit yourself to serious sniping, there is no urgency to do so. You can continue hand-sniping, however, it will likely yield less results than using an automated bot.
Lastly, I hope you have an amazing time sniping and wish you luck along your journey!
