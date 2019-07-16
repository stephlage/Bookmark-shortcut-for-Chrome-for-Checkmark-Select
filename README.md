# Bookmark-shortcut-for-Chrome-for-Checkmark-Select

## SETUP
1. Open Chrome.
2. Right click in bookmarks toolbar.
3. Click Add Page
4. Give it a name like "Quick Checkmark Selector" 
5. Copy and paste the following into the URL spot:
```javascript  
  javascript:(function(e,a,g,h,f,c,b,d){if(!(f=e.jQuery)||g>f.fn.jquery||h(f)){c=a.createElement("script");c.type="text/javascript";c.src="http://ajax.googleapis.com/ajax/libs/jquery/"+g+"/jquery.min.js";c.onload=c.onreadystatechange=function(){if(!b&&(!(d=this.readyState)||d=="loaded"||d=="complete")){h((f=e.jQuery).noConflict(1),b=1);f(c).remove()}};a.documentElement.childNodes[0].appendChild(c)}})(window,document,"1.3.2",function($,L){$('<textarea id="folders2select" title="Quick Checkmark Selector" autofocus="true" placeholder="Names of folders to select, one per line" rows="10" cols="30" style="border: 1px solid;"/>').dialog({width:"auto",buttons:[{text:"Ok",click:function(){var b=$("#folders2select").val();var c=b.match(/[^\r\n]+/g);var a=[];$.each(c,function(e,d){if($("a:contains("+d+")").length==0){a.push(d)}$("a:contains("+d+")").parent().siblings("input").prop("checked",true)});$(this).dialog("close").dialog("destroy").remove();if(a.length!==0){$('<div title="PEBKAC">Could not find: '+a.toString()+"</div>").dialog()}1}}]});});
``` 

6. Save.

## RUN
To run, you will need to be in your CMS
1. Copy your line-break seperated list to paste into the box with the names of the stuff you want checkmarked.
2. While the CMS page is open, click the bookmark you named above "Quick Checkmark Selector".
3. Paste your list.
4. Click OK.
5. Your list should now be selected.
