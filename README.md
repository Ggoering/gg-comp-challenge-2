#Static Comp Challenge #2

## Requirements  
The objective of this project was to create a webpage layout that took 8 "cards" and placed them in the page underneath a primary and secondary header.  The cards, as well as the header elements are to keep their shape at all screen widths down to 320px, and have their layouts match the design composition of the sample image.  

### Design Approach  
The webpage was designed as a fake betting / fantasy bracket site for the World Warrior tournament from the Street Fighter universe.  Users can bet on their favorite fighter, check out the statistics for each fighter via the cards, and see how many others have chosen each particular fighter as their favorite to win the tournament within each of their leagues.  A risky pick background of diamond textured steel plate was chosen to match the tone of a tough & rugged single combat tournament.  Primary colors are gray, dark gray, and crimson.  The dark gray and gray closely match the colors of the background, and crimson is used for links, the logo, and important text.  White was chosen for the logo text for purposes of contrast and emphasizing special importance.  
The font impact was another risky pick, but was chosen because it nicely accented the art of the characters, and matched with the video game theme.

### Technical Approach  
The card contents are wrapped in a div with the display: flex property, as well as flex-wrap and they are justified left.  This ensures the cards will remain lined up at all widths, with no widows.  There are 4 media queries for the page.  The site was built first at a widescreen mobile view, and adjusted for screens accommodating 2, 3, and 4 columns of cards.  The 4th media query is for very small screens, which simply shrinks the size of all elements on the page proportionally so that an entire card can fit in a 320px screen.  

### Difficulties
 * When using the display: flex property on the containing element of the cards, this containing element could not be easily centered in the page.  Margin: 0 auto had no affect, and as screen width increased the page looked heavily unbalanced just before a new column of cards was displayed.  Furthermore having this element automatically adjust its width as its contents shifted also did not have a straightforward solution.  To solve this issue the flexing element was contained in another element, which at each media query had a max width setting.  This new, larger container could accept the margin: 0 auto; setting, and kept the content centered in the page nicely.  
 * The same trick was used on the secondary header.  It looked better to keep the secondary header text aligned with the left edge of the leftmost card.
