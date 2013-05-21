wagn-doc
========

1. Cards

  Not only is all the text on Wagn stored in cards, but images, files, users, settings, and searches are all cards.

  Every card has a unique name.

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

1. Plus Cards

  Plus cards are cards with a "+" in the name.
  Creating a plus card automatically creates a card for each of its parts (unless they already exist).

  Suppose we create a card named Joe's Coffee+hours.  
 
  When we see this plus card, we know that we have two other cards: one named Joe's Coffee, and another named hours.  If they didn't already exist when we created the plus card, then they were created automatically.

  More than one plus, a plus card can have more than one "+".  E.g. Joe's Coffee+menu+specials.

1. Contextual Names

  Contextual (or "relative") names are card names that can be interpreted differently based on context.

  A few examples of contextual names:
    * _
    * _self
    * _user
    * +address
    * _left+address

  Card Content

    Our planet is named {{_self|link}}. {{_|name}} has seven continents.  See [[+continents]]

  Plus Card Content

    Australia, Asia, Africa, Europe, Antarctica, and North and South America are all [[_right]] on planet [[_left]].

  Tips
    * These terms can be used as variables in regular web addresses.

      [[http://{{Google base URI|raw}}{{_right|name}}]]
    * In the context of Searches, _self refers to the left side of the card's name.

      E.g., if John+friends is a Search card, then _self  refers to John, not John+friends. 

1. Views
  
  Views are most often applied via inclusions or WQL, and are especially useful in formatting.
    * content (default for inclusions) — shows the content of the card, without the surrounding card interface
    * titled — content view, but after a header of the card's name. You can also make the title different from the card's actual name with "title:yournewtitle" in the inclusion markup
    * open / closed — both show the content inside the surrounding card interface. Closed is the default for items in Searches and Pointers)
    * labeled — card title followed by what content will fit on a single line, formatted so that the labels/content of multiple such inclusions line up
    * link — instead of the card content, this just shows a link to the card, very much like using double square brackets for linking
    * name — instead of the card content, this just shows the card's name
    * linkname — like name, but puts in underscores instead of spaces (helpful when using inclusions to build URLs)
    * url — shows the full, canonical URL for the card
    * change — only applies to items in Searches and Pointers, showing who last edited each card and when. This is the view used on Recent.
    * core — shows the processed card content without any enclosing HTML
    * raw — shows the unprocessed card content, including markup. Note that any HTML will still be interpreted by your browser.

  When including a Search or Pointer, you can also specify the view for each item (card) in the returned list, e.g., {{User+*type cards|item:link}}

  In WQL syntax, item views are applied with WQL's usual key/value syntax, e.g.: {"type":"User", "view":"link"}

  In special web addresses, you append views after a normal web address with "?view=" or "?item=", e.g. http://wagn.org/wagn/Fruit?view=closed or http://www.wagn.org/wagn/Image+*type+by_update?item=change

  Tips
    * In addition to setting a view for an inclusion, you can show and hide pieces of a view. To use more than one, separate them with a comma. Here are some that work and in what context:
        + hide:menu on any view that has the menu - titled, open, and closed
        + hide:paging on Searches
        + show:comment_box will show the add-a comment box at the bottom of the card
        + show:title_link will make the title a link to the card (in titled and open/closed - any view that shows the title)
    * The name and linkname views are especially useful for contextual web addresses.
 
1. Comments

  Wagn lets you enable commenting on a card with a friendly comment box. User comments simply get added to the end of the card's content.

  To let someone who is signed in be able to comment on a card, go to it's rules, click on the menu to the left of "...can comment on this card", select "Anyone signed in" and click "Save Changes".

  You can't add comments to cards controlled by a *structure rule, but you can include a commentable card on them. For example the +discussion card below appears because "+discussion" is included.