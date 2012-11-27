# Browser Input Type Support Lie-detector with Modernizr
## Cross-check what you see with what your browser tells Modernizr
### [Check it Out](http://tessa-lt.github.com/Modernizr-Browser-Lie-Detector/)
The fantastic Modernizr library can only detect whether a browser 'supports' an html5 input type, not whether it has an implemented widget. For example, a browser could recognize `<input type="date">` as a date input, but still render it as a regular text field. This page just lets you test how accurate your modernizr tests are going to be for input types. So open it up in all your Android/WP7/8/iOS devices, take a look at whether native input widgets are supported, and check that it matches with the Modernizr output. 
### Results So Far
<table>
  <tr>
    <th>Browser</th>
    <th>Results</th>
  </tr>
  <tr>
    <td>Android Stock Browser on 2.3.3</td>
    <td>No lies</td>
  </tr>
  <tr>
    <td>Safari Mobile 6.0</td>
    <td><code>Modernizr.inputtype.week</code> returns <code>true</code>, but Safari renders plain text input</td>
  </tr>
  <tr>
    <td>Opera Mobile 12.1 on Android 2.3.3</td>
    <td>All input types return true, but <code>tel</code>, <code>url</code>, and <code>email</code> are plain text boxes. Also note that while all date and time pickers as well as `range` are technically supported, implementation is godawful. Surprisingly, <code>color</code> works ok.</td>
  </tr>
</table>