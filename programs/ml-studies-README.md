# ML Studies

This program is built to oversee different projects within the ML specialty.

# Random Indexes

Top USA Websites

Date Scraped: 04-28-2022

URL: https://blog.feedspot.com/usa_news_websites/

Script:

```
Array
  .from(
    document
      .querySelector('#fsb')
      .querySelectorAll('h3')
  )
  .map(e => ([e.innerText, e.childNodes.length === 3 ? e.childNodes[1] : null]))
  .filter(e => e[1])
  .map(e => [e[0], e[1].href])
  .map(e => ['[' + e[0] + ']', '(' + e[1] + ')'])
  .map(e => e.join(''))
  .join(' | ')
```

Data:

[1. CNN - Breaking News, Latest News and Videos](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=117&q=site:http%3A%2F%2Frss.cnn.com%2Frss%2Fcnn_topstories.rss) | [2. The New York Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=9470&q=site:https%3A%2F%2Fwww.nytimes.com%2Fservices%2Fxml%2Frss%2Fnyt%2FHomePage.xml) | [3. The Huffington Post](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=1215&q=site:https%3A%2F%2Fwww.huffpost.com%2Fsection%2Ffront-page%2Ffeed%3Fx%3D1) | [4. Fox News | Breaking News Updates | Latest News Headlines](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=118508&q=site:http%3A%2F%2Ffeeds.foxnews.com%2Ffoxnews%2Flatest) | [5. USA TODAY](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=667240&q=site:http%3A%2F%2Frssfeeds.usatoday.com%2FUsatodaycomNation-TopStories) | [6. POLITICO](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=150897&q=site:http%3A%2F%2Fwww.politico.com%2Frss%2Fpoliticopicks.xml) | [7. Yahoo News » Latest News & Headlines](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4633676&q=site:https%3A%2F%2Fwww.yahoo.com%2Fnews%2Frss) | [8. NPR News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=20253&q=site:http%3A%2F%2Fwww.npr.org%2Frss%2Frss.php%3Fid%3D1001) | [9. Los Angeles Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=2253987&q=site:https%3A%2F%2Fwww.latimes.com%2Flocal%2Frss2.0.xml) | [10. New York Post](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3294268&q=site:https%3A%2F%2Fnypost.com%2Ffeed%2F) | [11. Breitbart News Network](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4210776&q=site:http%3A%2F%2Ffeeds.feedburner.com%2Fbreitbart) | [12. ABC News » Top Stories](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=8678&q=site:http%3A%2F%2Ffeeds.abcnews.com%2Fabcnews%2Ftopstories) | [13. NBC News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=370715&q=site:https%3A%2F%2Fwww.nbcnews.com%2Fid%2F3032091%2Fdevice%2Frss%2Frss.xml) | [14. CBS Chicago](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=2575&q=site:https%3A%2F%2Fchicago.cbslocal.com%2Ffeed%2F) | [15. CBS Boston](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3085&q=site:https%3A%2F%2Fboston.cbslocal.com%2Ffeed%2F) | [16. CBS Philly](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3037&q=site:https%3A%2F%2Fphiladelphia.cbslocal.com%2Ffeed%2F) | [17. Newsweek](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3423301&q=site:http%3A%2F%2Fwww.newsweek.com%2Frss) | [18. CBS San Francisco](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=2222&q=site:https%3A%2F%2Fsanfrancisco.cbslocal.com%2Ffeed%2F) | [19. CBS New York](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=2362&q=site:https%3A%2F%2Fnewyork.cbslocal.com%2Ffeed%2F) | [20. CBS Dallas Fort Worth](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3276&q=site:https%3A%2F%2Fdfw.cbslocal.com%2Ffeed%2F) | [21. Chicago Tribune](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=109&q=site:https%3A%2F%2Fwww.chicagotribune.com%2Frss2.0.xml) | [22. CBS Tampa](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634532&q=site:https%3A%2F%2Ftampa.cbslocal.com%2Ffeed%2F) | [23. WCCO - CBS Minnesota](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3092&q=site:https%3A%2F%2Fminnesota.cbslocal.com%2Ffeed%2F) | [24. CBS Los Angeles](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=936052&q=site:https%3A%2F%2Flosangeles.cbslocal.com%2Ffeed%2F) | [25. New York Daily News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=363915&q=site:https%3A%2F%2Fwww.nydailynews.com%2Findex_rss.xml) | [26. Boston.com](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4437703&q=site:https%3A%2F%2Fwww.boston.com%2Ffeed%2F) | [27. Salon](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4873358&q=site:https%3A%2F%2Fwww.salon.com%2Ffeed) | [28. The Seattle Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4366653&q=site:https%3A%2F%2Fwww.seattletimes.com%2Ffeed%2F) | [29. NBC Chicago](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4574320&q=site:https%3A%2F%2Fwww.nbcchicago.com%2F%3Frss%3Dy) | [30. The Mercury News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4476920&q=site:https%3A%2F%2Fwww.mercurynews.com%2Ffeed%2F) | [31. Miami Herald](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634395&q=site:https%3A%2F%2Fwww.miamiherald.com%2Fnews%2F%3FwidgetName%3Drssfeed%26widgetContentId%3D712015%26getXmlFeed%3Dtrue%2Ffeed) | [32. KTLA | Los Angeles News and Video for Southern California](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=927031&q=site:https%3A%2F%2Fktla.com%2Ffeed%2F) | [33. NBC New York](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=1232631&q=site:https%3A%2F%2Fwww.nbcnewyork.com%2Ffeed%2F) | [34. The Washington Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=762100&q=site:http%3A%2F%2Fwww.washingtontimes.com%2Frss%2Fheadlines%2Fnews%2F) | [35. Newsday](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4633937&q=site:https%3A%2F%2Fwww.newsday.com%2Fxml%2Fnewsday-latest-stories-1.21987683) | [36. Chicago Sun-Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4277680&q=site:https%3A%2F%2Fchicago.suntimes.com%2Frss%2Findex.xml) | [37. Observer](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=19235&q=site:https%3A%2F%2Fobserver.com%2Ffeed%2F) | [38. ABC13 Houston | KTRK Houston and Southeast Texas News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4027768&q=site:https%3A%2F%2Fabc13.com%2Ffeed%2F) | [39. FOX31 Denver KDVR](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=922&q=site:https%3A%2F%2Fkdvr.com%2Ffeed%2F) | [40. Gothamist](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=26964&q=site:https%3A%2F%2Fgothamist.com%2Ffeed) | [41. WFLA WFLA News Channel 8 On Your Side in Tampa Bay Florida](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4511068&q=site:https%3A%2F%2Frss2.feedspot.com%2Fhttps%3A%2F%2Fwww.wfla.com%2F%3Fcontext%3D2087087408) | [42. NBC Los Angeles](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634548&q=site:https%3A%2F%2Fwww.nbclosangeles.com%2Fnews%2Ftop-stories%2F%3Frss%3Dy%2Ffeed) | [43. The Intercept](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4477517&q=site:https%3A%2F%2Ftheintercept.com%2Ffeed%2F%3Flang%3Den) | [44. KXAN News | Austin News & Weather Austin Texas, Round Rock, TX](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4473993&q=site:https%3A%2F%2Fwww.kxan.com%2Ffeed%2F) | [45. Boston Herald](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=531749&q=site:https%3A%2F%2Fwww.bostonherald.com%2Ffeed%2F) | [46. ABC7 News » San Francisco Music](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4418692&q=site:https%3A%2F%2Fabc7news.com%2Ffeed%2F) | [47. Daily Herald | Suburban Chicago Breaking News, Daily News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=39949&q=site:https%3A%2F%2Fwww.dailyherald.com%2Frss%2Ffeed%2F%3Ffeed%3Dnews_top5) | [48. Automotive News](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3593963&q=site:https%3A%2F%2Fwww.autonews.com%2Fsection%2Frss%2Fnews%3Ftopics%3D48856) | [49. NBC4 Washington](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634169&q=site:https%3A%2F%2Fwww.nbcwashington.com%2F%3Frss%3Dy) | [50. L.A. Weekly](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4414845&q=site:https%3A%2F%2Fwww.laweekly.com%2Ffeed%2F) | [51. PhillyVoice](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634177&q=site:https%3A%2F%2Fwww.phillyvoice.com%2Ffeed%2F) | [52. KRON4.com | San Francisco Bay Area News and Weather](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4407213&q=site:https%3A%2F%2Fwww.kron4.com%2Ffeed%2F) | [53. amNewYork](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4633928&q=site:https%3A%2F%2Fwww.amny.com%2Fxml%2F1.2427115%2Frss) | [54. WSVN 7 News Miami](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4466556&q=site:https%3A%2F%2Fwsvn.com%2Ffeed%2F) | [55. NBC 7 San Diego](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634478&q=site:https%3A%2F%2Fwww.nbcsandiego.com%2Fnews%2Ftop-stories%2F%3Frss%3Dy%26amp%3BembedThumb%3Dy%26amp%3Bsummary%3Dy) | [56. NBC 5 Dallas-Fort Worth](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634155&q=site:https%3A%2F%2Fwww.nbcdfw.com%2Fnews%2Ffeed%2F) | [57. FOX5 San Diego](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=3696356&q=site:https%3A%2F%2Ffox5sandiego.com%2Ffeed%2F) | [58. NBC 10 Philadelphia](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634391&q=site:http%3A%2F%2Fwww.nbcphiladelphia.com%2Fnews%2Ftop-stories%2F%3Frss%3Dy%2Ffeed) | [59. FOX2now](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=915&q=site:https%3A%2F%2Ffox2now.com%2Ffeed%2F) | [60. NBC 6 South Florida](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634398&q=site:https%3A%2F%2Fwww.nbcmiami.com%2F%3Frss%3Dy) | [61. Village Voice](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4633920&q=site:https%3A%2F%2Fwww.villagevoice.com%2Findex.rss) | [62. Pioneer Press](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634522&q=site:https%3A%2F%2Fwww.twincities.com%2Ffeed%2F) | [63. 7News Boston WHDH](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634423&q=site:https%3A%2F%2Fwhdh.com%2Ffeed%2F) | [64. Chicago Reader](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=665&q=site:https%3A%2F%2Fwww.chicagoreader.com%2Fchicago%2FRss.xml) | [65. Riverfront Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634506&q=site:http%3A%2F%2Fwww.riverfronttimes.com%2Fstlouis%2FRss.xml) | [66. Detroit Metro Times](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634535&q=site:http%3A%2F%2Fwww.metrotimes.com%2Fdetroit%2FRss.xml) | [67. NEWS10 ABC](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4308138&q=site:https%3A%2F%2Fwww.news10.com%2Ffeed%2F) | [68. WIVB-TV](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4407514&q=site:https%3A%2F%2Fwww.wivb.com%2Ffeed%2F) | [69. City Limits](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634021&q=site:https%3A%2F%2Fcitylimits.org%2Ffeed%2F) | [70. Times of San Diego](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634491&q=site:http%3A%2F%2Ftimesofsandiego.com%2Ffeed%2F) | [71. MinnPost](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634511&q=site:https%3A%2F%2Fwww.minnpost.com%2Ffeed%2F) | [72. The Published Reporter®](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=5168359&q=site:https%3A%2F%2Fwww.publishedreporter.com%2Ffeed%2F) | [73. The Alike](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=5353858&q=site:https%3A%2F%2Fthealike.com%2Ffeed%2F) | [74. New York Sun](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=119&q=site:https%3A%2F%2Fwww.nysun.com%2Frss.xml) | [75. The Texas Observer](https://www.feedspot.com/infiniterss.php?_src=feed_title&followfeedid=4634556&q=site:https%3A%2F%2Fwww.texasobserver.org%2Ffeed%2F)