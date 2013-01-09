#Generic product reviews & rating
  
## Version
current version: 0.1.0  
   
   

## Documentation
### Table of contents  
1. **[Example](https://github.com/karolgorecki/generic-product-rev#example)**
1. **[Requirements](https://github.com/karolgorecki/generic-product-rev#requirements)**
1. **[HTML Structure](https://github.com/karolgorecki/generic-product-rev#html-structure)**
1. **[Cross-browser](https://github.com/karolgorecki/generic-product-rev#cross-browser)**
1. **[TODO](https://github.com/karolgorecki/generic-product-rev#todo)**

## Example
### [http://karolgorecki.github.com/generic-product-rev/](http://karolgorecki.github.com/generic-product-rev/)


## Requirements
### Files
[reviews.less](https://github.com/karolgorecki/generic-product-rev/blob/master/less/reviews.less)  
[reviews-custom.less](https://github.com/karolgorecki/generic-product-rev/blob/master/less/reviews-custom.less) - to make custom style

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
* write documentation
* test in all browser's
* add more vars
* add more configuration options
