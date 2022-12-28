# twitter-offboarding
Collection of helpful tools for leaving Twitter, enhancing the Twitter archive, deleting your data and moving over to Mastodon.

Feel free to suggest other tools by creating an issue or pull request.

## Table of contents
  - [Use and enhance your Twitter archive](#use-and-enhance-your-twitter-archive)
    * [twitter-archive-parser](#twitter-archive-parser)
    * [get-twitter-bookmarks](#get-twitter-bookmarks)
    * [twitter-archive-browser](#twitter-archive-browser)
  - [Back up information not included in your twitter archive](#back-up-information-not-included-in-your-twitter-archive)
    * [Export your Twitter lists](#export-your-twitter-lists)
    * [Offload your followings' information](#offload-your-followings-information)
    * [Export bookmarks as markdown file](#export-bookmarks-as-markdown-file)
  - [Mastodon](#mastodon)
    * [Move your followings to Mastodon](#move-your-followings-to-mastodon)
    * [Find accounts to follow](#find-accounts-to-follow)
      + [Accounts your followings follow the most](#accounts-your-followings-follow-the-most)
  - [Clean up your Twitter profile and DMs](#clean-up-your-twitter-profile-and-dms)
    * [1. Go private](#1-go-private)
    * [2. Soft-block your followers](#2-soft-block-your-followers)
    * [3. Delete your tweets, likes (and DMs) with Semiphemeral](#3-delete-your-tweets-likes-and-dms-with-semiphemeral)
    * [4. Check for online-archives of your profile](#4-check-for-online-archives-of-your-profile)

## Use and enhance your Twitter archive
[Download your Twitter archive](https://twitter.com/settings/download_your_data) in your account settings. Here are some tools that can help to enhance the downloaded archive or make better use of it.

### twitter-archive-parser
[twitter-archive-parser](https://github.com/timhutton/twitter-archive-parser) is some python code to parse a Twitter archive and output in various ways. Takes your archive and converts it to markdown with embedded images, videos and links. Replaces the obfuscated t.co-links with their original links. Comes with a second script that can help you downloading the original size of the images you've posted.

### get-twitter-bookmarks
Your Twitter archive does not include tweets you bookmarked. [get-twitter-bookmarks](https://gist.github.com/divyajyotiuk/9fb29c046e1dfcc8d5683684d7068efe) intakes JSONs of your bookmarked tweets and saves them in a markdown file. You need to be familiar with using your browser's dev tools in order to collect the JSONs as they are not included in the official Twitter archive. The script's author has also written a [short tutorial](https://dev.to/divyajyotiuk/exporting-your-twitter-bookmarks-in-markdown-file-19bj) on how to collect everything you need.

### twitter-archive-browser
[twitter-archive-browser](https://sk22.github.io/twitter-archive-browser/) lets you browse your Twitter archive and bulk-delete tweets in a certain timeframe or containing certain keywords with your browser's console.

## Back up information not included in your twitter archive
### Export your Twitter lists
The easiest way to export your twitter lists is by using Tweetdeck and following [this guide](https://www.makeuseof.com/tag/backup-export-twitter-lists/).

### Offload your followings' information
Your Twitter archive does not contain information about your followings, especially not their profiles' bio or websites. Download this information in case you want to stay connected outside of Twitter or follow their blog. [Twitter Followings OPML Export](http://opml.glitch.me/) helps you to get websites and RSS Feeds of the people you follow on Twitter.

### Export bookmarks as markdown file
You first need to collect JSONs of your bookmarks which then can be converted to a Markdown file with the help of this Python script. The instructions and a link to the script can be found [here](https://dev.to/divyajyotiuk/exporting-your-twitter-bookmarks-in-markdown-file-19bj).

## Mastodon

### Move your followings to Mastodon
Tools that match your Twitter followings' accounts with their Mastodon account(s) and enable you to bulk-follow all of them.

- [Debirdifiy](https://pruvisto.org/debirdify/) authorises with your Twitter account and scans your followings' accounts (display name, bio, website, pinned tweet) for Fediverse account names
- [Fedifinder](https://fedifinder.glitch.me) works just like Debirdifiy but results may vary between the two services. Give them both a try.
- [Movetodon](https://www.movetodon.org/) scans your Twitter followings' profiles just like Fedifinder and Debirdify but lets you selectively follow their respective Mastodon account right outside of your browser without the need for a .csv download & upload
- [Twitodon](https://twitodon.com/) takes a different approach by authorising with both your Twitter and Mastodon account and display people of your Twitter followings who have done the same

### Find accounts to follow
#### Accounts your followings follow the most
[Who To Follow](https://whotofollow.tibor.net/) runs locally in your browser. First it collects all your followings, then looks for all the people your followings follow and sorts them by who's followed the most.

[Followgraph](https://followgraph.vercel.app/) does a similar job but was a bit quicker in my tests.

## Clean up your Twitter profile and DMs
I don't suggest or even recommend deleting your Twitter profile as this makes your handle (the @username-thingy) available again for anyone to take over. If you want to leave Twitter and clean up behind yourself it's a good idea to first inform your followers where else they may be able to contact you. Also it is better to leave the account active but - depending on your likes - delete some or all contents. Find some recommendations with increasing "severity" below.

### 1. Go private
The easiest way to quickly prevent new users, search engines and other crawlers to read your content. Your followers will of course still be able to read your profile's contents. Your bio will still be visible to anyone.

### 2. Soft-block your followers
To prevent (some of) your followers from reading your past tweets, soft-block them by going to their profile, blocking and (if you wish) unblocking them again. For a large follower count this may be rather time consuming so you could use an automated tool like [Redblock](https://github.com/gaeulbyul/RedBlock/blob/main/README.en.md).

### 3. Delete your tweets, likes (and DMs) with Semiphemeral
[Semiphemeral](https://github.com/micahflee/semiphemeral) is a hosted service (though you could also set it up yourself) that connects to your Twitter account and automatically deletes your old tweets, except for the ones you want to keep. Can also be used to delete all of your DMs - though that will only delete them on your end.

Keep in mind that there are limits to the number of tweets and DMs Twitter exposes via their API. Without academic access you can only retrieve and therefore delete the last [3200 tweets](https://github.com/micahflee/semiphemeral) and [30 days of DMs](https://twittercommunity.com/t/retrieving-older-than-30-days-direct-messages-direct-messages-events-list/104901).

In case you have more than 3200 tweets there are some paid tools but I am not comfortable sharing them here because I haven't tested them (yet).

### 4. Check for online-archives of your profile
There are services like the Internet Archive that anyone can use to create snapshots of webpages - and yes, that includes Twitter profiles. Getting a profile page deleted from the Internet Archive takes some steps on its own and I published a step-by-step guide on [Twitter](https://twitter.com/achisto/status/1591065125167190018?s=20&t=KeqeI8H7lVPlrdyAzlegDg) and [Mastodon](https://mastodon.social/@achisto/109325841635487550).
