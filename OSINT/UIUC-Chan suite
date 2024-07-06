*team name: example.com*

We read through each of the prompts in the suite to get an idea what we were getting into before beginning. There isn't much to go off of, but seems like it will be fun, so let's get started.

> Disclaimer: all screenshots taken after UIUCTF ended
# Challenge 1: Hip With the Youth

![[Pasted image 20240706120753.png]]
__Information gained from prompt__
- `Long Island Subway Authority` or `LISA` are names to look out for
- Something on `Instagram`

Okay, so we need to use Instagram and "find a way" to somewhere else with it?

## Information Gathering Stage
Searching for `LISA` for accounts on Instagram didn't give us much, but `long island subway authority` got us to what we suspected was the correct account.

![[LISA account.jpg|center|400]]
Both posts themselves are not helpful, the account was not tagged in any external posts, and the followers seemed to just be other participants of the CTF event.

Then we noticed the [threads link](https://www.threads.net/@longislandsubwayauthority). 

> The member working on this challenge at the time did not have the threads app on her phone, and did not want to install it or create an account for it. Because of this, we skipped to Challenge 2 and came back to this challenge later. 

After we figured out we could go to threads on the Web, we did and arrived at the relevant account (with the same LinkedIn page link found in Challenge 2).

![[Pasted image 20240706140010.png|center|550]]

## Thinking Stage
The following image shows the posts that are visible for this account. We can see that one mentions the flag, but are not sure what to do since we aren't logged in.

![[Pasted image 20240706140052.png|center|525]]
Again we thought that we had to log in to see more, so we took a pause on this challenge and came back a few minutes later.

	The reason we thought we needed an account to view more was because we were not familiar with the threads interface and it looked like you had to log in to see more content.

## The Solve
Coming back to this challenge again, we became more determined and actually clicked on the posts. By selecting either of the last two posts shown in the image above, we can see the flag immediately.

![[Pasted image 20240706140626.png|center|500]]

**The flag for this challenge is `uiuctf{7W1773r_K!113r_321879}
`**

> Leet-speak translation for the flag - "twitter killer"

---
# Challenge 2: An Unlikely Partnership

![[Pasted image 20240706120915.png]]
__Information gained from prompt__
- LISA has a `business partnership`

> We start this challenge off *prior* to completing `Hip With the Youth` (Part 1 of this suite), so we do not have the LinkedIn link found at the completion of that part.

## Information Gathering Stage
We decide to go to our trusty search engine and see what it'll chug out for us... see what I did there? :)

Our initial search didn't give us much, but with some keyword addition we get a LinkedIn page!

**Search #1**

![[Pasted image 20240706133601.png|575]]

**Search #2**

![[Pasted image 20240706132845.png]]
The following information about the account makes us even more certain we have the right one.

| ![[Pasted image 20240706125234.png\|200\|260]] | ![[Pasted image 20240706125248.png]] |
| ---------------------------------------------- | ------------------------------------ |

## Thinking Stage
The following elements are included in a typical LinkedIn page:
- About
- Activity
- Experience
- Skills
- Interests

We can immediately cross off About, Experience, and Interests just from looking at them because those are simply text fields without any links, so we have Activity and Skills left. 

Three of the four items on the Activity page are simply links to LinkedIn games Pinpoint and Crossclimb, so we ignore those. The last post left is just a text post, no flags in sight.

![[Pasted image 20240706141744.png]]

## The Solve
Last, but not least, we check out the Skills page. 

![[Pasted image 20240706141758.png]]
> Ooh, an endorsement... I wonder who that could be?

![[Pasted image 20240706141843.png]]
Gotchya! UIUC Chan has endorsed the Transportation skill of LISA! The flag is now pinpointed to be in the About section of UIUC Chan's profile.

![[Pasted image 20240706141924.png]]

**The flag for this challenge is `uiuctf{0M1g0D_UIUCCH4N_15_MY_F4V0r173_129301}`**
> Leet-speak translation for the flag - "omigod uiucchan is my favorite"

---
# Challenge 3: The Weakest Link

![[Pasted image 20240706120449.png]]
__Information gained from prompt__
- What we need will be on `Spotify`
- Look out for a feature that can be set to private or not private (public?)
- It includes something that is a "collaboration"

		From Challenge 2 in this suite, we know the name of the "secret business partner" is `UIUC-Chan`.

## Information Gathering Stage
UIUC Chan's LinkedIn profile found in Challenge 2 has the link to her Spotify profile, much to her embarrassment!
![[Pasted image 20240706142452.png|500]]
Spotify link: [open.spotify.com/user/31d2lcivqdieyl4qzx25vfmp6jt4?si=b769b2466f7e4101](https://open.spotify.com/user/31d2lcivqdieyl4qzx25vfmp6jt4?si=b769b2466f7e4101)

At first glance, it doesn't look like much to us. It only has one public playlist.

| ![[Pasted image 20240706122053.png \| 300]] | ![[Pasted image 20240706122202.png\|200]] |
| ------------------------------------------- | ----------------------------------------- |

We begin playing the songs in from the `songs to hail to the orange and hail to the blue to` playlist, perhaps the flag is hidden in a song? (we thought that might be cool) The name of the playlist threw us off a bit. Were we supposed to know something about the Illini fight song??

![[Pasted image 20240706121354.png|650]]
Next, we check the people who created the songs in the playlist. We find that both belong to verified accounts with a large number of monthly listeners. Due to this fact, they seem legit (i.e. not made for this challenge), so we try another direction.

![[Pasted image 20240706121818.png]]
![[Pasted image 20240706121803.png]]
It was at this point that we noticed the UIUC-Chan account had gained several more followers since we started looking, having only 4 followers the first time we viewed the account. This seemed interesting, so we also followed the account, hoping for something.

## Thinking Stage
After following the account, it did not seem like anything changed, so we did a quick Google search. The first hit gave us an explanation.
![[Pasted image 20240706122631.png]]
![[Pasted image 20240706122659.png|600]]
Aha! `You will see what your friend is playing as long as his listening habits are public and you have the Friend Feed open.` We now recall the prompt `Spotify collaboration ... neither ... keep it private.` This line with this new knowledge makes it clear to us that we are on the right track.

We find the `Friend Activity` button (seems they renamed the feature since 2017) at the top right of the screen. Clicking on it opens a new panel to the right with the activity, just as we were told by @detective889 in the post!

| ![[Pasted image 20240706123057.png\|250]] | ![[Pasted image 20240706123301.png\|400]] |
| ----------------------------------------- | ----------------------------------------- |
## The Solve
Going in order of what is shown to us - from top to bottom and left to right - we have:
- profile name of friend: `UIUC-Chan`
- name of current song this user is playing: `Skimbleshanks: The Railway Cat` 
	we play the song for good measure, still hoping the flag would be given to us in song form
- artist name: `Andrew Lloyd Webber`
- playlist name: `songs for train lovers`

From here, we clicked on each item just in case, but then remembered the prompt again - `collaboration` - this must mean a combined playlist! Selecting the playlist name leads us to the playlist and low and behold, we have captured the flag!

![[Pasted image 20240706130929.png]]
It is located in the description section of the playlist information. We know for certain it is related to our challenge because now we see LISA added the songs to the playlist!

**The flag for this challenge is `uiuctf{7rU1Y_50N65_0F_7H3_5UMM3r_432013}`**
	Leet-speak translation for the flag - "truly songs of the summer"

Hooray! We finished the UIUC-Chan OSINT suite. That was super fun.
# Post Completion Thoughts
- During the creation of this writeup, we realized that if we had been reading more carefully that this suite would have been more straightforward. 
- We commend the challenge writer of this suite, Emma, for writing such great hidden-in-plain-sight hints.
