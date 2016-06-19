# Quantifiers

<table>
<tr>
<td>Quantifier</td>
<td>Meaning</td>
</tr>
<tr>
<td><code>*</code></td>
<td>O or more</td>
</tr>
<tr>
<td><code>+</code></td>
<td>1 or more</td>
</tr>
<tr>
<td><code>?</code></td>
<td>O or 1</td>
</tr>
<tr>
<td><code>{3}</code></td>
<td>Exactly 3</td>
</tr>
<tr>
<tr>
<td><code>{3,}</code></td>
<td>3 or more</td>
</tr>
<tr>
<td><code>{3,5}</code></td>
<td>3, 4 or 5</td>
</tr>
<tr>
</table>

## * : 0 or more

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c*</td>
<td>
<code>ab</code><br/>
<code>abc</code><br/>
<code>abcc</code><br/>
</td>
</tr>
</tbody>
</table>

## + : 1 or more

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c+</td>
<td>
ab<br/>
<code>abc</code><br/>
<code>abcc</code><br/>
</td>
</tr>
</tbody>
</table>

## ? : 0 or 1

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c?</td>
<td>
<code>ab</code><br/>
<code>abc</code><br/>
abcc<br/>
</td>
</tr>
</tbody>
</table>

## {3}: Exactly 3

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c{3}</td>
<td>
ab<br/>
abc<br/>
abcc<br/>
abcc<br/>
<code>abccc</code><br/>
abcccc
</td>
</tr>
</tbody>
</table>

## {3, }: Exactly 3 or more

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c{3,}</td>
<td>
abcc<br/>
abcc<br/>
<code>abccc</code><br/>
<code>abcccc</code><br/>
<code>abcccccc</code><br/>
</td>
</tr>
</tbody>
</table>

## {3, 5}: 3, 4 or 5 

<table>
<thead>
<tr>
<td>Regular Expression</td>
<td>Test Strings</td>
</tr>
</thead>
<tbody>
<tr>
<td>(ab)c{3, 5}</td>
<td>
abc<br/>
abcc<br/>
<code>abccc</code><br/>
<code>abcccc</code><br/>
<code>abccccc</code><br/>
abcccccc<br/>
</td>
</tr>
</tbody>
</table>

## Greedy and Lazy

<table>
<thead>
<tr>
<td>String</td>
<td>Greedy</td>
<td>Lazy</td>
</tr>
</thead>
<tbody>
<tr>
<td>aabaaba</td>
<td>
Regex: <b>^.b</b><br/>
Match: <code>aabaab</code>a
</td>
<td>
Regex: <b>^.*b?</b><br/>
Match: <code>aab</code>aaba
</td>
</tr>
</tbody>
</table>

# References

* [Regular Expressions cheat sheet](http://web.mit.edu/hackl/www/lab/turkshop/slides/regex-cheatsheet.pdf)
