# How to Mirror Content From One Webpage to Another Using PHP

Suppose we must duplicate content on two different pages of a website. Manually copying and pasting runs the risk of future updates going out of sync. We would prefer that one page serve as the source of the other page, so when the source is updated, the destination page updates automatically.

1. Wrap the source content in a div element and give it a memorable id:
```sh
<div id="memorable">
  Source content
</div>
```
2. Place the following PHP code in the destination file where you want the content to appear:
```sh
<?php
  $doc = new DOMDocument();
  $doc -> loadHTMLFile('/directory/source.php');
  $elt = $doc -> getElementById("memorable");
  echo $doc->saveHTML($elt);
?>
```