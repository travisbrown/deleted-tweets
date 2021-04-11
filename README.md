## About the project

The original motivation for this project was a [cease and desist letter][cease-and-desist]
that I received from John De Goes (a prominent conference organizer in the Scala community),
who claims that I defamed him by quoting abusive and white-nationalist-friendly tweets that he had deleted.
You can read more about that situation [here][response-to-de-goes].

## Datasets

We've currently published the following metadata:

* [Suspended account information](data/suspended/README.md)

The complete dataset now includes 11,395,758 distinct deleted or unavailable tweets from 1,109,230 Twitter accounts,
out of a total of 38,218,401 tweets from 3,730,580 accounts scraped from 20,812,445 Wayback Machine pages.

## Methodology

Please note that none of the content linked here or associated with this project was accessed directly from Twitter.
All data was gathered from the [Wayback Machine][wayback-machine] over several months, via the following steps:

* We choose a set of seed accounts, mostly representing far-right activists associated with [LambdaConf][lambdaconf], Gamergate, QAnon, etc.
* We use the [Wayback Machine's CDX index][wayback-machine-cdx] to list all archived tweet URLs for these accounts.
* We download these archived pages (which are a mix of HTML and JSON) from the Wayback Machine, saving the Wayback Machine's "original" version of each page, together with the Wayback Machine's digest for that page.
* We parse these pages to extract information about individual tweets and Twitter accounts.
* We identify retweets, replies, and other relationships between accounts, and use these relationships to add new accounts to the download queue.
* We repeat these steps with the updated set of accounts.

Most of this process is automated using tools from the [cancel-culture] project.

## Future plans

We're planning to launch a full-text search interface for these deleted tweets in the next couple of months.
In the meantime please contact [me][travisbrown] on Twitter if you're interested in
getting access to the data or in generating
[deleted tweet reports for individual accounts][deleted-tweet-report-example].

## Current top hundred accounts

The following list shows the current top 100 Twitter accounts by number of deleted or unavailable tweets.

```
  71039 JackPosobiec
  45286 infowars
  44137 dotjenna
  35837 ali
  34924 RealAlexJones
  33432 mattyglesias
  33232 MorlockP
  31643 Communism_Kills
  30156 StefanMolyneux
  29694 GrrrGraphics
  26903 tracybeanz
  26517 dbongino
  26305 DVATW
  23434 razibkhan
  21707 getongab
  21228 a_centrism
  20659 metalliclown
  20396 DrDavidDuke
  20375 Glinner
  19329 ChiefScientist
  18418 AlwaysActions
  18410 gatewaypundit
  17295 Grummz
  16899 realDonaldTrump
  16567 Cernovich
  16064 Carpedonktum
  16005 qwertyplication
  15998 DeAnna4Congress
  14939 gwern
  14590 va_shiva
  13218 jonkay
  12336 SidneyPowell1
  12304 Styx666Official
  12168 AndreVanDelft
  11583 PepeMatter
  11462 davidicke
  10904 MAGAPILL
  10899 AdamBaldwin
  10378 WarRoomPandemic
  10089 TeamTrump
   9843 JAGKEV
   9476 pegobry
   9379 breaking911
   9210 dysinger
   8916 MaggieL
   8564 mirriam71
   8560 stillgray
   8558 ExcludedMuddle
   8530 NickJFuentes
   8343 pnehlen
   7764 Worried_Canuck
   7654 spakhm
   7619 JacobAWohl
   7412 prezcannady
   7391 mamendoza480
   7225 larrydaliberal
   7049 soulcookie322
   6895 JesseKellyDC
   6894 mitchellvii
   6845 FaithGoldy
   6768 RealWayneRoot
   6569 JCompson_III
   6363 LLinWood
   6334 BluehandArea
   6136 S___Elliott
   6035 salvamedomine
   5993 LeLook4
   5916 johanatan
   5845 RyanMaue
   5815 johnroderick
   5778 AlwaysACowboy
   5595 Docstockk
   5459 Austen
   5412 TheMadDimension
   5396 Project_Veritas
   5075 TheHinduDindu
   4869 SteveStuWill
   4869 LauraLoomer
   4604 LanaLokteff
   4601 journalistew
   4423 CelticWoman5
   4402 Goy_Talk_USA
   4298 drawandstrike
   4167 Michael82379998
   4122 Stalin_Groyper
   3976 BoolinFool
   3913 HumansOfFlat
   3694 BrianKolfage
   3687 Cinderwooded
   3522 laikasrefectory
   3514 philderome
   3431 rooshv
   3421 RichardTBurnett
   3412 CassandraRules
   3234 CanAditude
   3200 PereGrimmer
   3162 CodeMonkeyZ
   3137 hawk_cloud
   3122 jondelarroz
   3091 peterboghossian
```

[cancel-culture]: https://github.com/travisbrown/cancel-culture
[cease-and-desist]: https://gist.github.com/travisbrown/d9e2e727d7a43b9be4ce6e05c85e1626
[deleted-tweet-report-example]: https://gist.github.com/travisbrown/059310042193a2e143408b05bdc2278d
[lambdaconf]: https://meta.plasm.us/posts/2019/09/01/jdg-and-the-fp-community/
[response-to-de-goes]: https://meta.plasm.us/posts/2020/07/25/response-to-john-de-goes/
[travisbrown]: https://twitter.com/travisbrown
[wayback-machine]: https://archive.org/web/
[wayback-machine-cdx]: https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md
