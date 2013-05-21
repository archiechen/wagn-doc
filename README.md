wagn-doc
========

1. Cards

  Not only is all the text on Wagn stored in cards, but images, files, users, settings, and searches are all cards.

  Tips
  * To make a link to create a new card: /card/new (see web address for everything).
  * To make links that create new cards of a specified type, use something like: /new/Recipe

1. Editing

  To edit a card, click on its Edit tab, or double-click anywhere in the content of the card.

  Some card types, like Images, Files, Pointers and Dates, have different editors. If you edit an image or file, for example, you'll see a "Browse" button that lets you select a file on your computer

1. Card Types

  Card Types are a powerful tool for organizing information on Wagn. Every card has a type, and that type shapes what kind of information goes into each card. 
    * Basic
    
      Rich text, and it's the default cardtype.  Uses a simple wysiwyg editor.
    * Html
    
      HTML cards let you add in and keep all the HTML you like. 
    * File
    
      On Wagn you upload files to File cards, then include the cards wherever you want a link to the file to appear.
    * Image

      To use a photograph or picture or any kind of image in Wagn:
      + Including image cards
      + Sizing and location

          {{nymph|size:small}} {{nymph|float:left}}
      + Images as links

          [[Grass Commons|{{Grass Commons+logo}}]]
    * Phrase & PlainText

      Phrase cards contain text, much like Basic cards, but without linking or bold, italics, and other layout and styling.
      PlainText are the same except that the editing area is a few lines long.
    * Pointer

      Pointer cards let you create and maintain lists of cards.

    * Search

      Search cards let you query for cards using the Wagn Query Language (WQL, pronounced "wuckle") .

      { "type": "User" }

    * Set + Setting = Rule

      A set is a card that defines a group of cards.
      + all (All Cards)
      + Basic+*type (All Basic Cards)
      + Wiki on Wheels+*self (Just "Wiki on Wheels")


1. Inclusion
  
  Cards can include other cards inside them.
    * Edit inclusions in place, making them faster and easier than editing whole pages.
    * Keep data current. a card's updates (e.g., an address or event info) appear everywhere it's included.
    * Display the same card in different ways using inclusion views.  Eg, closed view let you use space more efficiently.
    * Specify content patterns with inclusion-based formats.

  {{Wiki on Wheels}}

  {{Wiki on Wheels|open}}

  {{Wiki on Wheels|closed}} 

  {{nymph|name}}

  {{nymph|link}}

  Specifying view of cards in lists

  {{sample user search | open; item:link}}

  Tips
    * You can edit included cards by double-clicking anywhere in them, or clicking on the Edit in the enclosing card's header.
    * Inclusions are inline, so you can use them in a sentence.
    * When you're including a card that doesn't exist yet, you can specify what type it should be with something like {{Tel|type:Phrase}}. 

1. Formatting
  
  Forms are content patterns.
  Forms are settings, meaning configurations that can apply to any set of cards.
    * default

      The *default setting controls the initial content for cards in a set.  If you change a *default setting, it won't impact existing cards in the set.
    * structure  

      The *structure setting controls the structure of cards in a set on an ongoing basis.  If you change a *structure setting, it will impact every card in the set.

  Tips
    * Checkboxes, radio buttons, and other form elements can be added using Pointers.
    * You can add help text that shows up when inclusions are being created or edited.




