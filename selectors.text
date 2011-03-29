Usable Selectors for Cocoa Key Bindings
=======================================

  by Jacob Rus  
  Friday, 17 March 2006


We can use a very wide variety of selectors in our key bindings. Note, if you
find more usable selectors, please let me know about them. Thanks.

## Generally-applicable selectors

  * `cancelOperation:` -- "cancel the current operation."

  * `showContextHelp:` -- "invoke the help system, displaying information 
    relevant to the receiver and its current state. The sender argument is 
    typically the object that invoked this method."

### Undo/redo ###

  * `undo:`
  * `redo:`

  * `breakUndoCoalescing` -- this one sets up an undo state.  So if some more 
    text is typed, and then undo is invoked, it will come back to this point.


## Text manipulation

These selectors are for inserting, selecting, deleting, and moving text.


### Inserting text ###

In general, these selectors: "Insert a ... at the insertion point or selection, deleting the selection if there is one"
    
  * These two also "end editing if the receiver is a text field"
  
      * `insertTab:`
      * `insertNewline:`

  * These selectors should be used to avoid tabbing out of, for instance, a
    form field

      * `insertTabIgnoringFieldEditor:`
      * `insertNewlineIgnoringFieldEditor:`

  * `insertLineBreak:`
  * `insertParagraphSeparator:`
  * `insertContainerBreak:`

  * `insertBacktab:` --  "handle a 'backward tab'"

  * `insertText:` -- my favorite selector, "insert a string at the insertion 
    point or selection, deleting the selection if there is one."

### Deleting text ###

This group of selectors simply wipes text off the face of the planet.

  * `delete:` -- "deletes the selected text only"

  * `deleteBackward:`  
  * `deleteForward:`
  * `deleteWordBackward:`  
  * `deleteWordForward:`

  * `deleteBackwardByDecomposingPreviousCharacter:` -- "If the previous 
    character is canonically decomposable, try to delete only the last 
    character in the grapheme cluster (for example, deleting “a”+ “´” results 
    in “a”)"


### Killing and yanking text ###

These selectors delete text, but also put it onto the kill ring (which means that it can be "yanked back later"):

  * `deleteToBeginningOfLine:`  
  * `deleteToEndOfLine:`

  * `deleteToBeginningOfParagraph:`  
  * `deleteToEndOfParagraph:`

  * `deleteToMark:` -- "Delete all items from the insertion point to a 
    previously placed mark, including the selection itself if not empty."

This one brings back text:

  * `yank:` -- "Replaces the insertion point or selection with text from the 
    kill buffer."

### Change the case of the selected text ###

"change the case of a letter or letters in the selection, perhaps by opening a panel with capitalization options or by cycling through possible case combinations."

  * `changeCaseOfLetter:`
    
"set the case of the word or words surrounding the insertion point or 
selection, expanding the selection if necessary"

  * `lowercaseWord:`
  * `uppercaseWord:`
  * `capitalizeWord:`


### Moving the insertion point ###

"move the selection or insertion point one element or character"

  * `moveBackward:`  
  * `moveForward:`
  * `moveLeft:`  
  * `moveRight:`
  * `moveUp:`
  * `moveDown:`

"move the selection or insertion point one word..."

  * `moveWordBackward:`
  * `moveWordForward:`
  * `moveWordLeft:`
  * `moveWordRight:`

"move the selection to... or the insertion point to..."

  * `moveToBeginningOfLine:`
  * `moveToEndOfLine:`
  * `moveToBeginningOfParagraph:`
  * `moveToEndOfParagraph:`
  * `moveToBeginningOfDocument:`
  * `moveToEndOfDocument:`

"scroll the receiver... one page in its scroll view, also moving the insertion 
point to the top of the newly displayed page."

  * `pageUp:`
  * `pageDown:`


### Scroll the text view ###

"scroll the receiver... in its scroll view, without changing the selection"

  * `scrollLineUp:`
  * `scrollLineDown:`
  * `scrollPageUp:`
  * `scrollPageDown:`


"scroll the selection, whatever it is, inside its visible area."

  * `centerSelectionInVisibleArea:`

### Move the insertion point and modify the selection ###

"expand or reduce either end of the selection by one element or character"

  * `moveBackwardAndModifySelection:`
  * `moveForwardAndModifySelection:`
  * `moveLeftAndModifySelection:`
  * `moveRightAndModifySelection:`
  * `moveUpAndModifySelection:`
  * `moveDownAndModifySelection:`

