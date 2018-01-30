# [blockPoll](http://georgeosddev.github.com/markdown-edit)

blockPoll is a pseudo-anonymous, online, blockchain-based voting tool, used to facilitate organizational-based proxy voting and polling mechanisms for a wide array of uses. 

[![Screen Shot](images/ScreenShot.png)](http://georgeosddev.github.com/markdown-edit)

## What is it

By leveraging the power of the Etherium blockchain, coupled with an easy to use web API, blockpoll provides a mechanism whereby both corporate and non-corporate organisations can conduct voting or polling-like events in a decentralised manner. During the voting process, all participants (voters and candidates) are able to see in real-time the progress results of the undertaken vote without anyone other than the registrar(s) being able to see which voter voted for which candidate. <br> The final tallied outcome of the vote is also publicly accessible to all members, with the same level of anonymity discussed above. The creator of the vote is able to specify the type of proxy voting procedure (partial, non-partial) as well as user decided input arguments decided upon during contract creation.

## How it works

Given a list of potential candidates, as well as the those who are eligible within the organization to vote for said candidates (Decided upon by a central authorizing committee within the organization), the tool allows an administrative user to create both partial or non-partial proxy voting schemes. By uploading a CSV file of the voters and their associated voting power, the voting participants are randomly bound to a voting Id generated by the tool. The Id of each voter and the numerical representation of their voting power is made publically available, but the Id-voter pair is known only by the administrator/registrar and the voter itself. By displaying the Id of each voter, as well as who that Id voted for, the current progress of the voting process can be displayed to each voter and candidate. This means that the voter is able to verify that his/her vote has been logged correctly while still preserving the anonymity of the voter. An ethereum deployed smart contract manages the creation, tallying of votes and deletion of each instantiated voting contract. This allows for complete immutability of all results, and prevents those with malicious intent from interfering with the voting process or the results they produce. Additionally, after creation, as long as the voting process has not yet begun (Start and end date/time decided upon by administrator of the contract through by specifying block numbers), the administrator is able to delete the contract in the event of a miscreated poll. However, once the specified begin block has been mined, the contract cannot be deleted, preserving its immutability and transparency for the benefit of both those who are voting and the candidates being voted for.

## Why it works

Why choose blockPoll over current proxy voting mechanisms?

### Current voting mechanisms
In a corporate business context, proxy voting allows for a ballot to be cast by one person on behalf of a shareholder of a corporation. This allows for the vote to be conveniently cast without the shareholder having to attend a shareholders meeting. These shareholders receive a ballot - either by mail, internet or, in some cases, over the phone - along with an information booklet called a proxy statement. This statement outlines the circumstances surrounding the vote including new board electives, merger or acquisition approval, stock compensation, inter-office policies etc. Additionally, the proxy statement asserts whether the vote  is:

* **Non-Partial** -- The vote is carried out in a binary type manner, ie: YES, NO or - in some cases - ABSTAIN. In circumstances where a specific candidate or event is being voted for, the voter is only allowed to vote for one candidate. Here the voter is forced to assign the full weight of their shareholding power behind their vote meaning that they are only allowed to vote for one candidate (event) and they are only allowed to vote once. 
* **Partial** -- Depending on the voting circumstances, the voter is able to assign all or only part of their voting power to a candidate (event). This means that the voter is able to vote more than once for multiple different candidates (events), splitting their voting power between candidates in however incremental portion they choose. The voter is able to do this until all of his/her weighting power has been assigned to their chosen voting candidate(s). 

Once the vote is cast, a central tallying authority is responsible for ensuring that the voting process was conducted fairly 
and - depending on the type of system used - the votes have been recorded and tallied correctly ensuring the validity of the winning candidate.

### How does blockPoll improve on these mechanisms?

#### Immutability
The Proof of Work (PoW) consensus protocol used by the Ethereum network ensures that once all nodes have agreed on its state, no one node has the power to falsify the data or to censor changes. As such, once the contract has been deployed and the start block has been mined, no individual can alter the state of the contract and in such disrupt the validity of the vote. Any change to the contract would result in a disagreement between the nodes. This gives both voters and voting candidates the peace of mind that the result of the vote has not been altered or tampered with during its life cycle. This relegates the voters and candidates from the need of a central tallying authority and removes the need to trust in these entities.

#### Auditability and Transparency

Because a blockchain requires that there exist a ledger containing the sequential time-stamped trial of transactions, and these transactions are stored in a sequential array of blocks containing reference to their predecessors, an audible trial of transactions is created which can be publicly viewed. This blockPoll leverages this, allowing voters to validate that their vote has been captured correctly, without revealing to other voters or candidate their identity. This also allows blockPoll to display in real-time (if chosen by the organization) to make public the progress of the election. The API provides a dashboard upon which the progress can be viewed, as well as providing visual metrics should the organization choose to make public the voting progress.

##### Persistence of results

Once created and deployed on the public chain, the contract cannot be destroyed. The data stored by the contact is forever accessible and allows users to see the outcome of an event in the past. This increases both its auditability and immutability as it prevents those with malicious intent to delete the contract in the hope of nullifying the vote.

#### Scalability

blockPoll does not make use of centralized servers. The decentralized nature of the blockchain means that once the contract has been created a deployed, nothing other than a total 51% attack on the ethereum network will prevent the contract from running correctly all the way through to completion. This alleviates the need for trust in central server services, and ensures the immutability and legitimacy of the voting procedure.

#### Cost

Other than the small transaction fee associated with deploying the contract to the network, as well as the almost negligible fee for each voter, the absence of a centralized server alleviates the financial weight of running a proxy (or any other) vote on blockPoll. blockPoll is free to use and open source, and exists therefore only to provide a user friendly blockchain based voting mechanism for the benefit of its own organization. Its open source nature means that any security faults found through testing on the test-net can be resolved timeously to provide a fail-proof robust solution for its users. 

#### Future Proof

Blockchain technology and smart contracts in general are still in the early adoption phase of its life cycle. The entire ecosystem has the potential to grow into one which spans every facet of our lives from how we deal with finance to what goes on in our homes. Being a blockchain based Dapp, blockPoll strives to make use of this evolving technology in a manner that increases efficiency and ease of use in a voting contest. Increased development in the field will bring with it more functionality that blockPoll hopes to employ in the future, should there be a market for it. Its our hope that blockPoll can be used in much larger, more decentralized applications through which any electoral-based projects can make use of the power of blockPoll.  

#### Decentralized


For more option, see [programming API](http://codemirror.net/doc/manuaal.html) of CodeMirror, and Hack [Markdown Edit](http://github.com/georgeosddev/markdown-edit)

### Converter
To Convert markdown to html, Markdown-Edit Use [Github's API](http://developer.github.com/v3/markdown/#render-a-markdown-document-in-raw-mode) as default.<br>
For more infomation, See official Guide
* [GitHub API v3](http://developer.github.com/v3/markdown/)
* [github-flavored-markdown](http://github.github.com/github-flavored-markdown/)

*NOTICE* : [GitHub API v3](http://developer.github.com/v3/#rate-limiting) is limited 5000requests per hour.

#### Option: Use [marked](https://github.com/chjj/marked) as conveter.
If you checked radio `Use marked for conveter` **markdown-edit** use [marked](https://github.com/chjj/marked)
and [highlight.js](http://softwaremaniacs.org/soft/highlight/en/) instad of Github's API.
It is faster than API call and make you enable to use this app at offline.

*NOTICE* : [marked](https://github.com/chjj/marked) does not support Anchor.

### Viewer
To display converted HTML like Github, Markdown-Edit apply github.css from highlight.js and github-style.css inspired by [gollum](https://github.com/gollum/gollum/blob/master/lib/gollum/public/gollum/css/template.css).

```html
<link rel="stylesheet" href="bower_components/highlightjs/styles/github.css">
<link rel="stylesheet" href="css/github-style.css">
```

If you want to see raw html what [Github's API](http://developer.github.com/v3/markdown/#render-a-markdown-document-in-raw-mode) responsed, click `Raw .html` button on navbar.

## Getting Started

### Install On your local PC

#### Download Sources

use git

```bash
git clone http://github.com/georegeosddev/markdown-edit.git
```

Or download from [Here](https://github.com/georgeOsdDev/markdown-edit/zipball/master)

#### Download dependencies

use [bower](http://bower.io/)

```bash
bower install
```


#### Deploy to some web server
To avoid ajax error yous should deploy whole files to some web server.

If you are using mac,
```bash
ln -s /path/to/markdown-edit ~/Sites/markdown-edit
```
Then access http://localhost/~usernamehere/markdown-edit

If you have installed python,this way is very easy.
```bash
cd /path/to/markdown-edit
python -m SimpleHTTPServer 4567
```
Then access http://localhost:4567

*NOTICE* :[Google Chrome](https://www.google.com/intl/en/chrome/browser/) upper v22.0 is most desirable browser.

### usage

#### Read local file
Only text file is enable to read.

#### Save to local
This feature is not implemented yet.<br>
So view file in Raw, and copy it to clipboard,then past it to your file by your self.

#### Auto Reload
If you **checked** Auto Reload.<br>Document will convert into html per 5second if it was changed.

#### shortcut keys
If you **checked** Enable Shortcut Key.<br>These shortcut will be enable.

* Exec convert<br>
Mac : ```⌘ + e```
Win : ```ctrl + e```
* Browse local file<br>
Mac : ```⌘ + o```
Win : ```ctrl + o```
* Read local file<br>
Mac : ```⌘ + r```
Win : ```ctrl + r```
* View Raw .md file<br>
Mac : ```⌘ + m```
Win : ```ctrl + m```
* View Raw .html file<br>
Mac : ```⌘ + h```
Win : ```ctrl + h```
* View html in other window<br>
Mac : ```⌘ + alt + h```
Win : ```ctrl + alt + h```

If your are using chrome,
* Enter Full Screen Mode<br>
Mac : ```⌘ + shift + f```
Win : ```F11```


### Markdown Syntax

This app is based on [github-flavored-markdown](http://github.github.com/github-flavored-markdown/)<br>
If you're not already familiar with Markdown, you should spend 15 minutes and go over the excellent [Markdown Syntax Guide](http://daringfireball.net/projects/markdown/) at Daring Fireball.

You can use markdown syntax and also pure html like this.

###### Sample of Table for two
-------------

```
ID  |Name|Rank
----|----|----
1   |Tom Preston-Werner |Awesome
2   |Albert Einstein |Nearly as awesome
```

become

ID  |Name|Rank
----|----|----
1   |Tom Preston-Werner |Awesome
2   |Albert Einstein |Nearly as awesome

and

```html
<table>
  <tr>
    <th>ID</th><th>Name</th><th>Rank</th>
  </tr>
  <tr>
    <td>1</td><td>Tom Preston-Werner</td><td>Awesome</td>
  </tr>
  <tr>
    <td>2</td><td>Albert Einstein</td><td>Nearly as awesome</td>
  </tr>
</table>
```

also become

<table>
  <tr>
    <th>ID</th><th>Name</th><th>Rank</th>
  </tr>
  <tr>
    <td>1</td><td>Tom Preston-Werner</td><td>Awesome</td>
  </tr>
  <tr>
    <td>2</td><td>Albert Einstein</td><td>Nearly as awesome</td>
  </tr>
</table>


## Special Thanks
 * [CodeMirror](http://codemirror.net/).
 * [Github](http://developer.github.com/) for API and style.
 * [marked](https://github.com/chjj/marked).
 * [highlight.js](http://softwaremaniacs.org/soft/highlight/en/).
 * [Twitter Bootstrap](http://twitter.github.com/bootstrap/) with [Font Awesome](http://fortawesome.github.com/Font-Awesome/).
 * [HTML5 ★ BOILERPLATE](http://html5boilerplate.com/).
 * [jQuery](http://jquery.com/).
 * [HTML5 ROCKS](http://www.html5rocks.com/en/tutorials/file/xhr2/) for usage of BLOB.
 * [balupton](https://github.com/balupton).

## Licence

Source code can be found on [github](https://github.com/georgeOsdDev/markdown-edit), licenced under [MIT](http://opensource.org/licenses/mit-license.php).

Developed by [Takeharu.Oshida](http://about.me/takeharu.oshida)

    



