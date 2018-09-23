# php-live-template
An extensive set of php [live templates](https://www.jetbrains.com/help/idea/2018.2/using-live-templates.html) for use with JetBrains IDEs phpStrom
## 目录

1. [描述](#description)
1. [基本语法](#syntax)
1. [文档](#documentation)
1. [安装和使用](#installation)
1. [自定义](#define)

## 描述

An extensive set of PHP [live templates](https://www.jetbrains.com/help/idea/2018.2/using-live-templates.html) for use
in JetBrains phpStrom.
<br>phpStrom中一个可扩展的php快捷短语模板

## 基本语法
1. [$VAR$ 可以定义一个变量](#syntax)
1. [$ARRAY$ 可输入一个数组](#syntax)
1. [$PARAM$ 可变长度参数](#syntax)
1. [$END$ 光标结束符号](#syntax)

## 文档
<table>
  <thead>
        <tr>
            <th>Live Template Short Hand</th>
            <th>Description</th>
            <th>Template </th>
        </tr>
    </thead>
  <tbody>
<tr>
<td> ? </td>
<td>
php 基础语句
</td>
<td><pre>
&lt?php $END$ ?&gt               
</pre></td>
</tr>

<tr>
<td> ?3 </td>
<td>
三目运算
</td>
<td><pre>
$VAR$ = ($CONDITION$) ? $VAL1$ : $VAL2$;              
</pre></td>
</tr>

<tr>
<td> ?? </td>
<td>
echo 语句
</td>
<td><pre>
&lt ?php echo $END$; ? &gt               
</pre></td>
</tr>

<tr>
<td> ?co </td>
<td>
const 语句
</td>
<td><pre>
const $NAME$;             
</pre></td>
</tr>

<tr>
<td> ?coe </td>
<td>
const 语句
</td>
<td><pre>
const $NAME$ = '$value$';           
</pre></td>
</tr>

<tr>
<td> ?fn </td>
<td>
function 语句
</td>
<td><pre>
function $NAME$($PARAMETERS$){
    $END$
}          
</pre></td>
</tr>

<tr>
<td> ?for </td>
<td>
for 语句
</td>
<td><pre>
for ($INDEX$ = 0; $INDEX$ < count($ARRAY$); $INDEX$++) {
    $END$    
}         
</pre></td>
</tr>

<tr>
<td> ?fore </td>
<td>
foreach 语句
</td>
<td><pre>
&lt?php foreach ($ITERABLE$ as $VAR_VALUE$): ?&gt
    $END$
&lt?php endforeach ?&gt  
</pre></td>
</tr>

<tr>
<td> ?fork </td>
<td>
foreach 语句
</td>
<td><pre>
&lt?php foreach ($ITERABLE$ as $VAR_KEY$ => $VAR_VALUE$): ?&gt
    $END$
&lt?php endforeach ?&gt   
</pre></td>
</tr>

<tr>
<td> ?he </td>
<td>
header 语句 文档类型
</td>
<td><pre>
header('Content-type: text/html; charset=utf-8');       
</pre></td>
</tr>

<tr>
<td> ?if </td>
<td>
if 语句
</td>
<td><pre>
&lt?php if ($CONDITION$): ?&gt
    $END$
&lt?php endif ?&gt   
</pre></td>
</tr>

<tr>
<td> ?msg </td>
<td>
$GLOBALS 语句 定义一个全局变量 $msg
</td>
<td><pre>
$GLOBALS['msg'] = '$TXT$';     
</pre></td>
</tr>

<tr>
<td> ?re </td>
<td>
require 语句
</td>
<td><pre>
require('$PATH$');     
</pre></td>
</tr>

<tr>
<td> ?vd </td>
<td>
var_dump 语句
</td>
<td><pre>
var_dump($content$);    
</pre></td>
</tr>

<tr>
<td> ?wh </td>
<td>
while 语句
</td>
<td><pre>
&lt?php while ($CONDITION$): ?&gt
  $END$
&lt?php endwhile ?&gt
</pre></td>
</tr>

<tr>
<td> if </td>
<td>
if 语句
</td>
<td><pre>
if ($CONDITION$) { }  
</pre></td>
</tr>

<tr>
<td> ifex </td>
<td>
exit 语句
</td>
<td><pre>
if(!$condition$) {
    exit('&lth2&gt$END$&lt/h2&gt');
}
</pre></td>
</tr>

<tr>
<td> r </td>
<td>
return 语句
</td>
<td><pre>
return;
</pre></td>
</tr>

<tr>
<td> r0 </td>
<td>
return 语句
</td>
<td><pre>
return 0;
</pre></td>
</tr>

<tr>
<td> r1 </td>
<td>
return 语句
</td>
<td><pre>
return 1;
</pre></td>
</tr>

<tr>
<td> r2 </td>
<td>
return 语句
</td>
<td><pre>
return -1;
</pre></td>
</tr>

<tr>
<td> rf </td>
<td>
return 语句
</td>
<td><pre>
return false;
</pre></td>
</tr>

<tr>
<td> rt </td>
<td>
return 语句
</td>
<td><pre>
return true;
</pre></td>
</tr>

<tr>
<td> ro </td>
<td>
return 语句
</td>
<td><pre>
return $object$;
</pre></td>
</tr>

  </tbody>
</table>

## 安装和使用
>安装
<br>把my PHP.xml文件拷贝到下面的目录中：
<br>windows: C:\Users\Administrator\.PhpStorm\config\templates
<br>macOS: ~/Library/Preferences/<intellij-product-install>/templates

>使用
<br>我的PHP自定义快捷模板，我设置的默认触发是 Enter（系统默认是Tab），这个可以自己修改。
<br>使用方法：
<br>在phpStrom开发环境中（HTML/PHP文档中）输入一个 <code>?</code> ,再按 <code>Enter</code> 键，就可以输出：
<pre>&lt?php //光标位置 ?&gt</pre>

## 自定义 Live Template
>配置步骤
1. [进入设置界面](#define)
1. [搜索 <code>Live Templates</code>进入模板的编辑界面](#define)
1. [点开 <code>my PHP</code> ，点击右侧的 <code>+</code> 号，选择<code>live template</code>，也可选择 <code>template group</code> 来建立一个新的组比如 <code>my PHP2</code>](#define)
1. [填入相应的数据：](#define)
1. [<code>abbreviation</code> 定义快捷短语](#define)
1. [<code>description</code>  描述该快捷模块的功能](#define)
1. [<code>Template text</code> 模板代码](#define)
1. [点击<code>define</code>选择该模板的生效范围](#define)
1. [在<code>Expand with</code>选择快捷短语触发键](#define)
1. [点击<code>ok</code>保存](#define)
