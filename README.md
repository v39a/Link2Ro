# Link2Ro

## Where's the Discord server link to the Link2Ro Discord support server?
> You can get the link by running the `/support` command or by clicking this [link](https://discord.gg/uZh9c59XVS).

## How do I invite Link2Ro?
> You can invite Link2Ro to your own guild by using this [link](https://discord.com/oauth2/authorize?client_id=1245056156184088596).

## How do I set-up Link2Ro for my guild?
> You can setup Link2Ro for your own guild by running any of the `/settings` commands. Like, `/settings-permissions`, `/settings-channels`, etc. We recommend setting up rankbinds last and everything else first.

## What are the valid nickname templates?
> Below is a list of the valid nickname templates, and you can even add emojis and words to the templates. Here's a few examples: `💎 {roblox-username}`, `[SPC] 💎 {roblox-username}`, `{roblox-username}`.
```
{roblox-username}, {roblox-display}, {roblox-smart}, {discord-username}, {none}
```

## How do priorities work?
> Priorities tell Link2Ro which nickname template to use if a user is ranked in more than one group. Take, for example, you have two separate groups in the rankbinds database and the user has a specific role in both groups:
```
Group ID: 111
Priority: 1
Template: {roblox-username}

Group ID: 222
Template: {roblox-display}
Priority: 2
```
> Since the second rankbind has a greater priority than the first, Link2Ro will change the user's nickname to their roblox display name instead of their username.

## How do identifiers work?
> Identifiers work as a way to combine nickname templates between two different groups:
```
Group ID: 111
Priority: 1
Template: [ADMIN] {roblox-username}
Identifier: ADMIN
Identifier-Placement: 1

Group ID: 222
Template: 💂 {roblox-display}
Priority: 2
Identifier: ADMIN
Identifier-Placement: 2
```
> If a user is ranked in both group 111 and group 222, then their nickname will be `[ADMIN] 💂 {roblox-username}`. If group 222 had the identifier placement of 1 and group 111 had the identifier placement of 2, then their nickname will be `💂 [ADMIN] {roblox-display}`.
