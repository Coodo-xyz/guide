---
description: >-
  Here we will see how to create a recurrent poll with the Strawpoll bot.
  Recurrent polls are a way of posting polls at a certain interval.
cover: .gitbook/assets/coodo motif banner.png
coverY: 0
---

# 🕐 Recurrent Polls

## Recurrent Poll creation

Go to a channel on your discord server and type `/recurrent-poll create`.

<figure><img src=".gitbook/assets/Capture d&#x27;écran 2023-11-13 224653.png" alt=""><figcaption></figcaption></figure>

{% content-ref url="i-get-an-error/i-cant-see-the-commands.md" %}
[i-cant-see-the-commands.md](i-get-an-error/i-cant-see-the-commands.md)
{% endcontent-ref %}

Click on the command, select your options and fill them.

{% hint style="info" %}
To display all options place your cursor at the end of the line
{% endhint %}

## Options

| Option | What it does |
| --- | --- |
| `channel` | The channel where each poll is posted. |
| `schedule` | How often the poll repeats: every day, weekdays (Mon to Fri), weekends, one day of the week, or every month (same date as the day you create it). |
| `at` | The time of day the poll is posted, 24h format. Example: `20:00` |
| `timezone` | The timezone of `at`. Default: Europe/Paris. Start typing to search, for example `New York` or `UTC`. |
| `maxchoices` | How many choices a member can pick (1 for a single choice). |
| `anonymous` | Hide who voted: results show counts only, never names. |
| `hideresults` | Hide the results while the poll is open. |
| `title`, `choice1` to `choice14`, `description`, `image` | The content of the poll. |
| `sendnow` | Also post the first poll right away. |

{% hint style="info" %}
The old `time` option (for example `1d6h`) no longer exists. The interval is now set with `schedule` and `at`.
{% endhint %}

## Closing the polls

A recurrent poll stays open until it is closed with its "End the poll" button.

With 💎 Premium, the `autoclose` option of `/recurrent-poll edit` closes each poll when the next one is posted, and the new poll shows how the previous one ended.

## Change a recurrent poll

Use `/recurrent-poll edit` and pick your poll in `id`. You can change `schedule`, `at`, `timezone`, `channel`, `title`, `description` and `image`.

💎 Premium options, on `/recurrent-poll edit` only:

* `autoclose`: close the previous poll when the next one is posted, with a recap.
* `role`: a role mentioned each time the poll is posted (`removerole` to stop).

You can also edit your recurrent polls on the [dashboard](https://dashboard.coodo.xyz/user/recurrentpolls): title, description, image, time of day, days of the week, day of the month, and pause or resume.

## Other commands

* `/recurrent-poll list`: your recurrent polls and when each one is posted next.
* `/recurrent-poll trigger`: post a poll right now, without changing the schedule.
* `/recurrent-poll state`: pause (`active: False`) or resume (`active: True`) a recurrent poll.
* `/recurrent-poll delete`: delete a recurrent poll. The polls already posted stay in the channel.