"expand or reduce either end of the selection... by one whole word"

  * `moveWordBackwardAndModifySelection:`
  * `moveWordForwardAndModifySelection:`
  * `moveWordLeftAndModifySelection:`
  * `moveWordRightAndModifySelection:`

Apparently some of the options are undocumented, but work just fine

  * `moveToBeginningOfDocumentAndModifySelection:`
  *	`moveToEndOfDocumentAndModifySelection:`
  *	`moveToBeginningOfLineAndModifySelection:`
  *	`moveToEndOfLineAndModifySelection:`
  *	`moveToBeginningOfParagraphAndModifySelection:`
  *	`moveToEndOfParagraphAndModifySelection:`
  * `pageUpAndModifySelection:`
  * `pageDownAndModifySelection:`


### Select text ###

"select..."

  * `selectAll:`
  * `selectLine:`
  * `selectParagraph:`
  * `selectWord:` -- "extend the selection to the nearest word boundaries
    outside it (up to, but not including, word delimiters)."
  * `selectToMark:` -- "select all items from the insertion point or selection
    to a previously placed mark, including the selection itself if not empty."


### Working with marks ###

  * `setMark:` -- "set a mark at the insertion point or selection, which is
    used by deleteToMark: and selectToMark:"

  * `swapWithMark:` -- "swap the mark and the selection or insertion point, so
    that what was marked is now the selection or insertion point, and what was
    the insertion point or selection is now the mark."

  * `selectToMark:` -- "select all items from the insertion point or selection
    to a previously placed mark, including the selection itself if not empty."

  * `deleteToMark:` -- "delete all items from the insertion point to a
    previously placed mark, including the selection itself if not empty."



### Other text editing options ###

  * `complete:` -- "complete an operation in progress or a partially 
    constructed element."
  
  * `indent:` -- "indent the selection or the insertion point if there is no 
    selection."
  
  * `transpose:` -- "Transposes the characters to either side of the insertion 
    point and advances the insertion point past both of them. Does nothing to 
    a selected range of text."
  
  * `transposeWords:` -- "Transposes the words to either side of the insertion 
    point and advances the insertion point past both of them. Does nothing to 
    a selected range of text."



### Cut/Copy/Paste ###

  * `copy:` -- "copies the selected text onto the general pasteboard, in as 
    many formats as the receiver supports."
    
  * `cut:` -- "deletes the selected text and places it onto the general 
    pasteboard, in as many formats as the receiver supports."
    
  * `paste:` -- "pastes text from the general pasteboard at the insertion 
    point or over the selection."


  * `pasteAsPlainText:` -- "inserts the contents of the pasteboard into the 
    receiver’s text as plain text, in the manner of insertText:."

  * `pasteAsRichText:` -- "inserts the contents of the pasteboard into the 
    receiver’s text as rich text, maintaining its attributes."

  * Copy/paste fonts:

      * `copyFont:` -- "copies the font information for the first character of 
        the selection (or for the insertion point) onto the font pasteboard, 
        as NSFontPboardType."
    
      * `pasteFont:` -- "pastes font information from the font pasteboard onto 
        the selected text or insertion point of a rich text object, or over 
        all text of a plain text object."

  * Copy/paste ruler:
  
      * `copyRuler:` -- "copies the paragraph style information for first 
        selected paragraph onto the ruler pasteboard, as NSRulerPboardType, 
        and expands the selection to paragraph boundaries."
    
      * `pasteRuler:` -- "pastes paragraph style information from the ruler 
        pasteboard onto the selected paragraphs of a rich text object."


## Text Styles and formatting (mostly applies to rich text) ##


### Set the text alignment ###

"applies ... alignment to selected paragraphs (or all text if the receiver is 
a plain text object)"

  * `alignCenter:`
  * `alignLeft:`
  * `alignRight:`
  * `alignJustified:`

"changes the base writing direction of a paragraph, for languages like Hebrew 
and Arabic, for example."

  * `toggleBaseWritingDirection:`
  * `changeBaseWritingDirectionToRTL:`
  * `changeBaseWritingDirectionToLTR:`


### Superscript/subscript ###

  * `superscript:` -- "applies a superscript attribute to selected text (or
    all text if the receiver is a plain text object), raising its baseline
    offset by a predefined amount."

  * `subscript:` -- "applies a subscript attribute to selected text (or all
    text if the receiver is a plain text object), lowering its baseline offset
    by a predefined amount."

  * `unscript:` -- "removes any superscripting or subscripting from selected
    text (or all text if the receiver is a plain text object)."


### Underline/outline ###

  * `underline:` -- "underlines selected text for a rich text object, or all
    text for a plain text object."

  * `outline:`


