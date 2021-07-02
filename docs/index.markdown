---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: splash
header:
 overlay_image: /assets/feetinthesnow.jpg
---






Hi, welcome to my personal web page. This is the home page. Make yourself comfortable.
  
I have a collection of blog posts on various data applications, or if you want to know more about my background head to the About tab.

<html>
<body>


<script>
function callbackName(response) {
    document.getElementById('visits').textContent = parseFloat(response.value);
}
</script>
<script async src="https://api.countapi.xyz/hit/bibblybobbly/home/?callback=callbackName"></script>



You're visitor number:   <div id='visits' innerText=20> </div>



</body>
</html>