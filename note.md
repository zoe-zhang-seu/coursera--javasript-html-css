## L13 CSS element, class, ID
selector: 
-  `p{}`   for element e.g. "<p>"
- `.a{}`  for class e.g. class="a"  
- `#a{}`  for ID    e.g. ID="a" 
- `p,h1{}`for AND   e.g. "<p>" AND "<h1>"

selector combination:
- element with class: ` <p class= "A">` --> quote by ` p.A{} `  
- element with ID: `<p ID="A"> ` -->quote by `p#A{} `  
- child: `<section> <h2>`  -->quote by `section>h2{} `
- decendent `<section><Li> ` -->quote by `section Li {}`

pseudoclass selector:
- `:link`  oftern points to links such as e.g.`<a href="default.asp" target="_blank">` the useage is `a:link{color:red;}` under the `<style>`
- `:visited`
- `:hover `
- `:active `
- `:nth-child ` 
