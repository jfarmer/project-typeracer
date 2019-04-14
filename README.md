# Typeracer!

[Typeracer][typeracer-homepage] is a website where people compete against each other to see who can type the fastest.  We're going to build a little clone.

Play the game a few times to get a sense of how the game works.  Pay particular attention to how it keeps track of what you type.

## Technology

You can use whatever technologies you want for this project.  You can use technologies you're familiar with so you can get more done.  You can use technologies you're less familiar with so you can learn more.

It's up to you, although this makes for a very good React/Vue project.  The backend is up to you.

## Example Quotes

To build a Typeracer clone you'll need some quotes.  Fortunately, you can download the list of quotes from Typeracer, here: http://www.typeracerdata.com/texts

## Iterations

In order to keep the project on track, we want people to get to something useful / fun as quickly as possible.  You might be tempted to dive into the server-side, multi-player aspect of the game, but a typing game without typing is no fun.

So, let's start with typing.

The second-hardest part will be the multi-player aspect, because the client needs to both send and receive data from the server and it needs to happen in close-to-real-time.  To handle this, consider something like websockets.

See:

- [Websockets API - MDN][mdn-websockets]
- [Beyond REST - Using Websockets][blog-beyond-rest-websockets]
- [8 NodeJS Web Socket Libraries for 2018][blog-node-websockets-2018]

### v0.1 - Single-Player, Front-End Only

The main user experience element in Typeracer is the "typing engine":

1. A user is presented with a quote
1. A countdown begins
1. When the countdown ends, the user must type the quote as quickly as possible.
1. They must type every letter correctly
1. They see which letters they have yet to type, which they've typed correctly, and which they've typed incorrectly.
1. Once the entire text is typed correctly they're informed of their typing speed in words per minute (WPM).

Create a front-end component that enabled the above interaction.  Do not worry about the multi-player or server-side aspects.  Imagine you were building a standalone JavaScript/React/Vue/etc. library that someone else could use on their website.

This is the highest-risk part of the project and therefore the part we want everyone working on it first.

### v0.2 Multi-Player, Single Game

Typeracer fills up games with 3-5 people, but first let's build a version where there's only one game at a time.  The goal is to get the real-time, multi-player aspect working.

Keep it simple:

1. A game consists of 2 players
1. Only one game is active at a time
1. Both players are informed of the winner
1. We keep track of the winner of each game server-side

### V1.0 - Multiple Games + Beyond

We don't expect anyone to get past the first two iterations in a week, but some features that are worth adding:

- Player accounts
- Multiple games
- Leaderboards
- Anti-cheating measures (no copy-paste, forcing users to verify if they type at a crazy speed, etc.)
- Games that match players based on their skill, so people are paired with players who type at similar speeds
- Ability to spectate games
- Ability to replay games


[typeracer-homepage]: https://play.typeracer.com/
[mdn-websockets]: https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API
[beyond-rest-websockets]: https://blog.logrocket.com/beyond-rest-using-websockets-for-two-way-communication-in-your-react-app-884eff6655f5
[blog-node-websockets-2018]: https://blog.bitsrc.io/8-node-js-web-socket-libraries-for-2018-818e7e5b67cf