### Baseline, kerning, ligatures ###

Set the baseline of the text.

* `lowerBaseline:` -- "lowers the baseline offset of selected text by 1 point,
  or of all text if the receiver is a plain text view."

* `raiseBaseline:` -- "raises the baseline offset of selected text by 1 point,
  or of all text if the receiver is a plain text view."


Set the kerning to be used for the text.


  * `useStandardKerning:` -- "cause the receiver to use pair kerning data for
    the glyphs in its selection, or for all glyphs if the receiver is a plain
    text view."

  * `turnOffKerning:` -- "cause the receiver to use nominal glyph spacing for 
    the glyphs in its selection, or for all glyphs if the receiver is a plain 
    text view."

  * `loosenKerning:` -- "increase the space between glyphs in the receiver’s
    selection, or in all text if the receiver is a plain text view."

  * `tightenKerning:` -- "decrease the space between glyphs in the receiver’s
    selection, or for all glyphs if the receiver is a plain text view."


Tell the selection whether to use standard ligatures, or all ligatures.

  * `useStandardLigatures:` -- "cause the receiver to use the standard
    ligatures available for the fonts and languages used when setting text,
    for the glyphs in the selection if the receiver is a rich text view, or
    for all glyphs if it’s a plain text view."

  * `turnOffLigatures:` -- "cause the receiver to use only required ligatures
    when setting text, for the glyphs in the selection if the receiver is a
    rich text view, or for all glyphs if it’s a plain text view."

  * `useAllLigatures:` -- "cause the receiver to use all ligatures available
    for the fonts and languages used when setting text, for the glyphs in the
    selection if the receiver is a rich text view, or for all glyphs if it’s a
    plain text view."

  * `toggleTraditionalCharacterShape:` -- "toggle the
    NSCharacterShapeAttibuteName attribute at the current selection."


### Open up useful panels for text formatting ###

  * `orderFrontLinkPanel:` -- "bring forward a panel allowing the user to
    manipulate links in the text view."

  * `orderFrontListPanel:` -- "bring forward a panel allowing the user to
    manipulate text lists in the text view."

  * `orderFrontSpacingPanel:` -- "bring forward a panel allowing the user to
    manipulate text line heights, interline spacing, and paragraph spacing, in
    the text view.

  * `orderFrontTablePanel:` -- "bring forward a panel allowing the user to
    manipulate text tables in the text view."


## Spelling and speech ##


Check the spelling of the text view:

  * `toggleContinuousSpellChecking:` -- "toggle whether continuous spell
    checking is enabled for the receiver."

  * Perform spell checking. If I remember, the first one of these simply
    selects a misspelled word. The second one opens the spelling panel, and
    the third one tells the spelling system to ignore the selected word. I'm
    not positive of that however.

      * `checkSpelling:` -- "search for a misspelled word in the receiver’s 
        text."

      * `showGuessPanel:` -- "open the Spelling panel, allowing the user to 
        make a correction during spell checking."

      * `ignoreSpelling:`

OS X Speech synthesis:

  * `startSpeaking:` -- "speak the selected text, or all text if no 
    selection."

  * `stopSpeaking:` -- "stop the speaking of text."


## Window and document options ##


### Printing ###


  * `printDocument:` -- "bring up print sheet"

  * `runPageLayout:` -- the same thing happens as when the user chooses the
    Page Setup menu command.


### Closing, saving, reverting documents ###

These do the same as the menu options of the same name:
  
  * `save:`

  * `saveAs:`

  * `saveTo:`

  * `revert:`

  * `performClose:` -- "simulate the user clicking the close button by
    momentarily highlighting the button and then closing the window."

<!--
    
  * `new:`
    
  * `openDocument:`

  * `saveAllDocuments:`
    
  * `clearRecentDocuments:` - "empty the recent documents list for the
      application."
-->



### Window manipulations ###

These three simulate clicking the little gem buttons in the top left corner of
the window. Note that `close:`, etc. are also usable selectors, but not
advisable, as they act slightly differently. Most importantly, `close:`
doesn't prompt the user to save changes to unsaved documents, so data loss is
possible if it is used:

  * `performClose:`
  * `performMiniaturize:`
  * `performZoom:`

These change window ordering or position:

  * `center` -- "set the window’s location to the center of the screen."

  * `orderBack:` -- move the window behind all the other windows, without
    changing either the key window or the main window.

  * `orderFront:` -- move the window in front of all the other windows,
    without changing either the key window or the main window.


This one hides the application:

  * `hide:` -- "Hide all the application’s windows, and the next application
    in line is activated."
