<h1>Java 11 | Selenium | TestNG | Maven | POM Project</h1>
<p>This is a sample Java 11 AdoptOpenJDK | Selenium WebDriver | Maven | TestNG project created in IntelliJ IDE, using Page Object Model and Generic Type.</p>
<p>Website <a href="https://www.99-bottles-of-beer.net/">https://www.99-bottles-of-beer.net/</a>&nbsp;was used to create functional, API, and UI tests.</p>
<p><strong>pom.xml dependencies used:</strong></p>
<blockquote>
<pre>&lt;dependencies&gt;<br /><br />    &lt;dependency&gt;<br />        &lt;groupId&gt;org.testng&lt;/groupId&gt;<br />        &lt;artifactId&gt;testng&lt;/artifactId&gt;<br />        &lt;version&gt;7.6.1&lt;/version&gt;<br />    &lt;/dependency&gt;<br /><br />    &lt;dependency&gt;<br />        &lt;groupId&gt;org.seleniumhq.selenium&lt;/groupId&gt;<br />        &lt;artifactId&gt;selenium-java&lt;/artifactId&gt;<br />        &lt;version&gt;4.5.3&lt;/version&gt;<br />    &lt;/dependency&gt;<br /><br />    &lt;dependency&gt;<br />        &lt;groupId&gt;io.github.bonigarcia&lt;/groupId&gt;<br />        &lt;artifactId&gt;webdrivermanager&lt;/artifactId&gt;<br />        &lt;version&gt;5.3.0&lt;/version&gt;<br />    &lt;/dependency&gt;<br /><br />&lt;/dependencies&gt;</pre>
</blockquote>
<h1>API testing</h1>
<p>For testing requests and responses&nbsp;<strong>DevTools&nbsp;type property</strong> was used&nbsp;</p>
<blockquote>
<pre>&nbsp; DevTools devTools;<br /><br /></pre>
</blockquote>
<p><strong>setUpDevTool(WebDriver driver)&nbsp;</strong> method was created in the class CaptureNetworkTraffic &nbsp;to capture the traffic:</p>
<blockquote>
<pre><br />public&nbsp;CaptureNetworkTraffic setUpDevTool(WebDriver driver) {<br />&nbsp; &nbsp; &nbsp;devTools&nbsp;= ((ChromeDriver) driver).getDevTools();<br />&nbsp; &nbsp; &nbsp;devTools.createSession();<br />&nbsp; &nbsp; &nbsp;devTools.send(Network.enable(Optional.empty(), Optional.empty(), Optional.empty()));<br />&nbsp;<br />&nbsp; &nbsp; &nbsp;return this;<br />&nbsp;}&nbsp;</pre>
</blockquote>
<p><strong>org.openqa.selenium.devtools.v106.network.Network</strong>&nbsp;was used for traffic interception.</p>
<p>Class&nbsp;<strong>HttpURLConnection</strong>&nbsp;was used to send direct API calls and check responses.</p>
<h1>POM scheme</h1>
<img src="src/images/scheme-0.png">
<img src="src/images/scheme-1.png">
<img src="src/images/scheme-2.png">
<img src="src/images/scheme-3.png">
