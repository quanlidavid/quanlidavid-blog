Title: 解析xml的CDATA里的html tag
Date: 2017-12-11 10:20
Modified: 2017-12-11 19:30
Category: Tech
Tags: beautifulsoup, xml
Slug: tech3
Authors: Quan
Summary: Parse html tag in xml CDATA

参考：
[XML CDATA是什么？](https://www.cnblogs.com/qiantuwuliang/archive/2010/03/29/1699361.html)

需要解析如下xml的CDATA里的HTML tag：
```
<component vis="true" id="m785e53fe-sccombobox_textbox_holder" compid="m785e53fe-sccombobox_textbox"><![CDATA[

<input datatype="0" id="m785e53fe-sccombobox_textbox"  aria-required="true"  role="combobox" aria-autocomplete="none"  class="fld pmscoffcat_text_node cbt  ibfld fld_req"     ctype="textbox"   li="m785e53fe-sccombobox_dropimage" liclick="1"    maxlength="254" style=";width:247.5px;"      sue="1"  readonly="readonly" type="text"   value="small.1" ov="small.1" work="1" fldInfo='{&quot;length&quot;:&quot;254&quot;,&quot;eventpriority&quot;:1,&quot;required&quot;:true,&quot;inttype&quot;:&quot;0&quot;}'/>]]></component>
	<compvalue id="m785e53fe-sccombobox_textbox"><![CDATA[small.1]]></compvalue>
```

需要拿到input的value值。

```
r = s.post('https://10.180.19.18/maximo/ui/maximo.jsp', data=payload)
soup = BeautifulSoup(r.text, "lxml-xml")
tshirtsize = BeautifulSoup(soup.text, 'html5lib').find('input', attrs={'id': 'm785e53fe-sccombobox_textbox'})['value']
```

通过以上方式可以拿到。