## Finishing the HTML for email input and footer

```html(index.html)
+	<!-- Call to Action
+	================================================== -->
+	<div id="action">
+		<h2>Give it a try before you commit.</h2>
+		<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>				
+	</div>
```



```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+		
+    <input type="text" placeholder="Enter your email address"/>
+    <button type="submit">Sign Up Now</button>
</div>
```

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
</div>
+
+	<!-- Footer
+	================================================== -->
+	<div id="footer">
+	</div>
```

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
</div>

<!-- Footer
================================================== -->
<div id="footer">
+     <nav>
+          <ul>
+               <li><a href="#">About</a></li>
+               <li><a href="#">Contact</a></li>
+               <li><a href="#">Privacy Policy</a></li>
+               <li><a href="#">Terms</a></li>
+          </ul>
+     </nav>
</div>
```

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
</div>

<!-- Footer
================================================== -->
<div id="footer">
     <nav>
          <ul>
               <li><a href="#">About</a></li>
               <li><a href="#">Contact</a></li>
               <li><a href="#">Privacy Policy</a></li>
               <li><a href="#">Terms</a></li>
          </ul>
     </nav>
+    <img src="images/small_logo.png" />
+    <p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
</div>
```
