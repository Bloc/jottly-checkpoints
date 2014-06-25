```CSS(stylesheets/base.css)
...
 	input[type="submit"],
  	input[type="reset"],
  	input[type="button"] {
 -		background: #eee; /* Old browsers */
 -		background: #eee -moz-linear-gradient(top, rgba(255,255,255,.2) 0%, rgba(0,0,0,.2) 100%); /* FF3.6+ */
 -		background: #eee -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.2)), color-stop(100%,rgba(0,0,0,.2))); /* Chrome,Safari4+ */
 -		background: #eee -webkit-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Chrome10+,Safari5.1+ */
 -		background: #eee -o-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Opera11.10+ */
 -		background: #eee -ms-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* IE10+ */
 -		background: #eee linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* W3C */
 -	  border: 1px solid #aaa;
 -	  border-top: 1px solid #ccc;
 -	  border-left: 1px solid #ccc;
 -	  -moz-border-radius: 3px;
 -	  -webkit-border-radius: 3px;
 -	  border-radius: 3px;
 -	  color: #444;
 -	  display: inline-block;
 -	  font-size: 11px;
 -	  font-weight: bold;
 -	  text-decoration: none;
 -	  text-shadow: 0 1px rgba(255, 255, 255, .75);
 -	  cursor: pointer;
 -	  margin-bottom: 20px;
 -	  line-height: normal;
 -	  padding: 8px 10px;
 -	  font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif; }
 +		-moz-border-radius: 8px;
 +		-webkit-border-radius: 8px;
 +		border-radius: 8px; /* border radius */
 +		-moz-background-clip: padding;
 +		-webkit-background-clip: padding-box;
 +		background-clip: padding-box; /* prevents bg color from leaking outside the border */
 +		background-color: #009ae8; /* layer fill content */
 +		color: #fff;
 +		font-size: 1.2em;
 +		border:0;
 +		text-transform: uppercase;
 +		font-weight: 900;
 +		padding:0.82em 2.5em;
 +		cursor: pointer;
 +		margin:0; }
  
  	.button:hover,
  	button:hover,
  	input[type="submit"]:hover,
  	input[type="reset"]:hover,
  	input[type="button"]:hover {
 -		color: #222;
 -		background: #ddd; /* Old browsers */
 -		background: #ddd -moz-linear-gradient(top, rgba(255,255,255,.3) 0%, rgba(0,0,0,.3) 100%); /* FF3.6+ */
 -		background: #ddd -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.3)), color-stop(100%,rgba(0,0,0,.3))); /* Chrome,Safari4+ */
 -		background: #ddd -webkit-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Chrome10+,Safari5.1+ */
 -		background: #ddd -o-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Opera11.10+ */
 -		background: #ddd -ms-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* IE10+ */
 -		background: #ddd linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* W3C */
 -	  border: 1px solid #888;
 -	  border-top: 1px solid #aaa;
 -	  border-left: 1px solid #aaa; }
 +		background:#0483c3; }
  
  	.button:active,
  	button:active,
  	input[type="submit"]:active,
  	input[type="reset"]:active,
  	input[type="button"]:active {
 -		border: 1px solid #666;
 -		background: #ccc; /* Old browsers */
 -		background: #ccc -moz-linear-gradient(top, rgba(255,255,255,.35) 0%, rgba(10,10,10,.4) 100%); /* FF3.6+ */
 -		background: #ccc -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.35)), color-stop(100%,rgba(10,10,10,.4))); /* Chrome,Safari4+ */
 -		background: #ccc -webkit-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Chrome10+,Safari5.1+ */
 -		background: #ccc -o-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Opera11.10+ */
 -		background: #ccc -ms-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* IE10+ */
 -		background: #ccc linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* W3C */ }
 +		}
  
  	.button.full-width,
  	button.full-width,
 @@ -219,15 +193,15 @@
  	textarea,
  	select {
  		border: 1px solid #ccc;
 -		padding: 6px 4px;
 +		padding: 0.75em 1em;
  		outline: none;
 -		-moz-border-radius: 2px;
 -		-webkit-border-radius: 2px;
 -		border-radius: 2px;
 -		font: 13px "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
 +		-moz-border-radius: 8px;
 +		-webkit-border-radius: 8px;
 +		border-radius: 8px;
 +		font: 1.2em "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  		color: #777;
  		margin: 0;
 -		width: 210px;
 +		width: 90%;
  		max-width: 100%;
  		display: block;
  		margin-bottom: 20px;
 @@ -322,4 +296,18 @@
  }
  #header p strong {
  	color:#fff;
 +}
 +
 +/* Benefits */
 +#benefits {
 +	padding:4em 0 0;
 +	text-align: center;
 +}
 +#benefits h2, #testimonials h2 {
 +	color:#009be8;
 +	font-weight: 300;
 +}
 +#benefits p, #testimonials p {
 +	color:#9d9d9d;
 +	font-size:1.2em;
  }
  ```