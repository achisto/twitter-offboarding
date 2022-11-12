# twitter-offboarding
Collection of helpful tools to offboard Twitter, enhance the Twitter archive, delete your data and move over to Mastodon.

## Use and enhance your Twitter archive
Download your Twitter archive in your account settings. Here are some tools that can help to enhance the downloaded archive or make better use of it.

### [twitter-archive-parser](https://github.com/timhutton/twitter-archive-parser)
Python code to parse a Twitter archive and output in various ways. Takes your archive and converts it to markdown with embedded images, videos and links. Replaces the obfuscated t.co-links with their original links.

### [get-twitter-bookmarks](https://gist.github.com/divyajyotiuk/9fb29c046e1dfcc8d5683684d7068efe)
Your Twitter archive does not include tweets you bookmarked. This python code helps to get text and link of your bookmarked tweets and save them in a markdown file.

### [twitter-archive-browser](https://sk22.github.io/twitter-archive-browser/)
Browse your Twitter archive and bulk-delete tweets in a certain timeframe or containing certain keywords with your browser's console.

## Back up information not included in your twitter archive
### Export your Twitter lists
The easiest way to export your twitter lists is by using Tweetdeck and following [this guide](https://www.makeuseof.com/tag/backup-export-twitter-lists/).

### Offload your followings' information
Your Twitter archive does not contain information about your followings, especially not their profiles' bio or websites. Download this information in case you want to stay connected outside of Twitter or follow their blog. [Twitter Followings OPML Export](http://opml.glitch.me/) helps you to get websites and RSS Feeds of the people you follow on Twitter.


## Move your followings to Mastodon
Tools that match your Twitter followings' accounts with their Mastodon account(s) and enable you to bulk-follow all of them.

- [Debirdifiy](https://pruvisto.org/debirdify/) authorises with your Twitter account and scans your followings' accounts (display name, bio, website, pinned tweet) for Fediverse account names
- [Fedifinder](https://fedifinder.glitch.me) works just like Debirdifiy but results may vary between the two services. Give them both a try.
- [Twitodon](https://twitodon.com/) takes a different approach by authorising with both your Twitter and Mastodon account and display people of your Twitter followings who have done the same


## Clean up your Twitter profile and DMs
I don't suggest or even recommend deleting your Twitter profile as this makes your handle (the @username-thingy) available again for anyone to take over. If you want to leave Twitter and clean up behind yourself it's a good idea to first inform your followers where else they may be able to contact you. Also it is better to leave the account active but - depending on your likes - delete some or all contents. Find some recommendations with increasing "severity" below.

### 1. Go private
The easiest way to quickly prevent new users, search engines and other crawlers to cread your content. Your followers will of course still be able to read your profile's contents. Your bio will still be visible to anyone.

### 2. Soft-block your followers
To prevent (some of) your followers from reading your past tweets, soft-block them by going to their profile, blocking and (if you wish) unblocking them again. For a large follower count this may be rather time consuming so you could use an automated tool like [Redblock](https://github.com/gaeulbyul/RedBlock/blob/main/README.en.md).

### 3. Delete your tweets, likes (and DMs) with Semiphemeral
[Semiphemeral](https://github.com/micahflee/semiphemeral) is a hosted service (though you could also set it up yourself) that connects to your Twitter account and automatically deletes your old tweets, except for the ones you want to keep. Can also be used to delete all of your DMs - though that will only delete them on your end.

Keep in mind that there are limits to the number of tweets and DMs Twitter exposes via their API. Without academic access you can only retrieve and therefore delete the last [3200 tweets](https://github.com/micahflee/semiphemeral) and [30 days of DMs](https://twittercommunity.com/t/retrieving-older-than-30-days-direct-messages-direct-messages-events-list/104901).

In case you have more than 3200 tweets there are some paid tools but I am not comfortable sharing them here because I haven't tested them (yet).

### 4. Check for online-archives of your profile
There are services like the Internet Archive that anyone can use to create snapshots of webpages - and yes, that includes Twitter profiles. Getting a profile page deleted from the Internet Archive takes some steps on its own and I published a step-by-step guide on [Twitter](https://twitter.com/achisto/status/1591065125167190018?s=20&t=KeqeI8H7lVPlrdyAzlegDg) and [Mastodon](https://mastodon.social/@achisto/109325841635487550).
