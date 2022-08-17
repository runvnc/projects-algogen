
# ALGOGEN (runvnc) Algorand Projects
_algogen.algo_

## gifeconomy.com
(In Production, specific improvements planned)

NFT Marketplace

_75% Owner -- Devon Hurt (dhurtknobs). Devon hired me to build an NFT Marketplace and his sponsorship of the project
allowed me to train up on Algorand development._

gifeconomy has unlockable content (access by signing and then verifying a 'dummy' transaction),
auctions and direct sales. Also a simple NFT gallery accessible via VR headset.

First UI design was scrapped, second not yet finished. Have a third design started by a volunteer (iamp2.algo), have not
had time to start trying to integrate it.

## Tealang
(In "Production" (not actively used))

Some minor but useful improvements to the Tealang compiler (Go-like language compiles to TEAL).
https://github.com/runvnc/tealang

## genpyteal
(Released, in use in own projects)

Python program that generates PyTeal from Python. Reduces the awkwardness and verbosity of PyTeal.
Simplifies ARC4 ABI routing. Generates interface files.

### Planned improvements (no time/resources):
 
* very redundant call graph, much room for performance improvement

* dictionary-like access to Box storage

* watch files for changes

* use Levenshtein distance to provide rough source lines from PyTeal compile errors

* web page to provide simple Python -> PyTeal conversion, possible ARC4 contract registry, etc.


## avmjs and "Adventure game" genpyteal demo

Demo ARC4 ABI genpyteal features and ARC4 command line interface (avmjs) with a simple game involving somewhat interesting state
and a "store".

https://youtu.be/WiiVs-C2BN8

https://github.com/runvnc/avmjs

## algofilter

Modular pipelines for processing Algorand transaction data
https://github.com/runvnc/algofilter


## algonfts.art Algorand NFT Generator and minter
(In Production)

Web application for uploading variant images, specifying rarity, conflicts, etc. 
Includes built-in code editor for procedural generation.
Provides pinning service with uploads to both web3.storage and Filebase.io.

Creates Arc69 metadata and mints on the Algorand blockchain. Modest fee (0.07 ALGO)
per item minted.

### ⚡⚡ Arc19 minting
(Planned)

* Mint modifyable NFTs using Arc19. 

* Add input field to allow specifying an already-minted Arc19 asset to overwrite during minting.

* Add Upgrade price and Upgrade only column to application. (Embeddable?) Web page allowing
purchase of variants and reminting over item.

* Evolution. Add sections to the algonfts.art interface, so that creators can specify different parameters
for each stage of generation (tracked with a Stage/Phase/Generation trait). Create a web page, API endpoint, iframe or embeddable script so that creators can integrate this.

## Matthias Trinley figures generation
(In Production)

_Partially sponsored by Matthias Trinley_

Create characters using algonfts.art code generation interface. Secondary store contract calls backend contract
monitored by block watcher to trigger image generation, pin, mint and transfer back to store.

## algonfts.art extra tools

### Drop Manager

_Partially sponsored by Matthias Trinley_

Create opt-in link for up to 3 assets. View all holders, randomly assign token amounts weighted by holdings.
Execute transfers. Show history of drops and all holdings.

###  Swap and Sale creator

_Partially sponsored by Matthias Trinley_

Embeddable (iframe) swap or sale

### Holders

Show all holders and amounts of a collection

### ⚡ NFTGEN API
(In Progress)

Planned to release an open API exposing the algonfts.art generation and pinning services over HTTP. This will allow
projects to leverage their image assets and configuration for many types of applications.

Tentative endpoints:

* `generate_image(s) [force variants]`

Generates one or more images using the image and other NFT configuration data, optionally specifiying
some variants (otherwise random according to config)
Returns metadata

* `pin`

Pin an NFT

* `mint [overwrite Arc19 assetid]`

This can be less than ideal because applications may prefer to have the minting atomic with other application-specific transactions
 (as is the case with the burn-to-mint Discord bot).


* `recordMint`

Record an NFT's CID (used to prevent duplicate generation).


## gifeconomy.com Inst-a-Mint
(In Production, specific improvements planned)

_Partially sponsored by AlgoTheOwl_

Essentially a proof-of-concept for an early version of the NFTGEN API.

Integration allowing gifeconomy.com to leverage the generation and pinning service of algonfts.art
to provide a burn-to-mint system where Discord users can easily "re-roll" NFTs to improve their rarity or
other desirable traits.

Configuration of tokens, pricing, logicsig signing through gifeconomy site.

LogicSigs enable mint, transfers, payment, burn to be atomic.

⚡ Planned: (non-burn) mint-on-demand Discord bot, leveraging existing burn-to-mint code.

## Alvatars

### Image Generation
(In Production)

Custom LiveScript code using algonfts.art infrastructure to generate tiles for the Alvatars game according to their specifications.

### Alvatars Tile Upgrades
(Should deploy August 19)

Using the algonfts.art infrastructure to generate, pin and mint replacement NFTs for the Alatars Tile game.
Non-foil system in place, more expensive "foil" tiles in testing and should be in production by Friday.

## ⚡ vrfshuffle.com
(In progress, investigatory stage)

_Partially sponsored by AlgoWhales_

Shuffle system, ideally taking advantage of the new VRF feature to be released in the next AVM. 
Should have good UX for transferring NFTs to the shuffle wallet.

## ⚡ algobreeder.com
(Planned)

Website to randomly combine traits from two (arc69?) NFTs (possibly allow some trait selection).
Will probably burn one or more of the "parents" ('deflation' strongly requested by AlgoTheOwl).


## ALGOGEN Engineering website
(In Progress, barely)

Just barely started a website for an entity called ALGOGEN with the theory that someday I would have money to hire help
and then would call it ALGOGEN Engineering Group or something.
Have a very simple page started and a logo.

## Miscellaneous

There are a few (hopefully smaller projects?) collaborations that don't necessarily have specific dates or plans at this point
but have had serious discussion (middledoug, faun). Or that I just forgot about. Hopefully they will remind me.


