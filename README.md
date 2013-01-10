#Generic product reviews & rating
  
## Version
current version: 0.1.0  
   
   

## Documentation
### Table of contents  
1. **[Example](https://github.com/karolgorecki/generic-product-rev#example)**
1. **[Requirements](https://github.com/karolgorecki/generic-product-rev#requirements)**
1. **[Variables](https://github.com/karolgorecki/generic-product-rev#variables)**
1. **[Display options](https://github.com/karolgorecki/generic-product-rev#display-options)**
1. **[Misc](https://github.com/karolgorecki/generic-product-rev#misc)**
1. **[HTML Structure](https://github.com/karolgorecki/generic-product-rev#html-structure)**
1. **[Cross-browser](https://github.com/karolgorecki/generic-product-rev#cross-browser)**
1. **[TODO](https://github.com/karolgorecki/generic-product-rev#todo)**

## Example
### [http://karolgorecki.github.com/generic-product-rev/](http://karolgorecki.github.com/generic-product-rev/)


## Requirements
* **[reviews.less](https://github.com/karolgorecki/generic-product-rev/blob/master/less/reviews.less)**
* **[reviews-variables.less](https://github.com/karolgorecki/generic-product-rev/blob/master/less/reviews-variables.less)** - generic product review variables
* **[reviews-custom.less](https://github.com/karolgorecki/generic-product-rev/blob/master/less/reviews-custom.less)** - to make custom style
* **[Fonts](https://github.com/karolgorecki/generic-product-rev/tree/master/fonts)** - using Font Awesome
* **[Images](https://github.com/karolgorecki/generic-product-rev/tree/master/images)** - for star rating
* **[JQuery Rating](http://www.fyneworks.com/jquery/star-rating/)** - jquery rating script to enable rating
* **[Less](http://lesscss.org/)**
* **[Twitter Bootstrap](http://twitter.github.com/bootstrap/)**
* **[JQuery library](http://code.jquery.com/jquery.min.js)**

## Variables
All variables starting with *@rev* prefix.

![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/rev-block.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/rev-block.gif)
![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/rat-block.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/rat-block.gif)

#### Typography
##### General
* **@rev-base-font-family** - base font family for the blocks
* **@rev-base-font-size** - base font size for the blocks. Used to calculate other default sizes.
* **@rev-base-line-height** - base line height

##### Review-block typography
######Main title  
* **@rev-main-title-color** - the main title color in *reviews-block* and *rating-block*  
* **@rev-main-title-font** - font of the main title in reviews and rating block

######Review content
* **@rev-content-font** - review content font style
* **@rev-content-font-column** - review content when reviews are displayed in columns
* **@rev-content-align-column** - text align of review displayed in column

######Date  
* **@rev-date-color** - color of posted on date
* **@rev-date-font** - font of review-date

######Author  
* **@rev-author-color** - color of review author  
* **@rev-author-font** - font of review author

######Summary  
* **@rev-summary-color** - color of review summary  
* **@rev-summary-font** - review summary font style
* **@rev-summary-font-column** - review summary font style when displayed in column

######Numbering /counter
* **@rev-numbering-font** - font style of the numbering at corner
* **@rev-numbering-color** - text color

##### Rating-block typography
######Subtitle
* **@rev-sub-title-color** - subtitle color
* **@rev-sub-title-font** -subtitle font style

######Rating stars heading
* **@rev-rating-heading-font** - font properties for rating stars heading
* **@rev-rating-heading-color** - color for rating start heading

######Rating labels
* **@rev-rate-label-color** - color of label for star rating
* **@rev-required-color** - color of the asterix in required inputs
* **@rev-rate-label-font** - font properties for label star rating

######Ratting submit button
* **@rev-rating-submit-btn-font** - font properties for submit button
* **@rev-rating-submit-btn-color** - text color


######Inputs and textareas
* **@rev-input-font-family** - font family for inputs and textareas
* **@rev-rate-input-color** - inside input and textarea text color

#### Blocks
##### Review-block
######Single review
* **@rev-single-bgcolor** - background color for single review row/col
* **@rev-single-padding** - padding
* **@rev-single-striped-power** - defines the darken value for striped bg

######Review content overlay (.display-column)
* **@rev-column-overlay-direction** - overlay vertical position (top/bottom)
* **@rev-content-overlay-bshadow** - defines box shadow
* **@rev-content-overlay-bgcolor** - background color for the overlay
* **@rev-content-overlay-color** - text color in overlay

######Review content
* **@rev-content-max-width** - the max width of the review content box
* **@rev-content-padding** - padding of the review content box

######Numbering counter
* **@rev-numbering-size** - size of the number box
* **@rev-numbering-bgcolor** - background color

##### Rating-block
######Rating inputs textareas
* **@rev-rate-top-spacing** - the space between elements such as inputs, textareas (li padding top)
* **@rev-rate-input-padding** - input padding
* **@rev-rate-textarea-padding** - textarea padding
* **@rev-rate-input-box-shadow** - box shadow of inputs, textareas
* **@rev-rate-bgcolor** - background color (will be used for creating gradient)
* **@rev-rate-input-border** - border properites for inputs and textareas

######Submit rating button
* **@rev-rating-submit-btn-border** - border properties for submit button
* **@rev-rating-submit-btn-bg** - background color
* **@rev-rating-submit-btn-bshadow** - box shadow
* **@rev-rating-submit-btn-height** - height of the button
* **@rev-rating-submit-btn-fsize** - font size of text
* **@rev-rating-submit-btn-icon-size** - size of the icon

#### Theme Variables
* **@rev-rating-theme** - can be used to switch theme

#### Turn on/off elements
######To hide element just add *false* value.
* **@rev-SUMMARY**
* **@rev-AUTHOR**
* **@rev-CONTENT**
* **@rev-DATE**
* **@rev-RATING**
* **@rev-NUMBERING**
* **@rev-QUOTES**

Example  
This will hide the *review-author* block  

    @rev-AUTHOR: false;

## Display options
##### Striped background
![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/striped.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/striped.gif)
Just add *striped-bg* class to reviews-block, to darken background of every second single-review block.

    <div class="reviews-block striped-bg">
      ...
    </div>
    
##### Display reviews in columns
![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/col.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/col.gif)
To display single-review in column add *display-column* to reviews-block.
```html
<div class="reviews-block display-column">
  ...
</div>
```    
##### Enable icon in submit button
![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/btn.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/btn.gif)
To enable display icon in submit button add *icon* class to rating-submit-btn.
```html
<button type="submit" class="rating-submit-btn icon">
  Add Your Rating
</button>
```    
##### Required input
![https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/req.gif](https://raw.github.com/karolgorecki/generic-product-rev/master/docs_img/req.gif)
To make an label have required state (asterix appear) just add to label class *required*
```html
<label class="rate-label required" for="nickname_field">
  Nickname
</label>
```
## Misc
##### Using star rating
To set value of the star rating use *data-rating*
```html
<div class="rating" data-rating="2" title="Quality">
  <span itemprop="ratingValue">2</span>
</div>
```
    
## HTML Structure
### Reviews block
``` html
<!-- $[REVIEWS-BLOCK] -->
<div class="reviews-block striped-bg">
  		
	<!-- $[MAIN-TITLE] -->
	<div class="main-title">Reviews block</div>
			
		<!-- $[REVIEWS] -->
		<div class="reviews" itemscope itemtype="http://schema.org/Product">
			<meta itemprop="name" content="Product Name" />

			<div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
				<meta itemprop="ratingValue" content="4.5" />
				<meta itemprop="reviewCount" content="23">
				<meta itemprop="bestRating" content="5" />
			</div>

			<!-- single review -->
			<div class="single-review" itemprop="review" itemscope itemtype="http://schema.org/Review">

				<div class="review-summary" itemprop="name">I Feel Very Protected and Secure I Feel Very Protected and Secure</div>

				<div class="review-author" itemprop="author">by John Doe</div>
				
				<div class="review-content" itemprop="description">I am very happy that I have chosen Kaspersky for my virus protection software! My previous software was up for renewal and therefore it was perfect timing to switch to Kaspersky, I'm glad I did!
				</div>
				
				<div class="review-date"><meta itemprop="datePublished" content="2013-01-04" />posted on 2013-01-04</div>
				
				<div class="review-rating" itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
					<meta itemprop="worstRating" content="1" />
					<div class="rating" data-rating="2" title="Quality"><span itemprop="ratingValue">2</span></div>
					<meta itemprop="bestRating" content="5" />
				</div>

			</div><!-- end single review -->

	</div><!-- $[end-REVIEWS] -->
</div><!-- $[end-REVIEWS-BLOCK] -->
```

### Rating block
``` html
<!-- $[RATING-BLOCK] -->
<div class="rating-block">

  <!-- $[MAIN-TITLE-RATING] -->
	<div class="main-title">Rate this product</div>
	<div class="sub-title">you're reviewing Product Name</div>

	<form>
		<ul>
			<!-- Star rating -->
			<li>
				<div class="rating-heading">How do You rate this product?</div>
				<div class="rating-box-label">Your rating:</div>
				<div class="rating-box">
					<input id="Quality_1" name="ratings[1]" type="radio" title="Worst" value="1" class="star"/>
					<input id="Quality_2" name="ratings[1]" type="radio" title="Bad" value="2"class="star"/>
					<input id="Quality_3" name="ratings[1]" type="radio" title="OK" value="3"class="star"/>
					<input id="Quality_4" name="ratings[1]" type="radio" title="Good" value="4"class="star"/>
					<input id="Quality_5" name="ratings[1]" type="radio" title="Best" value="5"class="star"/>
				</div>

			</li><!-- End Star rating -->

			<!-- Nickname input -->
			<li>							
				<label class="rate-label required" for="nickname_field">Nickname</label>
				<input id="nickname_field" type="text" placeholder="Nickname..." name="nickname">
			</li><!-- End Nickname input -->

			<!-- Review summary input -->
			<li>
				<label class="rate-label required" for="summary_field">Summary of Your Review</label>
				<input id="summary_field" class="large" type="text" placeholder="Summary of Your Review..." name="title">
			</li><!-- End Review summary input -->

			<!-- Review content -->
			<li>
				<label class="rate-label" for="review_field">Review</label>
				<textarea class="large" id="review_field" type="text" placeholder="Summary of Your Review..." name="detail"></textarea>
			</li><!-- End Review content -->

			<!-- Submit button -->
			<li>
				<button type="submit" class="rating-submit-btn icon">Add Your Rating</button>
			</li><!-- End Submit button -->
		</ul>
	</form>

</div><!-- $[end-RATING-BLOCK] -->
```

## Cross-browser
Works on modern browsers, IE7+

## TODO
