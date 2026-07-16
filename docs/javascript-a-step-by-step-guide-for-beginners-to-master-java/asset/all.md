Javascript

A step-by-step guide for beginners to master javascript programming

Lena neill

©  copyright  2023  –  ryan  roffe,

All  rights  re,se,rve,d.

The,  conte,nt  containe,d  within  this  book  may  not  be,  re,produce,d,  duplicate,d,  or  transmitte,d  without  dire,ct  writte,n  pe,rmission  from  the,  author  or  the,  publishe,r.

Unde,r  no  circumstance,s  will  any  blame,  or  le,gal  re,sponsibility  be,  he,ld  against  the,  publishe,r,  or  author,  for  any  damage,s,  re,paration,  or  mone,tary  loss  due,  to  the,  information  containe,d  within  this  book,  e,ithe,r  dire,ctly  or  indire,ctly.

Le,gal  notice,:

This  book  is  copyright  prote,cte,d.  it  is  only  for  pe,rsonal  use,.  you  cannot  ame,nd,  distribute,,  se,ll,  use,,  quote,  or  paraphrase,  any  part,  or  the,  conte,nt  within  this  book,  without  the,  conse,nt  of  the,  author  or  publishe,r.

Disclaime,r  notice,:

Ple,ase,  note,  the,  information  containe,d  within  this  docume,nt  is  for  e,ducational  and  e,nte,rtainme,nt  purpose,s  only.  all  e,ffort  has  be,e,n  e,xe,cute,d  to  pre,se,nt  accurate,,  up  to  date,,  re,liable,,  comple,te,  information.  no  warrantie,s  of  any  kind  are,  de,clare,d  or  implie,d.  re,ade,rs  acknowle,dge,  that  the,  author  do  not  e,ngage,  in  the,  re,nde,ring  of  le,gal,  financial,  me,dical,  or  profe,ssional  advice,.  the,  conte,nt  within  this  book  has  be,e,n  de,rive,d  from  various  source,s.  ple,ase,  consult  a  lice,nse,d  profe,ssional  be,fore,  atte,mpting  any  te,chnique,s  outline,d  in  this  book.

By  re,ading  this  docume,nt,  the,  re,ade,r  agre,e,s  that  unde,r  no  circumstance,s  is  the,  author  re,sponsible,  for  any  losse,s,  dire,ct  or  indire,ct,  that  are,  incurre,d  as  a  re,sult  of  the,  use,  of  the,  information  containe,d  within  this  docume,nt,  including,  but  not  limite,d  to,  e,rrors,  omissions,  or  inaccuracie,s.

Table, of conte,nts

[Introduction](#index_split_003.html_id_Toc157349706)

[Chapter 1: what is javascript](#index_split_004.html_id_Toc157349707)

[Chapter 2: values, types, and operators](#index_split_005.html_id_Toc157349708)

[Chapter 3: program structure](#index_split_006.html_id_Toc157349709)

[Chapter 4: functions](#index_split_007.html_id_Toc157349710)

[Chapter 5: data structures: objects and arrays](#index_split_008.html_id_Toc157349711)

[Chapter 6: higher-order functions](#index_split_009.html_id_Toc157349712)

[Chapter 7: the secret life of objects](#index_split_010.html_id_Toc157349713)

[Chapter 8: a robot](#index_split_011.html_id_Toc157349714)

[Chapter 9: bugs and errors](#index_split_013.html_id_Toc157349715)

[Chapter 10: regular expressions](#index_split_014.html_id_Toc157349716)

[Chapter 11: modules](#index_split_016.html_id_Toc157349717)

[Chapter 12: asynchronous programming](#index_split_017.html_id_Toc157349718)

[Conclusion](#index_split_019.html_id_Toc157349719)

## Introduction

Javascript  is  a  distinguishe,d  and  de,ciphe,re,d  programming  language,  that  adhe,re,s  to  the,  e,cmascript  spe,cification.  the,  programming  language,  consists  of  high-powe,re,d  typing,  the,  curly  bracke,t  syntax,  top-quality  functions,  and  prototype,-base,d  obje,ct-orie,ntation.  accompanie,d  by  html  and  css,  javascript  is  one,  of  the,  significant  te,chnologie,s  of  the,  world  wide,  we,b.  javascript  facilitate,s  inte,rchange,able,  we,b  page,s  and  is  a  vital  part  of  we,b  applications.  almost  e,ve,ry  we,bsite,  utilize,s  javascript,  and  all  the,  significant  we,b  browse,rs  consist  of  the,  javascript  e,ngine,  to  function  corre,ctly.  bre,ndan  e,ich  de,ve,lope,d  javascript  in  1995  whe,n  he,  was  with  ne,tscape,  communications.  javascript  aids  functional,  e,ve,nt-drive,n,  prototype,-base,d  and  obje,ct-orie,nte,d  programming  style,s.  javascript  upgrade,s  we,b  use,r  inte,rface,  by  affirming  activitie,s  take,n  on  the,  clie,nt-side,  by  the,  use,r.  you  can  inse,rt  javascript  e,ngine,s  into  diffe,re,nt  type,s  of  host  software,,  which  include,s  database,s  and  we,b  se,rve,rs,  and  non-we,b  re,late,d  programs  like,  word  proce,ssors.

The,  conce,pts  of  javascript  are,  e,xplaine,d  furthe,r  in  this  book  with  the,  goal  to  he,lp  you  le,arn  and  unde,rstand  javascript  language,  without  pre,ssure,.  the,  knowle,dge,  of  html,  te,xt  e,ditor,  we,b  browse,r,  and  css  are,  all  that's  ne,e,de,d  to  le,arn  javascript.  to  ge,t  the,  le,arning  proce,ss  starte,d,  one,  of  the,  e,sse,ntial  tools  is  a  te,xt  e,ditor,  and  it  is  re,quire,d  to  write,  code,s.  you’ll  also  ne,e,d  a  browse,r  to  unve,il  your  de,ve,lope,d  we,b  page,s.  the,re,  are,  diffe,re,nt  type,s  of  te,xt  e,ditors  such  as  the,  sublime,  te,xt,  note,pad++  and  browse,rs  such  as  fire,fox,  google,  chrome,,  and  so  on.

## Chapte,r  1:  what  is  javascript

Javascript,  abbre,viate,d  js,  is  a  high-le,ve,l  programming  language,  introduce,d  to  add  spe,cific  programs  to  we,b  page,s,  and  it  has  be,e,n  adopte,d  by  all  major  we,b  browse,rs.  javascript  can  be,  use,d  to  build  inte,ractive,  we,b  applications  to  function  appropriate,ly  without  re,loading  e,ve,ry  page,  pe,r-action.  javascript  is  use,d  to  cre,ate,  diffe,re,nt  forms  of  activitie,s  within  we,b  page,s  and  is  one,  of  the,  e,sse,ntial  compone,nts  of  the,  world  wide,  we,b  (www),  which  are,  html  (hype,rte,xt  markup  language,)  and  css  (cascading  style,  she,e,ts).  javascript  and  html  are,  use,d  to  de,ve,lop  we,b  page,s.  javascript  brings  a  page,  to  life,  by  adding  spe,cial  e,ffe,cts  such  as  slide,rs,  pop-ups,  form  validations,  e,tc.  css  de,te,rmine,s  the,  color  inte,nsity,  image,  size,,  background  colors,  type,face,,  font  size,,  e,tc.

Clie,nt-side,  javascript

Clie,nt-side,  javascript  is  the,  usual  form  of  javascript  language,.  the,  script  must  be,  inse,rte,d  or  re,fe,re,nce,d  by  an  html  docume,nt  so  that  the,  browse,r  can  inte,rpre,t  the,  code,.  it  e,nable,s  we,b  page,s  to  include,  inte,ractive,  programs  with  the,  use,r,  de,ve,lop  html  conte,nt  dynamically,  and  command  the,  browse,r.  use,rs  use,  javascript  code,  whe,n  the,y  want  to  submit  forms  and  also  de,te,rmine,  if  all  e,ntrie,s  are,  valid  be,fore,  it  transfe,rs  the,m  to  the,  se,rve,r.

Advantage,s  of  javascript

·  with  javascript,  use,rs  can  organize,  input  be,fore,  ge,tting  the,  page,  se,nt  to  the,  se,rve,r,  which  automatically  re,duce,s  loads  on  the,  se,rve,r.

·  javascript  e,nable,s  swift  re,sponse,  to  page,  visitors.  the,  page,  doe,s  not  have,  to  re,load  be,fore,  visitors  can  se,e,  if  the,re,  was  an  e,rror  in  typing.

·  javascript  is  use,d  to  build  a  re,active,  inte,rface,  that  give,s  a  re,action  whe,n  the,  mouse,  hove,rs  ove,r  the,m.

Limitations  of  javascript

Javascript  programming  language,  lacks  the,  following  e,sse,ntial  fe,ature,s.  the,y  are,:

·  for  se,curity  re,asons,  clie,nt-side,  javascript  doe,s  not  re,ad  or  write,  file,s

·  javascript  for  ne,tworking  applications

·  javascript  doe,s  not  contain  multiproce,ssor  capabilitie,s

Javascript  de,ve,lopme,nt  tools

You  do  not  ne,e,d  an  e,xpe,nsive,  de,ve,lopme,nt  tool  to  write,  javascript  code,s.  you  can  write,  with  a  simple,  te,xt  e,ditor  such  as  microsoft  frontpage,,  macrome,dia  dre,amwe,ave,r  mx,  macrome,dia  home,site,  5,  e,tc.

Javascript  place,me,nt

Javascript  code,  is  inse,rte,d  anywhe,re,  in  an  html  docume,nt.  howe,ve,r,  you  want  to  inse,rt  javascript  code,  in  an  html  file,  like,  this:

The,  script  within  <he,ad>  </he,ad>  part.

The,  script  within  <body>  </body>  part.

The,  script  within  <body>  </body>  and  <he,ad>  </he,ad>  part.

Include,  e,xte,rnal  file,  script  in  the,  <he,ad>...</he,ad>  part.

Javascript  in  <he,ad>...</he,ad>  se,ction

In  some,  case,s,  whe,n  you  want  the,  script  to  run  on  a  spe,cial  e,ve,nt,  such  as  an  action  whe,n  a  button  clicke,d,  place,  the,  script  in  the,  he,ad  se,ction  like,  this:

<html>

<he,ad>

<script  type,="te,xt/javascript">

<!--

Function  sayhi()  {

Ale,rt("he,llo  world")

}

//-->

</script>

</he,ad>

<body>

Tap  he,re,  for  re,sult

<input  type,="button"  onclick="sayhi()"  value,="say  hi"  />

</body>

</html>

Javascript  in  <body>...</body>  se,ction

Some,time,s  you  want  a  script  to  run  imme,diate,ly  and  to  cre,ate,  script  on  the,  conte,nt  page,,  inse,rt  the,  script  within  the,  <body>  se,ction.  this  is  what  the,  code,  should  look  like,:

<html>

<he,ad>

</he,ad>

<body>

<script  type,="te,xt/javascript">

<!--

Docume,nt.write,("he,llo  world")

//-->

</script>

<p>this  is  we,b  page,  body  </p>

</body>

</html>

Javascript  in  <body>  and  <he,ad>  se,ctions

Inse,rt  your  javascript  code,  in  <he,ad>  and  <body>  se,ction  like,  this:

<html>

<he,ad>

<script  type,="te,xt/javascript">

<!--

Function  sayhi()  {

Ale,rt("he,llo  world")

}

//-->

</script>

</he,ad>

<body>

<script  type,="te,xt/javascript">

<!--

Docume,nt.write,("he,llo  world")

//-->

</script>

<input  type,="button"  onclick="sayhi()"  value,="say  hi"  />

</body>

</html>

Javascript  in  e,xte,rnal  file,s

To  avoid  the,  use,  of  ide,ntical  javascript  code,  re,pe,tition,  the,  language,  e,nable,s  you  to  cre,ate,  an  e,xte,rnal  file,  and  store,  javascript  code,s  and  the,n  inte,grate,  the,  e,xte,rnal  file,  into  the,  html  file,s.  the,  sample,  be,low  displays  how  to  inte,grate,  an  e,xte,rnal  javascript  file,  within  the,  html  code,  utilizing  the,  script  tag  and  src  attribute,.

<html>

<he,ad>

<script  type,="te,xt/javascript"  src="file,name,.js"  ></script>

</he,ad>

<body>

.......

</body>

</html>

The,  e,xte,rnal  file,  source,  file,  should  be,  save,d  with  an  e,xte,nsion  .js.

Summary

In  this  first  chapte,r,  we,  e,xplaine,d  the,  origination  of  javascript  and  its  place,me,nt  into  inte,rnal  and  e,xte,rnal  file,s.  we,  discusse,d  the,  use,  of  javascript  to  build  inte,ractive,  we,b  applications  to  pe,rform  appropriate,ly  without  having  to  re,load  e,ve,ry  page,  pe,r-action.

E,xe,rcise,

How  do  you  inse,rt  javascript  code,  into  the,  he,ad,  body  and  include,  e,xte,rnal  file,  script  in  an  html  docume,nt?

Solution

The,  script  for  the,  he,ad  part  is  <he,ad>  </he,ad>.

The,  script  for  the,  body  part  is  <body>  </body>.

The,  script  within  the,  body  is  <body>  </body>  and  <he,ad>  </he,ad>.

The,  script  to  include,  e,xte,rnal  file,  script  in  the,  <he,ad>...</he,ad>.

## Chapte,r  2:  value,s,  type,s,  and  ope,rators

In  the,  world  of  compute,rs,  the,re,  is  data.  you  can  cre,ate,  ne,w  data,  re,ad  data  and  change,  data,  which  are,  all  store,d  as  a  look-alike,  long  succe,ssion  of  bits.  de,fine,  bits  as  ze,ros  and  one,s  that  take,  a  strong  or  we,ak  signal,  and  high  or  low  e,le,ctrical  charge,  from  inside,  the,  compute,r.  all  data  and  pie,ce,s  of  information  are,  de,scribe,d  as  a  succe,ssion  of  ze,ros  and  one,s  and  re,pre,se,nte,d  in  bits.

Value,s

Take,  a  de,e,p  bre,ath  and  think  of  an  oce,an  of  bits.  the,  late,st  pcs  contains  more,  than  30  billion  bits  in  its  data  storage,.  we,  use,  bits  to  cre,ate,  value,s.  the,  compute,r  can  function  corre,ctly  be,cause,  e,ve,ry  bit  of  information  is  split  into  value,s.  e,ve,ry  value,  consists  of  a  type,  that  influe,nce,s  its  role,,  and  value,s  can  be,  numbe,rs,  te,xt  or  functions,  e,tc.  to  ge,ne,rate,  value,,  you  ne,e,d  to  invoke,  its  name,,  and  it  appe,ars  from  whe,re,  it  was  store,d.

Arithme,tic

Arithme,tic  is  the,  major  thing  to  do  with  numbe,rs.  the,  multiplication,  addition,  and  subtraction  of  more,  than  one,  numbe,r  to  produce,  anothe,r  numbe,r  is  an  arithme,tic  ope,ration.  this  is  an  e,xample,  of  what  the,y  look  like,  in  javascript:

100  +  4  *  11

The,  +  and  *  symbols  are,  calle,d  ope,rators,  the,  first  me,ans  addition  while,  the,  othe,r  me,ans  multiplication.  an  ope,rator  inse,rte,d  be,twe,e,n  two  value,s  will  produce,  anothe,r  value,.  the,  -  ope,rator  is  for  subtraction  and  the,  /  ope,rator  is  for  the,  division.  if  ope,rators  show  toge,the,r  without  pare,nthe,se,s,  the,  pre,ce,de,nce,  of  the,  ope,rators  de,cide,s  the,  way  the,y  are,  applie,d.  if  se,ve,ral  ope,rators  with  the,  same,  pre,ce,de,nce,  show  right  ne,xt  to  e,ach  othe,r  like,  1  -  2  +  1,  apply  the,m  le,ft  to  right:  (1  -  2)  +  1.

Spe,cial  numbe,rs

Javascript  consists  of  thre,e,  unique,  value,s  that  do  not  act  like,  numbe,rs  but  are,  re,garde,d  as  numbe,rs.  infinity  and  -infinity  are,  the,  first  two,  which  me,an  the,  positive,  and  ne,gative,  infinitie,s,  and  the,  last  value,  is  the,  nan.  nan  says  “not  a  numbe,r,”  although  it  is  a  value,  of  the,  numbe,r  type,.

Strings

A  string  is  the,  succe,ssion  of  numbe,rs.  the,  string  is  the,  ne,xt  data  type,,  and  the,y  re,pre,se,nt  te,xt.  strings  confine,  the,ir  conte,nt  in  quote,s.

`down  the,  walkway  path.  `

"on  top  of  the,  roof."

'I  am  at  home,.'

Quote,s  are,  use,d  in  diffe,re,nt  type,s  like,  the,  double,  quote,s,  single,  quote,s,  or  the,  backticks  to  mark  strings.  it  is  e,sse,ntial  that  the,  strings  match.  the,  e,le,me,nts  within  the,  quote,s  cre,ate,  a  string  value,  by  javascript.  javascript  use,s  the,  unicode,  standard  to  assign  a  numbe,r  to  e,ve,ry  characte,r  ne,e,de,d,  including  arabic,  arme,nian,  japane,se,,  e,tc.  you  cannot  subtract,  multiply,  or  divide,  strings  but  you  can  use,  the,  +  ope,rator,  which  will  not  add  but  concate,nate,s  two  strings  toge,the,r.  concate,nation  me,ans  to  glue,  strings  toge,the,r.

Unary  ope,rators

Symbols  do  not  re,pre,se,nt  all  the,  ope,rators.  you  can  write,  some,  ope,rators  in  words.  a  cle,ar  e,xample,  is  a  type,  of  ope,rator,  and  this  ope,rator  cre,ate,s  a  string  value,  with  the,  name,  of  the,  type,of  its  attache,d  value,.

Console,.log(type,of  4.5)

//  →  numbe,r

Console,.log(type,of  "x")

//  →  string

The,  se,cond  displaye,d  ope,rator  is  calle,d  the,  binary  ope,rator  be,cause,  the,y  use,  two  value,s,  while,  ope,rators  that  use,  one,  value,  are,  the,  unary  ope,rator.

Console,.log(-  (10  -  2))

//  →  -8

Boole,an  value,s

Boole,an  is  a  value,  that  diffe,rs  only  be,twe,e,n  two  possibilitie,s  such  as  “on”  and  “off”  and  so  on.  the,  boole,an  consists  of  only  true,  and  false,.

Comparison

Comparison  is  a  way  to  cre,ate,  boole,an  value,s:

Console,.log(3  >  2)

//  →  true,

Console,.log(3  <  2)

//  →  false,

The,  >  and  <  characte,rs  are,  the,  signs  that  re,pre,se,nt  “is  gre,ate,r  than”  and  “is  le,ss  than,”  accordingly.  you  can  use,  binary  ope,rators  in  a  boole,an  value,  that  de,te,rmine,s  if  the,  containe,d  value,  if  true,  or  false,.

You  can  compare,  strings  in  the,  same,  manne,r.

Console,.log("aardvark"  <  "zoroaste,r")

//  →  true,

You  can  instruct  strings  in  alphabe,tical  orde,r,  uppe,rcase,  le,tte,rs  are,  ofte,n  “le,ss”  than  lowe,rcase,,  so  "z"  <  "a,"  and  non-alphabe,tic  characte,rs  (!  -,  and  so  on)  are,  also  pre,se,nt  in  the,  orde,ring.  whe,n  javascript  want  to  compare,  strings,  it  re,cognize,s  characte,rs  from  le,ft  to  right,  diffe,re,ntiating  the,  unicode,  code,s  individually.

He,re,  are,  othe,r  re,late,d  ope,rators  <=  (le,ss  than  or  e,qual  to),  >=  (gre,ate,r  than  or  e,qual  to),  ==  (e,qual  to),  and!=  (not  e,qual  to).

Console,.log("itchy"  !=  "scratchy")

//  →  true,

Console,.log("apple,"  ==  "orange,")

//  →  false,

In  javascript,  the,re,  is  only  one,  value,  that  is  not  e,qual  to  itse,lf,  which  is  the,  nan  (“not  a  numbe,r”).

Console,.log(nan  ==  nan)

//  →  false,

Logical  ope,rator

Javascript  e,ndorse,s  only  thre,e,  ope,rators  that  you  can  apply  to  boole,an  value,s,  the,y  are,  and,  or,  and  not.  the,  &&  ope,rator  signifie,s  logical  or  and  its  re,sults  de,pe,nd  on  whe,re,  the,  value,s  impute,d  are,  true,  or  false,.

Console,.log(true,  &&  false,)

//  →  false,

Console,.log(true,  &&  true,)

//  →  true,

The,  ||  ope,rator  indicate,s  logical  or.  this  ope,rator  outputs  true,  if  the,  give,n  value,  is  true,.

Console,.log(false,  ||  true,)

//  →  true,

Console,.log(false,  ||  false,)

//  →  false,

An  e,xclamation  mark  (!)  indicate,s  not.  it  is  an  ope,rator  that  ove,rturns  the,  se,t  value,,  and  it  change,s  from  true,  to  false,  and  false,  to  true,.

The,  ||  consists  of  the,  lowe,st  pre,ce,de,nce,  of  all  ope,rators,  the,n  &&,  the,  comparison  ope,rators  (>,  ==,  e,tc.),  and  so  on.  the,  e,xample,  be,low  state,s  that  pare,nthe,se,s  are,  ne,ce,ssary:

1  +  1  ==  2  &&  10  *  10  >  50

E,mpty  value,s

Null  and  unde,fine,d  are,  the,  only  two  type,s  of  spe,cial  value,s  that  are,  use,d  to  indicate,  the,  non-appe,arance,  of  an  important  value,.  the,y  contain  ze,ro  data.

Automatic  type,  conve,rsion

E,arlie,r  i  said  that  javascript  acce,pts  practically  all  give,n  programs,  including  programs  with  odd  be,haviors.  automatic  type,  conve,rsion  illustrate,s  in  the,  following  e,xpre,ssions:

Console,.log(8  *  null)

//  →  0

Console,.log("5"  -  1)

//  →  4

Console,.log("5"  +  1)

//  →  51

Console,.log("five,"  *  2)

//  →  nan

Console,.log(false,  ==  0)

//  →  true,

Whe,n  you  assign  an  ope,rator  the,  wrong  value,,  javascript  sile,ntly  re,turns  that  value,  to  the,  e,xact  type,  it  re,quire,s  using  the,  type,  coe,rcion  rule,.  in  the,  first  e,xpre,ssion,  the,  null  turns  to  0,  and  the,  5  in  the,  se,cond  re,mains  5  (from  string  to  numbe,r).  in  the,  third  e,xpre,ssion,  the,re,  was  a  string  concate,nation  be,fore,  the,  nume,ric  addition,  which  conve,rts  the,  1  to  1  (from  numbe,r  to  a  string).  whe,n  odd  numbe,rs  such  as  "five,"  or  unde,fine,d  change,s  to  the,  numbe,r,  it  ge,ts  the,  value,  of  nan.  if  you  want  to  diffe,re,ntiate,  be,twe,e,n  value,s  of  the,  same,  type,  using  ==,  the,  output  should  be,  true,  if  the,  value,s  are,  similar  e,xce,pt  nan.  if  you  want  to  te,st  if  a  value,  contains  a  re,al  value,,  use,  the,  ==  (or!  =)  ope,rator  to  compare,  it.  to  ave,rt  une,xpe,cte,d  type,  conve,rsions,  use,  the,  thre,e,-characte,r  comparison  ope,rators.

Short-circuiting  of  logical  ope,rators

The,  &&  and  ||  are,  calle,d  the,  logical  ope,rators.  the,y  are,  use,d  to  hold  se,ve,ral  type,s  of  value,s  in  a  spe,cific  way.  the,y  change,  the,  value,s  containe,d  in  the,  le,ft  side,  to  boole,an  type,  to  de,cide,,  although  it  de,pe,nds  on  the,  ope,rators  and  the,  type,  of  ge,ne,rate,d  re,sult,  but  will  always  re,instate,  the,  le,ft  or  right-hand  value,.  the,  ||  ope,rator  se,nds  back  value,  to  the,  le,ft  whe,n  it  can  be,  change,d  to  true,  and  will  re,instate,  the,  value,  to  the,  right.

Console,.log(null  ||  "use,r")

//  →  use,r

Console,.log("kate,"  ||  "use,r")

//  →  kate,

This  function  is  use,d  to  re,turn  value,s  to  its  de,fault  value,  and  place,d  within  an  e,mpty  value,  as  a  re,place,me,nt.  strings  and  numbe,rs  to  boole,an  value,  conve,rsion  rule,s  indicate,  that  0,  nan,  and  e,mpty  string  (")  count  as  false,  while,  othe,r  value,s  are,  true,.  the,re,fore,  0  ||  -1  outputs  -1,  and  ""  ||  "!?"  yie,lds  "!?".  the,  &&  ope,rator  ope,rate,s  ide,ntically  but  the,  othe,r  way  around.  whe,n  value,s  to  the,  le,ft  can  be,  change,d  to  false,,  re,turn  the,  value,,  or  it  se,nds  the,  value,  to  the,  right.  both  ope,rators  e,valuate,  the,  value,  to  the,  right  only  whe,n  it  is  re,quire,d.  for  e,xample,,  we,  have,  the,  following  value,s  se,t  as  true,  ||  x,  the,  value,  of  x  will  be,  true,  and  will  not  conside,r  it.  the,  same,  rule,  applie,s  to  the,  false,  &&  x,  which  the,  x  is  false,  and  will  ove,rlook  it.  you  can  call  this  proce,ss  the,  short-circuit  e,valuation.

Summary

This  chapte,r  looks  at  the,  four  type,s  of  javascript  value,s,  which  are,  strings,  numbe,rs,  unde,fine,d  value,s  and  boole,ans.  the,se,  value,s  are,  de,ve,lope,d  by  inse,rting  the,ir  name,s  as  true,,  null  or  value,  (13,  "abc").  ope,rators  can  inte,grate,  and  change,  value,s.  we,  looke,d  at  binary  ope,rators  for  arithme,tic  (+,  -,  *,  /,  and  %),  string  concate,nation  (+),  comparison  (==,  !=,  ===,  !==,  <,  >,  <=,  >=),  and  logic  (&&,  ||),  and  also  various  unary  ope,rators  (-  to  nullify  a  numbe,r,  !  to  nullify  logically,  and  type,  of  to  se,arch  for  a  value,’s  type,)  and  a  te,rnary  ope,rator  (?:)  to  choose,  one,  of  two  value,s  de,pe,nding  on  a  third  value,.  you  will  ge,t  sufficie,nt  information  to  use,  javascript  like,  a  small  calculator,  and  you  will  improve,  in  the,  following  chapte,rs.

E,xe,rcise,

Write,  a  javascript  practice,  to  build  a  variable,  through a  use,r-de,fine,d  name,.

Solution

![00193.jpg](images/00193.jpeg) 

## Chapte,r  3:  program  structure,

We,  will  be,gin  the,  e,xpansion  of  the,  javascript  programming  language,  commands  be,yond  se,nte,nce,  fragme,nts  and  nouns.

E,xpre,ssions  and  state,me,nts

A  block  of  code,  that  manufacture,s  a  value,  is  calle,d  an  e,xpre,ssion.  a  single,  value,  is  writte,n  pre,cise,ly  as  22,  or  psychoanalysis  is  calle,d  an  e,xpre,ssion.  an  e,xpre,ssion  within  a  binary  ope,rator  se,t  to  two  e,xpre,ssions  or  within  pare,nthe,se,s  is  an  e,xpre,ssion.  an  e,xpre,ssion  that  can  accommodate,  othe,r  e,xpre,ssions  comparably  to  how  the,  human  language,  translate,s.  it  e,nable,s  us  to  de,ve,lop  e,xpre,ssions  that  narrate,  the,  arbitrarily  comple,x  computations.  whe,n  an  e,xpre,ssion  is  comparable,  to  a  se,nte,nce,  fragme,nt,  the,  javascript  state,me,nt  will  comple,te,  the,  se,nte,nce,.  a  list  of  state,me,nts  is  calle,d  a  program,  and  the,  most  acce,ssible,  type,  of  state,me,nt  is  a  line,  of  code,  with  a  se,micolon  e,nding  it.

For  instance,:

1;

!False,;

With  this  function,  a  state,me,nt  can  stand  inde,pe,nde,ntly,  and  it  can  add  a  fe,ature,  that  change,s  colors  occasionally  to  a  scre,e,n  or  modify  the,  inne,r  state,  of  the,  machine,  influe,ncing  the,  following  state,me,nts  afte,r  it.

Bindings

Javascript  use,s  binding  of  variable,s  to  hold  value,s,  for  instance,:

Ge,t  mone,y  =  5  *  5;

Ge,t  is  the,  ke,yword  in  that  state,me,nt,  and  it  me,ans  that  the,  se,nte,nce,  will  spe,cify  a  binding  toge,the,r  with  the,  binding  name,  and  value,  can  be,  attache,d  using  the,  =  ope,rator  and  an  e,xpre,ssion.  use,  a  de,fine,d  binding  as  an  e,xpre,ssion,  an  e,xpre,ssion  containing  the,  binding  value,.  he,re,  is  an  e,xample,  be,low:

Le,t  te,n  =  10;

Console,.log(te,n  *  te,n);

//  →  100

The,  =  ope,rator  is  use,d  on  e,xisting  bindings  to  re,move,  the,  binding  from  a  se,t  value,  and  point  the,m  to  a  ne,w  one,.

Le,t  mood  =  "light";

Console,.log(mood);

//  →  light

Mood  =  "dark";

Console,.log(mood);

//  →  dark

De,fining  a  binding  without  assigning  a  value,  will  re,sult  in  nothing  to  hold.  the,re,fore,,  asking  for  the,  value,  of  a  binding  produce,  the,  unde,fine,d  value,.  you  can  de,fine,  multiple,  binding  by  a  single,  state,me,nt  divide,d  by  commas.

Le,t  one,  =  1,  two  =  2;

Console,.log(one,  +  two);

//  →  3

Use,  the,  var  and  const  words  to  de,ve,lop  bindings  familiarly:

Var  name,  =  "ayad";

Const  gre,e,ting  =  "he,llo  ";

Console,.log(gre,e,ting  +  name,);

//  →  he,llo  ayad

The,  word  const  me,ans  constant.  it  de,scribe,s  a  re,solute,  binding,  which  points  to  its  se,t  value,  for  its  life,time,.  the,se,  words  are,  ofte,n  use,d  to  de,clare,  a  name,  to  a  value,  to  e,nable,  e,asy  re,fe,re,nce,  late,r  on.

Binding  name,s

Although  the,re,  are,  some,  re,se,rve,d  words  like,  const,  class,  de,fault,  bre,ak,  continue,,  de,le,te,,  do,  e,lse,  ye,t  any  word  can  be,  calle,d  a  binding  name,,  it  can  also  consist  of  digits  but  do  not  be,gin  the,  state,me,nt  with  a  figure,.  a  binding  name,  can  also  contain  dollar  signs  ($)  or  unde,rscore,s  (_)  but  do  not  e,nte,rtain  any  othe,r  spe,cial  characte,rs  or  punctuation.

The,  e,nvironme,nt

The,  group  of  binding  and  value,s  e,xisting  at  a  stipulate,d  time,  is  known  as  the,  e,nvironme,nt.  whe,n  you  launch  a  program,  the,  e,nvironme,nt  holds  the,  language,  standard  binding  and  ofte,n  contains  the,  binding  that  cre,ate,s  inte,raction  with  syste,m  surroundings.  for  instance,,  a  browse,r  carrie,s  functions  that  communicate,  with  the,  launche,d  we,bsite,  as  we,ll  as  re,ad  the,  ke,yboard  and  mouse,  input.

Functions

A  bit  of  program  e,nclose,d  in  value,  is  calle,d  a  function,  and  the,se,  value,s  are,  adde,d  to  launch  the,  wrappe,d  program.  for  instance,,  a  function  that  displays  a  small  dialog  box  for  use,r  input.

Prompt  ("e,nte,r  passcode,");

The,  proce,ss  of  e,ffe,cting  a  function  is  de,scribe,d  as  a  calling,  invoking,  or  applying.  call  a  function  by  inse,rting  pare,nthe,se,s  following  an  e,xpre,ssion  that  provide,s  a  function  value,.  se,t  the,  pare,nthe,sis  value,  to  the,  program  within  the,  function.  de,fine,  value,s  se,t  to  functions  as  argume,nts.

The,  console,.log  function

In  the,  above,  sample,s,  we,  use,d  the,  console,.log  to  output  value,s.  all  major  browse,rs  utilize,  the,  console,.log  function  to  state,  out  its  argume,nts  to  the,  de,vice,  that  outputs  the,  te,xt.  in  mode,rn  browse,rs,  the,  output  is  ofte,n  in  the,  javascript  console,  that  is  invisible,  by  de,fault;  you  can  tap  the,  f12  command  on  your  ke,yboard  or  the,  command-option-i  on  mac.  binding  name,s  do  not  accommodate,  pe,riod  characte,rs,  but  console,.log  doe,s  be,cause,  it  is  an  e,xpre,ssion  that  re,claims  the,  log  prope,rty  from  the,  console,  binding  value,.

Re,turn  value,s

Functions  are,  use,d  to  produce,  side,  e,ffe,cts.  the,y  can  also  provide,  value,s  that  do  not  ne,e,d  side,  e,ffe,cts.  for  instance,,  the,  function  calculate,.max  will  take,  a  sum  of  numbe,r  argume,nts  and  re,turns  the,  gre,ate,st.

Console,.log(calculate,.max(2,  4));

//  →  4

Javascript  re,gards  anything  that  provide,s  value,  as  an  e,xpre,ssion,  which  e,nable,s  function  calls  to  attach  into  the,  substantial  e,xpre,ssion.  le,t’s  call  the,  calculate,.min,  which  is  a  dire,ct  opposite,  to  calculate,.max:

Console,.log(math.min(2,  4)  +  100);

//  →  102

Control  flow

Whe,n  more,  than  one,  state,me,nt  is  within  a  program,  the,y  e,xe,cute,  in  a  story  form  from  the,  be,ginning  of  the,  code,  to  the,  e,nd.  this  type,  of  program  consists  of  two  type,s  of  state,me,nt;  the,  first  de,mand  numbe,rs  from  the,  use,r  while,  the,  se,cond  displays  the,  square,  of  the,  numbe,r  and  e,xe,cute,s  imme,diate,ly  afte,r  the,  first.

Le,t  the,numbe,r  =  numbe,r(prompt("se,le,ct  a  digit  "));

Console,.log("your  digit  is  the,  square,  root  of  "  +  the,numbe,r  *  the,numbe,r);

A  value,  is  change,d  to  a  numbe,r  by  the,  function  numbe,r  and  outputs  a  string  value,.

Conditional  e,xe,cution

The,  ke,yboard  is  use,d  to  de,ve,lop  conditional  e,xe,cutions  in  javascript.  you  may  want  some,  code,  to  e,xe,cute,  if,  and  only  if,  a  spe,cific  condition  is  positive,.  le,t  us  display  the,  square,  of  the,  input  if  only  it  is  a  numbe,r.

Le,t  the,numbe,r  =  numbe,r(prompt("se,le,ct  a  digit  "));

If  (!  numbe,r.isnan(the,numbe,r))  {

Console,.log("your  digit  is  the,  square,  root  of  "  +

The,numbe,r  *  the,numbe,r);

}

The,  if  ke,yword  pe,rforms  or  e,vade,s  a  state,me,nt  de,te,rmine,d  by  the,  boole,an  e,xpre,ssion  value,.  type,  the,  de,te,rmining  e,xpre,ssion  afte,r  the,  ke,yboard  within  the,  pare,nthe,se,s  accompanie,d  by  the,  state,me,nt  to  accomplish.

The,  numbe,r.isnan  function  is  a  high-le,ve,l  javascript  function  that  outputs  only  true,  if  the,  state,me,nt  is  de,clare,d  as  nan.  the,  numbe,r  function  re,turns  nan  whe,n  an  assigne,d  string  is  not  a  valid  numbe,r.  state,me,nts  afte,r  the,  if  state,me,nt  is  e,nclose,d  in  brace,s  ({and}).  brace,s  are,  use,d  to  cate,gorize,  diffe,re,nt  numbe,rs  of  state,me,nt  within  an  individual  state,me,nt.

28

If  (1  +  1  ==  2)  console,.log("it's  true,");

//  →  it's  true,

The,  e,lse,  ke,yword  can  be,  utilize,d  toge,the,r  with  the,  if  state,me,nt  to  provide,  two  diffe,re,nt  e,xe,cution  paths.

Le,t  the,numbe,r  =  numbe,r  (prompt("se,le,ct  a  digit"));

If  (!  numbe,r.isnan(the,numbe,r))  {

Console,.log("your  digit  is  the,  square,  root  of  "  +

The,numbe,r  *  the,numbe,r);

}  e,lse,  {

Console,.log("he,y.  why  didn't  you  give,  me,  a  numbe,r?");

}

If  the,re,  are,  more,  than  two  paths  to  choose,  from,  you  can  “chain”  multiple,

If/e,lse,  pairs  toge,the,r.  be,low  is  an  e,xample,:

Le,t  num  =  numbe,r  (prompt("pick  a  numbe,r"));

If  (num  <  10)  {

Console,.log("small");

}  e,lse,  if  (num  <  100)  {

Console,.log("me,dium");

}  e,lse,  {

Console,.log("large,");

}

The,  program  confirms  if  the,  num  is  le,ss  than  10,  and  if  it  is,  it  se,le,cts  that  branch,  and  the,n  displays  "small".  but  if  the,  num  is  gre,ate,r  than  10,  it  se,le,cts  the,  e,lse,  branch  which  consists  of  a  se,cond  if  state,me,nt  of  its  own.

While,  and  do  loops

This  is  the,  way  to  write,  a  program  that  displays  all  the,  e,ve,n  numbe,rs  from  0  to  12.

Console,.log(0);

Console,.log(2);

Console,.log(4);

Console,.log(6);

Console,.log(8);

Console,.log(10);

Console,.log(12);

A  way  to  run  a  clock  of  code,  multiple,  time,s  is  de,scribe,d  as  a  loop.

The,  looping  control  flow  e,nable,s  the,  use,r  to  re,turn  to  ce,rtain  points  in  writte,n  programs  and  re,do  it  with  the,  curre,nt  state,  of  the,  program.  inte,grate,  this  with  a  binding  that  e,nume,rate,s  as  follows:

Le,t  numbe,r  =  0;

While,  (numbe,r  <=  12)  {

Console,.log(numbe,r);

Numbe,r  =  numbe,r  +  2;

}

//  →  0

//  →  2

//  …  e,tce,te,ra

A  state,me,nt  that  be,gins  with  the,  ke,yword  and  at  the,  same,  time,  producing  a  loop.  the,  ke,yword  while,  accompanie,d  by  an  e,xpre,ssion  in  pare,nthe,se,s  followe,d  by  a  state,me,nt  like,  the,  if  state,me,nt.  the,  loop  be,come,s  continuous  until  the,  e,xpre,ssion  provide,s  a  value,  that  state,s  true,  whe,n  translate,d  to  boole,an.  e,ach  time,  the,  loop  re,pe,ats,  numbe,rs  adopt  a  numbe,r  twice,  of  the,ir  pre,vious  value,.  le,t  us  write,  a  program  that  e,valuate,s  and  display  the,  value,  of  210  (2  raise,d  to  the,  powe,r  of  10th).  we,  will  utilize,  two  bindings.  one,  to  ke,e,p  an  e,ye,  on  our  re,sult  and  the,  othe,r  to  calculate,  how  many  time,s  the,  value,  of  two  multiplie,d  by  the,  re,sult.  it  multiplie,s  until  the,  se,cond  binding  re,ache,s  10:

Le,t  re,sult  =  1;

Le,t  counte,r  =  0;

While,  (counte,r  <  10)  {

Re,sult  =  re,sult  *  2;

Counte,r  =  counte,r  +  1;

}

Console,.log(re,sult);

//  →  1024

A  do  loop  is  a  command  structure,  re,late,d  to  a  while,  loop.  a  do  loop  always  take,  place,  at  le,ast  once,  in  a  state,me,nt,  and  the,n  it  be,gins  to  che,ck  if  it  e,nds  afte,r  the,  first  e,xe,cution  only.  follow  the,  following  ste,ps:

Le,t  yourname,;

Do  {

Yourname,  =  prompt("who  are,  you?");

}  while,  (!  yourname,);

Console,.log(yourname,);

For  loops

A  lot  of  loops  follow  the,  while,  loop  patte,rn,  cre,ating  a  counte,r  binding  to  track  the,  loop's  progre,ss.  the,n  a  while,  loop  with  a  te,st  e,xpre,ssion  to  se,e,  if  the,  counte,r  re,ache,s  the,  se,t  value,.

For  (le,t  numbe,r  =  0;  numbe,r  <=  10;  numbe,r  =  numbe,r  +  4)  {

Console,.log(numbe,r);

}

//  →  0

//  →  4

//  e,tc

The,  pare,nthe,se,s  must  consist  of  two  se,micolons  afte,r  the,  ke,yword,  the,  first  part  that  is  be,fore,  the,  first  se,micolon  se,parate,s  the,  loop  by  de,scribing  a  binding.  the,  othe,r  part  is  the,  state,me,nt  that  de,te,rmine,s  if  the,  loop  should  continue,.  he,re,  is  the,  code,  that  e,valuate,  210  using  for  inste,ad  of  while,:

Le,t  re,sult  =  1;

For  (le,t  counte,r  =  0;  counte,r  <  10;  counte,r  =  counte,r  +  1)  {

Re,sult  =  re,sult  *  2;

}

Console,.log(re,sult);

//  →  1024

Bre,aking  out  of  a  loop

The,re,  are,  othe,r  ways  to  e,nd  a  loop  othe,r  than  making  a  looping  condition  give,  a  false,.  bre,ak  can  influe,nce,  jumping  out  of  the,  confine,d  loop.  the,  bre,ak  state,me,nt  e,valuate,s  this  program  if  the,  first  numbe,r,  which  is  both  gre,ate,r  than  or  e,qual  to  20,  and  can  be,  divide,d  by  7.

For  (le,t  curre,nt  =  20;  curre,nt  =  curre,nt  +  1)  {

If  (curre,nt  %  7  ==  0)  {

Console,.log(curre,nt);

Bre,ak;

}

}

//  →  21

The,  (%)  ope,rator  is  use,d  to  che,ck  if  a  numbe,r  can  be,  divide,d  by  anothe,r  numbe,r.  if  it  can  be,  divide,d,  the,n  the,  re,maining  division  is  ze,ro.  the,  for  in  the,  e,xample,  is  not  che,cke,d  at  the,  e,nd  of  the,  loop,  which  me,ans  until  the,  bre,ak  state,me,nt  inside,  is  imple,me,nte,d  the,  loop  be,come,s  infinite,  and  ne,ve,r  stops.

Updating  bindings  succinctly

Whe,n  you  are,  in  a  loop,  programs  will  update,  a  binding  re,gularly  to  store,  a  value,  base,d  on  its  pre,vious  value,.

Counte,r  =  counte,r  +  1;

Javascript  offe,rs  a  shortcut.

Counte,r  +=  1;

Re,late,d  shortcuts  function  for  se,ve,ral  othe,r  ope,rators,  like,  re,sult  *=  2  to  multiply  re,sult  or  counte,r  -=  1  to  count  in  de,sce,nding  orde,r.

This  e,nable,s  us  to  minimize,  our  counting  e,xample,.

For  (le,t  numbe,r  =  0;  numbe,r  <=  12;  numbe,r  +=  2)  {

Console,.log(numbe,r);

}

For  counte,r  +=  1  and  counte,r  -=  1,  he,re,  are,  shorte,r  e,quivale,nts:

Counte,r++  and  counte,r--.

Dispatching  on  a  value,  with  switch

Dispatching  on  a  value,  with  switch  code,s  can  look  like,  this:

If  (x  ==  "value,1")  action1();

E,lse,  if  (x  ==  "value,2")  action2();

E,lse,  if  (x  ==  "value,3")  action3();

E,lse,  de,faultaction();

The,  switch  is  use,d  to  e,xpre,ss  the,  above,  form  of  dispatch  straightforwardly.  be,low  is  a  good  e,xample,:

Switch  (prompt("what  is  the,  atmosphe,re,  like,?"))  {

Case,  "rainy":

Console,.log("do  not  forge,t  to  come,  with  an  umbre,lla.");

Bre,ak;

Case,  "sunny":

Console,.log("be,  light  with  your  dre,ssing.");

Case,  "cloudy":

Console,.log("move,  out.");

Bre,ak;

De,fault:

Console,.log("we,athe,r  type,  unknown!");

Bre,ak;

}

Capitalization

Name,s  binding  do  not  allow  space,s,  but  it  supports  the,  usage,  of  se,ve,ral  words  to  de,fine,  the,  binding  value,s.  he,re,  are,  a  fe,w  type,s  that  can  be,  utilize,d  whe,n  binding  name,s  with  diffe,re,nt  words:

Fuzzylittle,turtle,

Fuzzy_little,_turtle,

Fuzzylittle,turtle,

Fuzzylittle,turtle,

Comme,nts

Some,time,s  raw  code,s  do  not  transmit  e,ve,ry  single,  pie,ce,  of  information  that  you  want  the,  program  to  se,nd  to  re,ade,rs  or  spre,ads  the,  me,ssage,  in  a  way  pe,ople,  will  find  it  hard  to  de,ciphe,r.  othe,r  time,s  you  fe,e,l  like,  you  should  attach  some,  similar  thoughts  to  your  program,  the,  comme,nt  pe,rforms  this  function.  a  comme,nt  is  a  bit  chunk  of  the,  te,xt  containe,d  in  a  program,  but  the,  compute,r  ignore,s  it.  to  code,  a  single,  line,  comme,nt,  use,  the,  two  slash  characte,rs  (//),  followe,d  by  the,  comme,nt  te,xt.

Le,t  accountbalance,  =  calculate,balance,(account);

//  it's  a  ye,llow-orange,  on  the,  mango  tre,e,  accountbalance,.adjust();

//  catching  gre,e,n  tatte,rs  in  our  home,.  le,t  re,port  =  ne,w  re,port();

//  whe,re,  the,  sun  and  the,  moon  me,e,ts:  addtore,port(accountbalance,,  re,port);

//  it's  a  large,  hallway,  and  the,  lights  are,  quite,  amazing.

A  //  comme,nt  appe,ars  only  at  the,  e,nd  of  the,  line,.  any  te,xt  within  /*  and  */  ignore,  it,  and  it  doe,s  not  matte,r  if  it  contains  line,  bre,aks.  it  is  use,d  to  attach  blocks  of  information  about  a  program  or  file,.

Summary

Now  you  unde,rstand  that  you  can  de,ve,lop  a  program  through  the,  use,  of  state,me,nts,  which  state,me,nt  itse,lf  can  contain  se,ve,ral  state,me,nts.  state,me,nts  consist  of  e,xpre,ssions,  and  you  can  cre,ate,  e,xpre,ssions  through  smalle,r  e,xpre,ssions.  se,tting  state,me,nts  afte,r  e,ach  anothe,r  provide,s  an  e,xe,cute,d  program  from  top  to  bottom.  disturbance,s  can  also  come,  into  the,  flow  of  influe,nce,  through  conditional  (if,  e,lse,,  and  switch)  and  looping  (while,,  do,  and  for)  state,me,nts.  and  we,  touche,d  bindings,  the,y  cate,gorize,  bits  of  data  unde,r  a  name,,  and  the,y  can  also  track  state,  within  the,  program.  the,  de,fine,d  bindings  e,njoy  the,  e,nvironme,nt  be,tte,r.  we,  also  touche,d  on  the,  functions  se,ction  be,ing  unique,  value,s  that  summarize,  a  pie,ce,  of  program.  you  can  call  the,m  by  typing  functionname,(argume,nt1,  argume,nt2).  this  type,  of  function  call  is  an  e,xpre,ssion  and  can  provide,  value,.

E,xe,rcise,

Write,  a  javascript  program  that  displays  the,  large,r  and  acce,pts  double,  inte,ge,rs.

Solution

![00104.jpg](images/00104.jpeg)![00054.jpg](images/00054.jpeg)

It  is  important  to  know  that  you  can  write,  .le,ngth  at  the,  e,nd  of  a  string  to  find  its  le,ngth.

Le,t  abc  =  "abc";

Console,.log(abc.le,ngth);

//  →  3

## Chapte,r  4:  functions

Functions  are,  the,  alpha  and  ome,ga  of  javascript  programming  language,.  the,  conce,pt  of  e,nclosing  a  bit  of  program  containe,d  in  value,  has  a  lot  of  advantage,s.  it  provide,s  a  way  to  organize,  more,  promine,nt  programs,  to  minimize,  re,pe,tition,  re,late,  name,s  with  subprograms,  and  se,parate,  programs  from  the,mse,lve,s.  functions  are,  use,d  to  de,scribe,  ne,w  words.

De,fining  a  function

A  function  is  a  syste,matic  binding  whe,re,by  a  function  de,fine,s  the,  binding  value,.  the,  code,  be,low  indicate,s  a  function  that  provide,s  the,  square,  of  a  state,d  numbe,r:

Const  square,  =  function(x)  {

Re,turn  x  *  x;

};

Console,.log(square,(12));

//  →  144

Cre,ate,  a  function  with  an  e,xpre,ssion  that  be,gins  with  the,  ke,yboard  function.  functions  consists  of  a  body  and  a  se,t  of  parame,te,rs  that  accommodate,s  the,  ye,t  to  be,  e,xe,cute,d  state,me,nts  whe,n  you  call  a  function.  the,  function  body  should  always  be,  e,nclose,d  in  brace,s,  e,ve,n  whe,n  it  is  just  an  individual  state,me,nt.  a  function  can  contain  se,ve,ral  parame,te,rs  or  ze,ro  parame,te,r.  in  the,  be,low  e,xample,,  make,noise,  contains  no  parame,te,r  name,s  and  powe,r  consists  of  two:

Const  make,noise,  =  function()  {

Console,.log("pling!");

};

Make,noise,();

//  →  pling!

Const  powe,r  =  function(base,,  e,xpone,nt)  {

Le,t  re,sult  =  1;

For  (le,t  count  =  0;  count  <  e,xpone,nt;  count++)  {

Re,sult  *=  base,;

}

Re,turn  re,sult;

};

Console,.log(powe,r(2,  10));

//  →  1024

Some,  functions  can  cre,ate,  value,s  such  as  square,  and  powe,r  while,  some,  re,sults  only  into  a  side,  e,ffe,ct.  a  re,turn  ke,yword  that  doe,s  not  contain  an  e,xpre,ssion  at  the,  e,nd  will  be,  re,turne,d  as  unde,fine,d.

Bindings  and  scope,s

E,ve,ry  binding  consists  of  a  scope,  that  e,nable,s  the,  visibility  of  the,  binding.  whe,ne,ve,r  you  call  a  function,  ne,w  illustrations  of  binding  are,  de,ve,lope,d.  this  cre,ate,s  se,paration  be,twe,e,n  functions,  e,ve,ry  function  call  be,have,s  in  its  own  world  and  is  e,asy  to  unde,rstand.  functions  that  we,re,  de,clare,d  with  the,  var  ke,yword  in  the,  pre,-2015  javascript  and  can  be,  se,e,n  throughout  the,  global  scope,.  the,y  are,  abse,nt  in  a  function.

Le,t  x  =  10;

If  (true,)  {

Le,t  y  =  20;

Var  z  =  30;

Console,.log(x  +  y  +  z);

//  →  60

}

//  y  is  not  visible,  he,re,

Console,.log(x  +  z);

//  →  40

Ne,ste,d  scope,

Javascript  diffe,re,ntiate,  be,twe,e,n  the,  global  and  local  bindings.  you  can  cre,ate,  block  and  functions  within  the,  othe,r  functions  and  blocks  manufacturing  se,ve,ral  de,gre,e,s  of  locality.  for  instance,,  this  function  produce,s  the,  ne,e,de,d  compone,nts  to  make,  a  group  hummus  contains  anothe,r  function  within  it:

Const  hummus  =  function(factor)  {

Const  ingre,die,nt  =  function(amount,  unit,  name,)  {

Le,t  ingre,die,ntamount  =  amount  *  factor;

If  (ingre,die,ntamount  >  1)  {

Unit  +=  "s";

}

Console,.log(`${ingre,die,ntamount}  ${unit}  ${name,}`);

};

Ingre,die,nt(1,  "can",  "chickpe,as");

Ingre,die,nt(0.25,  "cup",  "tahini");

Ingre,die,nt(0.25,  "cup",  "le,mon  juice,");

Ingre,die,nt(1,  "clove,",  "garlic");

Ingre,die,nt(2,  "table,spoon",  "olive,  oil");

Ingre,die,nt(0.5,  "te,aspoon",  "cumin");

};

The,  code,  within  the,  compone,nt  function  can  acce,ss  the,  factor  binding  from  the,  oute,r  function.  the,  se,t  of  bindings  acce,ssible,  within  a  block  is  de,cide,d  by  the,  block  position  in  the,  program  te,xt.  e,ve,ry  local  scope,  can  acce,ss  the,  containe,d  local  scope,  and  e,ve,ry  scope,  can  as  we,ll  acce,ss  the,  global  scope,.  this  conce,pt  is  name,d  le,xical  scoping.

Functions  as  value,s

A  function  binding  ofte,n  be,have,s  as  a  name,  for  a  particular  block  of  program.  this  type,  of  binding  doe,s  not  change,  be,cause,  it  is  de,fine,d.  functions  can  be,  use,d  in  arbitrary  e,xpre,ssions  as  we,ll  as  use,d  to  save,  a  function  value,  into  a  ne,w  binding.  a  binding  that  store,s  a  function  is  a  syste,matic  binding  and  a  ne,w  value,  can  be,  assigne,d  like,:

Le,t  launchmissile,s  =  function()  {

Missile,syste,m.launch("now");

};

If  (safe,mode,)  {

Launchmissile,s  =  function()  {/*  do  nothing  */};

}

De,claration  notation

The,re,  is  a  little,  way  to  ge,ne,rate,  a  function  binding.  whe,n  you  use,  the,  function  ke,yword  at  the,  be,ginning  of  a  state,me,nt,  it  will  function  diffe,re,ntly.

Function  square,(x)  {

Re,turn  x  *  x;

}

This  state,me,nt  de,scribe,s  the,  binding  square,  and  dire,cts  it  at  a  state,d  function.  this  type,  of  function  de,finition  consists  of  one,  pre,cision.

Console,.log("my  mind  te,lls  me,  e,ve,ry  time,:",  future,());

Function  future,()  {

Re,turn  "ill  surpass  bill  gate,s";

}

Arrow  functions

Functions  contains  a  third  notation  that  doe,s  not  look  ide,ntical  to  the,  othe,rs.  you  can  use,  the,  arrow  (=>)  as  an  alte,rnative,  to  the,  function  ke,yword.  the,  arrow  (=>)  contains  an  e,qual  sign  and  the,  gre,ate,r  than  characte,r.

Const  powe,r  =  (base,,  e,xpone,nt)  =>  {

Le,t  re,sult  =  1;

For  (le,t  count  =  0;  count  <  e,xpone,nt;  count++)  {

Re,sult  *=  base,;

}

Re,turn  re,sult;

};

If  you  have,  just  one,  parame,te,r  name,,  e,xclude,  the,  pare,nthe,se,s  surrounding  the,  parame,te,r  list.  some,time,s  the,  body  is  a  single,  e,xpre,ssion  inste,ad  of  a  block  of  brace,s,  taking  back  the,  e,xpre,ssion  from  the,  function.  the,re,fore,,  square,  de,finitions  pe,rform  the,  same,  task.

Const  square,1  =  (x)  =>  {re,turn  x  *  x;};

Const  square,2  =  x  =>  x  *  x;

Whe,n  the,re,  is  no  parame,te,r  on  an  arrow  function,  its  parame,te,r  list  be,come,s  a  se,t  of  unoccupie,d  and  ine,ffe,ctive,  pare,nthe,se,s.

Const  horn  =  ()  =>  {

Console,.log("toot");

};

You  don’t  have,  to  use,  both  the,  function  e,xpre,ssions  and  arrow  functions  in  the,  language,,  the,y  offe,r  and  pe,rform  the,  same,  ope,rations.

The,  call  stacks

Le,t  us  take,  some,  time,  to  se,e,  how  control  goe,s  through  functions.  be,low  is  a  simple,  program  making  fe,w  function  calls:

Function  gre,e,t(who)  {

Console,.log("he,llo  "  +  who);

}

Gre,e,t("harry");

Console,.log("bye,");

The,  gre,e,tings  call  influe,nce,s  to  control  to  jump  to  the,  be,ginning  of  the,  function.  the,  function  call  console,.log  ge,ts  its  job  done,  and  se,ize,  control,  and  the,n  se,nd  control  back  to  the,  function.  the,  function  cycle,  e,nds  the,re,  and  transfe,rs  back  to  the,  place,  that  calls  it.  the,  flow  of  control  is  be,low:

Not  in  function

In  gre,e,t

In  console,.log

In  gre,e,t

Not  in  function

In  console,.log

Not  in  function

The,  compute,r  has  to  re,colle,ct  the,  conte,xt  in  which  the,  call  se,que,nce,s  occurre,d  be,cause,  functions  go  back  to  whe,re,  it's  calle,d  position.  whe,n  console,.log  comple,te,s,  it  must  re,turn  to  the,  e,nd  of  the,  program.  a  call  stack  is  a  place,  whe,re,  the,  compute,r  store,s  this  conte,xt.  whe,ne,ve,r  you  call  a  function,  the,  pre,se,nt  conte,xt  save,s  at  the,  top  of  this  stack.  by  the,  time,  a  function  goe,s  back,  it  e,radicate,s  the,  top  conte,xt  and  utilize,s  the,  conte,nt  for  continual  e,xe,cution.

The,  stack  ne,e,ds  space,  to  be,  save,d  into  within  the,  compute,r  me,mory.  the,  be,low  code,  e,xplains  this  by  que,rying  the,  compute,r  that  cre,ate,s  ze,ro  limitation  be,twe,e,n  two  functions  back  and  forth.

Function  chicke,n()  {

Re,turn  e,gg();

}

Function  e,gg()  {

Re,turn  chicke,n();

}

Console,.log(chicke,n()  +  "  came,  first.");

//  →  ??

Optional  argume,nts

The,  be,low  code,  functions  prope,rly  without  inte,rfe,re,nce,:

Function  square,(x)  {re,turn  x  *  x;}

Console,.log(square,(4,  true,,  "he,dge,hog"));

//  →  16

The,  square,  is  de,scribe,d  with  just  one,  parame,te,r  and  we,  call  it  thre,e,.  that  is  possible,  be,cause,  the,  programming  language,  disre,gards  the,  surplus  argume,nts  and  re,cognize,s  the,  square,  of  the,  first  one,.  javascript  is  ve,ry  tole,rant  about  the,  amount  of  argume,nts  be,ing  passe,d  to  a  function.  the,  good  side,  of  this  characte,r  is  that  it  e,nable,s  calling  functions  with  se,parate,  numbe,rs  of  argume,nts:

Function  minus(a,  b)  {

If  (b  ===  unde,fine,d)  re,turn  -a;

E,lse,  re,turn  a  -  b;

}

Console,.log(minus(10));

//  →  -10

Console,.log(minus(10,  5));

//  →  5

Whe,n  an  =  ope,rator  is  writte,n  afte,r  a  parame,te,r  and  an  e,xpre,ssion,  the,  e,xpre,ssion  value,  will  re,store,  the,  non-spe,cifie,d  argume,nt.  if  you  want  to  pass  and  not  produce,  the,  se,cond  argume,nt,  the,  de,fault  be,come,s  two  and  the,  function  acts  like,  a  square,.

Function  powe,r(base,,  e,xpone,nt  =  2)  {

Le,t  re,sult  =  1;

For  (le,t  count  =  0;  count  <  e,xpone,nt;  count++)  {

Re,sult  *=  base,;

}

Re,turn  re,sult;

}

Console,.log(powe,r(4));

//  →  16

Console,.log(powe,r(2,  6));

//  →  64

Closure,

The,  capability  to  use,  functions  as  value,s  is  couple,d  with  the,  fact  that  local  bindings  are,  cre,ate,d  again  whe,ne,ve,r  you  call  a  function.  the,  be,low  code,  displays  this  e,xample,;  it  de,scribe,s  a  wrap  value,,  a  function  that  de,ve,lops  a  local  binding  and  the,n  se,nds  back  a  function  that  e,nte,rs  and  re,turns  the,  local  binding.

Function  wrapvalue,(n)  {

Le,t  local  =  n;

Re,turn  ()  =>  local;

}

Le,t  wrap1  =  wrapvalue,(1);

Le,t  wrap2  =  wrapvalue,(2);

Console,.log(wrap1());

//  →  1

Console,.log(wrap2());

//  →  2

This  conce,pt  is  calle,d  closure,.  it  give,s  the,  use,r  the,  ability  to  re,fe,re,nce,  a  particular  instance,  of  a  local  binding  within  a  confining  scope,.  adding  a  fe,w  change,s,  our  pre,vious  e,xample,  can  turn  into  a  way  to  de,ve,lop  functions  that  accumulate,s  by  an  arbitrary  amount.

Function  multiplie,r(factor)  {

Re,turn  numbe,r  =>  numbe,r  *  factor;

}

Le,t  twice,  =  multiplie,r(2);

Console,.log(twice,(5));

//  →  10

Re,cursion

A  function  can  call  itse,lf  but  should  not  call  itse,lf  re,gularly  to  avoid  stack  ove,rflow.  re,cursive,  function  is  a  function  that  calls  itse,lf.  re,cursion  e,nable,s  fe,w  functions  writte,n  in  se,parate,  style,s.  for  instance,,  the,  be,low  code,  is  the,  e,xe,cution  of  powe,r.

Function  powe,r(base,,  e,xpone,nt)  {

If  (e,xpone,nt  ==  0)  {

Re,turn  1;

}  e,lse,  {

Re,turn  base,  *  powe,r(base,,  e,xpone,nt  -  1);

}

}

Console,.log(powe,r(2,  3));

//  →  8

The,re,  is  one,  proble,m  with  this  e,xe,cution.  it  is  slowe,r  compare,d  to  othe,r  looping  ve,rsions.  utilizing  a  single,  loop  is  conside,re,d  low  cost  than  the,  multiple,  calling  of  functions.  although  that  doe,s  not  make,  re,cursion  an  ine,ffe,ctive,  option  of  looping,  fe,w  proble,ms  are,  solve,d  with  re,cursion  e,asie,r  than  with  the,  use,  of  loops.  proble,ms  that  ne,e,d  inspe,cting  or  proce,ssing  se,ve,ral  branche,s.  che,ck  this  out:  we,  be,gin  from  numbe,r  1  and  continuously  add  5  or  multiply  by  3.  for  instance,,  the,  numbe,r  13  can  be,  obtaine,d  by  multiplying  by  3  and  the,  addition  of  5  twice,,  the,re,by  we,  cannot  attain  the,  15.  the,  code,  is  the,  re,cursive,  solution:

Function  findsolution(targe,t)  {

Function  find(curre,nt,  history)  {

If  (curre,nt  ==  targe,t)  {

Re,turn  history;

}  e,lse,  if  (curre,nt  >  targe,t)  {

Re,turn  null;

}  e,lse,  {

Re,turn  find(curre,nt  +  5,  `(${history}  +  5)`)  ||

Find(curre,nt  *  3,  `(${history}  *  3)`);

}

}

Re,turn  find(1,  "1");

}

Console,.log(findsolution(24));

//  →  (((1  *  3)  +  5)  *  3)

The,  inne,r  function  find  take,s  two  argume,nts,  the,  curre,nt  numbe,r  and  a  string  that  docume,nts  the,  proce,ss  of  attaining  this  numbe,r.  if  a  solution  is  found,  it  se,nds  back  a  string  that  displays  the,  route,  to  the,  targe,t  and  if  no  solution  is  found,  the,  re,turne,d  value,  will  be,  null.  to  achie,ve,  this,  the,  function  e,xe,cute,s  one,  of  thre,e,  actions.  if  your  targe,t  is  the,  is  the,  curre,nt  numbe,r,  you  can  attain  that  targe,t  by  using  the,  curre,nt  history  so  it  is  se,nt  back.  some,time,s  the,  numbe,r  is  large,r  than  the,  targe,t,  but  you  do  not  ne,e,d  to  e,xplore,  this  option  be,cause,  addition  and  subtraction  can  only  e,nlarge,  the,  numbe,r  so  it  is  se,nt  back  as  null.  if  you  re,main  be,ne,ath  the,  targe,t  numbe,r,  both  paths  that  be,gin  the,  curre,nt  numbe,r  is  trie,d  by  calling  itse,lf  twice,,  one,  to  add  and  the,  othe,r  to  multiply.  if  the,  first  call  se,nds  some,thing  valid  back  in  re,turn,  the,n  good,  if  not,  re,turn  the,  se,cond  call,  it  doe,s  not  matte,r  whe,the,r  a  string  or  null  is  provide,d.  be,low  is  an  illustration  of  how  functions  provide,  e,ffe,cts.  this  e,xample,  se,arche,s  for  a  re,me,dy  for  the,  numbe,r  13.

Find(1,  "1")

Find(6,  "(1  +  5)")

Find(11,  "((1  +  5)  +  5)")

Find(16,  "(((1  +  5)  +  5)  +  5)")

Too  big

Find(33,  "(((1  +  5)  +  5)  *  3)")

Too  big

Find(18,  "((1  +  5)  *  3)")

Too  big

Find(3,  "(1  *  3)")

Find(8,  "((1  *  3)  +  5)")

Find(13,  "(((1  *  3)  +  5)  +  5)")

Found!

The,  inde,ntation  spe,cifie,s  profound  of  the,  call  stack.

Growing  functions

Functions  can  be,  introduce,d  into  programs  in  two  ways.  the,  first  is  by  writing  similar  code,s  a  lot  of  time,s,  which  e,nable,s  more,  mistake,s  while,  the,  se,cond  is  to  se,arch  for  a  fe,w  functionalitie,s  that  have,  not  be,e,n  writte,n  and  de,se,rve,s  its  own  function.  you  can  be,gin  by  naming  the,  function  and  write,  the,  body.  be,low  is  an  e,xample,.  we,  will  write,  a  program  that  re,produce,  two  numbe,rs–the,  amount  of  chicke,n  and  cows  available,  on  a  farm.

007  cows

011  chicke,ns

Function  printfarminve,ntory(cows,  chicke,ns)  {

Le,t  cowstring  =  string(cows);

While,  (cowstring.le,ngth  <  3)  {

Cowstring  =  "0"  +  cowstring;

}

Console,.log(`${cowstring}  cows`);

Le,t  chicke,nstring  =  string(chicke,ns);

While,  (chicke,nstring.le,ngth  <  3)  {

Chicke,nstring  =  "0"  +  chicke,nstring;

}

Console,.log(`${chicke,nstring}  chicke,ns`);

}

Printfarminve,ntory(7,  11);

Writing  le,ngth  afte,r  a  string  e,xpre,ssion  de,te,rmine,s  the,  le,ngth  of  the,  particular  string.  the,  loop  continue,s  to  add  ze,ros  at  the,  be,ginning  of  the,  numbe,r  strings  until  the,y  comprise,  of  thre,e,  characte,rs.

He,re,  is  a  be,tte,r  atte,mpt:

Function  printze,ropadde,dwithlabe,l(numbe,r,  labe,l)  {

Le,t  numbe,rstring  =  string(numbe,r);

While,  (numbe,rstring.le,ngth  <  3)  {

Numbe,rstring  =  "0"  +  numbe,rstring;

}

Console,.log(`${numbe,rstring}  ${labe,l}`);

}

Function  printfarminve,ntory(cows,  chicke,ns,  pigs)  {

Printze,ropadde,dwithlabe,l(cows,  "cows");

Printze,ropadde,dwithlabe,l(chicke,ns,  "chicke,ns");

Printze,ropadde,dwithlabe,l(pigs,  "pigs");

}

Printfarminve,ntory(7,  11,  3);

Inste,ad  of  taking  out  the,  re,plicate,d  part  of  the,  program,  try  to  pick  out  an  individual  conce,pt  with  the,  following  ste,ps:

Function  ze,ropad(numbe,r,  width)  {

Le,t  string  =  string(numbe,r);

While,  (string.le,ngth  <  width)  {

String  =  "0"  +  string;

}

Re,turn  string;

}

Function  printfarminve,ntory(cows,  chicke,ns,  pigs)  {

Console,.log(`${ze,ropad(cows,  3)}  cows`);

Console,.log(`${ze,ropad(chicke,ns,  3)}  chicke,ns`);

Console,.log(`${ze,ropad(pigs,  3)}  pigs`);

}

Printfarminve,ntory(7,  16,  3);

A  function  can  also  be,  use,d  to  print  aligne,d  table,s  of  numbe,rs.

Functions  and  side,  e,ffe,cts

Functions  can  consist  of  side,  e,ffe,cts  and  re,turn  a  value,.  the,y  de,ve,lop  value,s  that  inte,grate,  e,asily  in  ne,w  ways  much  more,  than  functions  that  produce,  side,  e,ffe,cts.  a  pure,  function  is  a  unique,  value,  manufacturing  function  that  doe,s  not  de,pe,nd  on  e,ithe,r  code,  side,  e,ffe,cts.  for  instance,,  it  will  not  re,cognize,  a  global  binding  with  a  change,able,  value,.  it  also  consists  of  a  callable,  prope,rty  toge,the,r  with  the,  same,  argume,nts  and  produce,s  e,qual  value,.

Summary

In  this  chapte,r,  you  now  unde,rstand  how  to  write,  your  functions.  knowing  how  to  write,  the,  function  ke,yword  and  whe,n  to  use,  an  e,xpre,ssion,  you  can  now  build  a  function  value,.  whe,n  you  use,  a  function  as  a  state,me,nt,  it  can  se,t  a  binding  and  name,  a  function  to  be,  its  value,.  you  can  also  use,  arrow  functions  to  build  functions.

//  de,fine,  f  to  hold  a  function  value,

Const  f  =  function(a)  {

Console,.log(a  +  2);

};

//  de,clare,  g  to  be,  a  function

Function  g(a,  b)  {

Re,turn  a  *  b  *  3.5;

}

//  a  le,ss  ve,rbose,  function  value,

Le,t  h  =  a  =>  a  %  3;

The,  major  pe,rspe,ctive,  of  unde,rstanding  functions  is  knowing  the,  scope,s.  e,ve,ry  block  builds  a  ne,w  scope,.  parame,te,rs  and  bindings  se,t  in  a  spe,cific  scope,  are,  local  and  invisible,  from  the,  outside,.  bindings  se,t  with  var  act  diffe,re,ntly,  and  the,y  re,sult  in  the,  global  scope,.  diffe,re,ntiating  the,  tasks  that  the,  program  e,xe,cute,s  into  various  functions  is  important.  you  do  not  ne,e,d  to  re,pe,at  yourse,lf  ofte,n,  and  functions  can  arrange,  a  program  by  cate,gorizing  code,  into  bits  that  pe,rform  spe,cific  actions.

E,xe,rcise,

Write,  a  javascript  program  to  se,e,  if  a  numbe,r  is  e,ve,n  or  not.

Solution

![00171.jpg](images/00171.jpeg)![00125.jpg](images/00125.jpeg)![00091.jpg](images/00091.jpeg) 

## Chapte,r  5:  data  structure,s:  obje,cts  and  arrays

Data  layouts  de,ve,lop  from  boole,ans,  strings,  and  numbe,rs  fragme,nts.  se,ve,ral  type,s  of  information  use,  more,  than  one,  chunk.  obje,cts  e,nable,  the,  use,r  to  collate,  value,s  toge,the,r  with  othe,r  obje,cts  to  de,ve,lop  more,  compound  layouts.  in  this  chapte,r,  you  will  unde,rstand  the,  conce,pts  of  solving  a  re,al  proble,m  at  hand.

Data  se,ts

If  you  want  to  work  with  a  lot  of  digital  data,  you  must  re,pre,se,nt  the,  digital  data  in  the,  machine,  me,mory.  for  instance,,  you  ne,e,d  to  re,pre,se,nt  a  group  of  numbe,rs  like,  2,  3,  5,  7,  and  11.  now  le,t’s  ge,t  prolific  with  our  use,  of  strings  as  strings  can  contain  quite,  a  lot  of  data.  we,  will  use,  2  3  5  7  11  as  the,  re,pre,se,ntation.  javascript  programming  language,  offe,rs  a  unique,  data  type,  for  saving  se,que,nce,s  of  value,s,  which  is  calle,d  an  array.  write,  an  array  as  a  list  of  value,s  within  the,  be,twe,e,n  square,  bracke,ts,  diffe,re,ntiate,d  by  commas.

Le,t  listofnumbe,rs  =  [2,  3,  5,  7,  11];

Console,.log(listofnumbe,rs[2]);

//  →  5

Console,.log(listofnumbe,rs[0]);

//  →  2

Console,.log(listofnumbe,rs[2  -  1]);

//  →  3

The,  notation  use,d  to  ge,t  e,le,me,nts  within  an  array  also  utilize,  the,  square,  bracke,ts.  a  comple,te,  square,  bracke,ts  pair  right  afte,r  an  e,xpre,ssion  that  contains  anothe,r  e,xpre,ssion  within.  whe,n  you  start  counting  e,le,me,nts  in  an  array,  you  be,gin  from  ze,ro  and  not  one,.  the,re,fore,  the,  first  e,le,me,nt  is  re,de,e,me,d  with  listofnumbe,rs[0].

Prope,rtie,s

The,  pre,vious  chapte,rs  have,  containe,d  e,xpre,ssions  like,  the,  mystring.  le,ngth  (to  calculate,  the,  le,ngth  of  a  string)  and  math.max  (the,  maximum  function).  the,se,  are,  prope,rtie,s  that  can  approach  the,  prope,rty  value,s.  virtually  all  javascript  value,s  contain  prope,rtie,s.  the,  fe,w  value,s  that  do  not  contain  prope,rtie,s  are,  null  and  unde,fine,d.  if  you  acce,ss  a  prope,rty  with  a  nonvalue,,  the,  re,sult  will  be,  an  e,rror.

Null.le,ngth;

//  →  type,e,rror:  null  has  no  prope,rtie,s

In  javascript,  the,  two  major  ways  to  e,valuate,  prope,rtie,s  are,  with  a  dot  and  square,  bracke,ts.  the,  value,.x  and  value,[x]  can  e,valuate,  the,  prope,rty  on  value,,  not  particularly  the,  same,  prope,rty.  how  you  use,  x  is  diffe,re,nt  from  how  you  use,  a  dot.

If  you  want  to  use,  the,  dot,  the,  te,xt  you  input  afte,r  the,  dot  is  the,  name,  of  the,  prope,rty.  and  if  you're,  going  to  use,  the,  square,  bracke,ts,  the,  e,xpre,ssion  within  the,  bracke,ts  is  acce,sse,d  to  re,de,e,m  the,  prope,rty  name,.  value,.x  de,live,rs  the,  prope,rty  of  value,  calle,d  “x,”  while,  value,[x]  acce,sse,s  the,  e,xpre,ssion  x  and  utilize,  the,  re,sult,  transforme,d  into  a  string  as  the,  name,  of  the,  prope,rty.  if  the,  prope,rty  you  want  is  name,d  color,  you  should  type,  value,.color.  you  can  withdraw  the,  prope,rty  that  the,  value,  calle,d  within  the,  binding  i,  type,  value,[i].  the,  name,  of  prope,rtie,s  are,  strings,  but  the,  dot  notation  pe,rforms  with  only  valid  binding  name,s.  the,re,fore,  if  you  want  to  e,valuate,  a  prope,rty  name,d  2  or  john  doe,,  use,  the,  square,  bracke,ts:  value,[2]  or  value,["john  doe,"].

The,  e,le,me,nts  within  an  array  save,  as  the,  prope,rtie,s  of  an  array  that  utilize,  numbe,rs  as  prope,rty  name,s.  an  array's  le,ngth  prope,rty  de,te,rmine,s  how  many  ite,ms  it  contains.  the,  name,  of  that  prope,rty  is  a  valid,  binding  name,.  type,  array.le,ngth  to  de,te,rmine,  the,  le,ngth  of  an  array,  it  is  much  e,asie,r  to  type,  than  the,  array["le,ngth"].

Me,thods

The,  string  and  array  obje,cts  accommodate,  se,ve,ral  prope,rtie,s  that  store,  function  value,s.

Le,t  doh  =  "doh";

Console,.log(type,of  doh.touppe,rcase,);

//  →  function

Console,.log(doh.touppe,rcase,());

//  →  doh

E,ach  string  consists  of  a  touppe,rcase,  prope,rty.  whe,n  you  call  this  prope,rty,  it  se,nds  back  a  copy  of  the,  string  whe,re,by  all  the,  containing  le,tte,rs  transform  into  uppe,rcase,.  although  the,  touppe,rcase,  do  not  go  through  an  argume,nt,  the,  function  can  e,valuate,  the,  string  "doh,"  which  is  the,  prope,rty  of  the,  value,  we,  calle,d  above,.  prope,rtie,s  that  consist  of  functions  are,  known  as  me,thods.  the,  be,low  e,xample,  illustrate,s  two  me,thods  that  can  be,  use,d  to  influe,nce,  arrays.

Le,t  se,que,nce,  =  [1,  2,  3];

Se,que,nce,.push(4);

Se,que,nce,.push(5);

Console,.log(se,que,nce,);

//  →  [1,  2,  3,  4,  5]

Console,.log(se,que,nce,.pop());

//  →  5

Console,.log(se,que,nce,);

//  →  [1,  2,  3,  4]

The,  push  me,thod  is  use,d  to  attach  a  value,  to  the,  e,nd  of  an  array  while,  the,  pop  me,thod  doe,s  the,  dire,ct  opposite,.  it  e,radicate,s  the,  last  value,  within  an  array  and  se,nds  it  back.  the,se,  are,  ge,ne,rational  te,rms  of  ope,rations  on  a  stack.  a  stack  is  a  data  layout  that  e,nable,s  use,rs  to  push  value,s  in  and  pop  the,m  out  in  the,  opposite,  dire,ction  so  that  the,  adde,d  value,  will  re,move,  first.

Obje,cts

You  can  re,pre,se,nt  a  group  of  log  e,ntrie,s  as  an  array  although  e,ach  string  e,ntry  is  re,quire,d  to  save,  a  list  of  activitie,s  as  we,ll  as  a  boole,an  value,  that  spe,cifie,s  if  jacque,s  transforme,d  to  a  squirre,l  or  not.  we,  will  group  this  into  a  single,  value,  and  place,  the,  groupe,d  value,s  within  an  array  of  log  e,ntrie,s.  arbitrary  colle,ctions  of  prope,rtie,s  are,  the,  value,  of  the,  type,  obje,ct.  we,  will  de,ve,lop  an  obje,ct  utilizing  brace,s  as  an  e,xpre,ssion.

Le,t  day1  =  {

Squirre,l:  false,,

E,ve,nts:  ["work",  "touche,d  tre,e,",  "pizza",  "running"]

};

Console,.log(day1.squirre,l);

//  →  false,

Console,.log(day1.wolf);

//  →  unde,fine,d

Day1.wolf  =  false,;

Console,.log(day1.wolf);

//  →  false,

The,  brace,s  contain  a  list  of  prope,rtie,s  divide,d  by  commas.  e,ve,ry  prope,rty  contains  a  name,  accompanie,d  by  a  value,  and  a  colon.  whe,n  you  write,  an  obje,ct  ove,r  se,ve,ral  line,s,  make,  sure,  your  inde,nting  is  good  be,cause,  it  e,nable,s  be,tte,r  re,adability.  quote,  invalid  binding  name,s  prope,rtie,s  or  valid  numbe,rs  should.

Le,t  de,scriptions  =  {

Work:  "we,nt  to  work,"

"touche,d  tre,e,":  "touche,d  a  tre,e,."

};

You  can  use,  brace,s  in  two  diffe,re,nt  ways  in  javascript.  it  is  use,d  at  the,  be,ginning  of  a  state,me,nt  and  can  also  be,  utilize,d  to  be,gin  a  block  of  state,me,nts.  you  can  spe,cify  a  value,  to  a  prope,rty  e,xpre,ssion  using  the,  =  ope,rator.  it  take,s  the,  place,  of  the,  prope,rty  value,,  and  if  it  is  in  e,xiste,nce,,  it  de,ve,lops  a  ne,w  one,.  the,  de,le,te,  ope,rator  is  a  unary  ope,rator  that  e,radicate,s  the,  prope,rty  name,  of  an  obje,ct.  be,low  is  an  illustration:

Le,t  anobje,ct  =  {le,ft:  1,  right:  2};

Console,.log(anobje,ct.le,ft);

//  →  1

De,le,te,  anobje,ct.le,ft;

Console,.log(anobje,ct.le,ft);

//  →  unde,fine,d

Console,.log("le,ft"  in  anobje,ct);

//  →  false,

Console,.log("right"  in  anobje,ct);

//  →  true,

The,  binary  in  ope,ration  de,te,rmine,s  if  an  obje,ct  or  string  contains  a  name,d  prope,rty.  the,  major  diffe,re,ntiation  be,twe,e,n  spe,cifying  a  prope,rty  to  unde,fine,d  and  de,le,ting  it  is  that  the,  obje,ct  consists  of  a  prope,rty  and  the,  de,le,ting  doe,s  not  posse,ss  the,  prope,rty,  so  the,  value,  re,turns  as  false,.  to  de,te,rmine,  what  prope,rtie,s  containe,d  in  an  obje,ct  and  se,nds  back  an  array  of  strings  with  prope,rty  name,s  of  the,  obje,ct.

Console,.log(obje,ct.ke,y({x:  0,  y:  0,  c:  2}));

//  →  ["x",  "y",  "c"]

The,  obje,ct.assign  function  is  use,d  to  copy  prope,rtie,s  from  one,  obje,ct  to  anothe,r.

Le,t  obje,cta  =  {a:  1,  b:  2};

Obje,ct.assign(obje,cta,  {b:  3,  c:  4});

Console,.log(obje,cta);

//  →  {a:  1,  b:  3,  c:  4}

An  array  is  a  unique,  obje,ct  use,d  for  saving  succe,ssion  of  things.  whe,n  you  acce,ss  the,  type,of  [],  it  provide,s  "obje,ct."  the,  be,low  illustration  stands  for  the,  journal  that  jacque,s  store,s  as  an  array  of  obje,cts.

Le,t  journal  =  [

{e,ve,nts:  ["work",  "touche,d  tre,e,",  "pizza",

"running",  "te,le,vision"],

Squirre,l:  false,},

{e,ve,nts:  ["work",  "ice,  cre,am",  "cauliflowe,r",

"lasagna",  "touche,d  tre,e,",  "brushe,d  te,e,th"],

Squirre,l:  false,},

{e,ve,nts:  ["we,e,ke,nd",  "cycling",  "bre,ak",  "pe,anuts",

"be,e,r"],

Squirre,l:  true,},

/*  and  so  on...  */

];

Mutability

We,  have,  discusse,d  diffe,re,nt  value,s  such  as  boole,ans,  strings,  and  numbe,rs  whose,  value,s  are,  difficult  to  change,,  although  the,y  can  be,  combine,d  to  acquire,  ne,w  value,s  from  the,m.  obje,cts  are,  diffe,re,nt  from  value,s,  and  it  e,nable,s  prope,rty  changing;  the,y  can  cre,ate,  diffe,re,nt  conte,nt  for  a  single,  obje,ct  value,  at  diffe,re,nt  time,s.  whe,n  the,re,  are,  two  numbe,rs,  120  and  120,  the,y  are,  conside,re,d  the,  same,,  and  the,re,  is  a  similarity  be,twe,e,n  se,tting  two  re,fe,re,nce,s  to  one,  obje,ct  and  posse,ssing  two  se,parate,  obje,cts  containing  the,  same,  prope,rtie,s.  che,ck  the,  be,low  code,:

Le,t  obje,ct1  =  {value,:  10};

Le,t  obje,ct2  =  obje,ct1;

Le,t  obje,ct3  =  {value,:  10};

63

Console,.log(obje,ct1  ==  obje,ct2);

//  →  true,

Console,.log(obje,ct1  ==  obje,ct3);

//  →  false,

Obje,ct1.value,  =  15;

Console,.log(obje,ct2.value,);

//  →  15

Console,.log(obje,ct3.value,);

//  →  10

The,  obje,ct1  and  obje,ct2  bindings  hold  the,  same,  obje,ct,  and  that  is  why  alte,ring  obje,ct1  one,  influe,nce,s  the,  value,  of  obje,ct2.  the,y  are,  ide,ntical  by  nature,.  the,  binding  obje,ct3  points  to  a  se,parate,  obje,ct  that  consists  of  similar  prope,rtie,s  as  the,  obje,ct1  but  has  a  diffe,re,nt  life,.  bindings  can  be,  constant  or  change,able,,  but  it  doe,s  not  influe,nce,  the,ir  value,s.  a  const  binding  an  obje,ct  cannot  be,  transforme,d  and  re,le,ntle,ssly  pointing  to  the,  same,  obje,ct.  it  is  the,  obje,ct  conte,nts  that  can  be,  change,d.

Const  score,  =  {visitors:  0,  home,:  0};

//  this  is  okay

Score,.visitors  =  1;

//  this  isn't  allowe,d

Score,  =  {visitors:  1,  home,:  1};

Whe,n  the,  javascript’s  ==  ope,rator  is  use,d  to  diffe,re,ntiate,  obje,cts,  it  use,s  the,  ide,ntity  to  pe,rform  that  task.  it  will  translate,  true,  if  the,  obje,cts  contain  the,  same,  value,.  diffe,re,ntiating  se,ve,ral  obje,cts  will  re,turn  false,,  e,ve,n  if  the,ir  prope,rtie,s  are,  similar.

The,  lycanthrope,'s  log

So,  you  be,gin  your  javascript  inte,rpre,te,r  and  cre,ate,s  the,  e,nvironme,nt  you  ne,e,d  to  ke,e,p  your  journal.

Le,t  journal  =  [];

Function  adde,ntry(e,ve,nts,  squirre,l)  {

Journal.push({e,ve,nts,  squirre,l});

}

Inste,ad  of  proclaiming  prope,rtie,s  such  as  e,ve,nts,  it  se,ts  a  prope,rty  name,.

So  the,n,  at  10  p.m.  e,ve,ry  e,ve,ning  or  occasionally  in  the,  following  morning,  afte,r

Ge,tting  down  from  the,  top  she,lf  of  your  bookcase,,  your  daily  re,cords.

Adde,ntry(["work",  "touche,d  tre,e,",  "pizza",  "running",

"te,le,vision"],  false,);

Adde,ntry(["work",  "ice,  cre,am",  "cauliflowe,r",  "lasagna",

"touche,d  tre,e,",  "brushe,d  te,e,th"],  false,);

Adde,ntry(["we,e,ke,nd",  "cycling",  "bre,ak",  "pe,anuts",

"be,e,r"],  true,);

Corre,lation  is  an  e,valuation  of  vulne,rability  be,twe,e,n  analytical  variable,s.  the,y  are,  known  as  value,s  that  span  from  -1  to  1.  an  unre,late,d  variable,  is  calle,d  a  ze,ro  corre,lation.  a  corre,lation  of  1  signifie,s  that  the,  two  are,  re,late,d.  ne,gative,  me,ans  that  the,  variable,s  are,  re,late,d  pe,rfe,ctly  but  opposite,s  to  e,ach  othe,r;  one,  is  true,,  and  the,  othe,r  is  false,.  to  calculate,  the,  e,valuation  of  the,  corre,lation  be,twe,e,n  two  boole,an  value,s,  utilize,  the,  phi  coe,fficie,nt  (φ).  this  formula  input  is  a  fre,que,ncy  table,  holding  the,  numbe,r  of  time,s  it  notice,s  se,ve,ral  mixture,s  of  the,  variable,s.  the,  formula's  output  will  be,  a  numbe,r  be,twe,e,n  -1  and  1.  that  is  the,  be,st  de,finition  of  a  corre,lation.

Le,t  us  use,  the,  e,ve,nt  if  e,ating  pizza  as  an  e,xample,  and  inse,rt  it  into  a  fre,que,ncy  table,  whe,re,by  e,ve,ry  numbe,r  signifie,s  the,  total  of  time,s,  and  we,  use,d  the,  combination  in  our  me,asure,me,nts.  we,  name,  the,  table,  n,  and  we,  calculate,  φ  with  the,  be,low  formula:

Φ  =

N11n00  −  n10n01

√

N1•n0•n•1n•0

The,  notation  n01  signifie,s  the,  numbe,r  of  me,asure,me,nts  whe,re,  the,  first  variable,  turns  false,  (0),  and  the,  se,cond  variable,  be,come,s  true,  (1).  the,  pizza  table,,  n01  is  9.

The,  value,  n1•  indicate,s  the,  sum  of  all  me,asure,me,nts  whe,re,  the,  first  variable,  turns  true,,  that  is  5  in  the,  table,  e,xample,.  as  we,ll  as  n•0  sugge,sts  the,  quantity  of  the,  me,asure,me,nts  whe,re,  the,  se,cond  variable,  be,come,s  false,.

The,  pizza  table,,  the,  top  of  the,  division  line,  would  be,  1×76−4×9  =  40,  and  the,  be,low  part  be,low  would  be,  the,  square,  root  of  5×85×10×80,  or  √340000.  the,  re,sult  will  be,  φ  ≈  0.069,  which  is  tiny.  the,re,fore,,  e,ating  pizza  had  no  impact  on  transformations.

Computing  corre,lation

Javascript  e,nable,s  the,  re,pre,se,ntation  of  a  two-by-two  table,  with  four  e,le,me,nt  arrays  ([76,  9,  4,  1]).  othe,r  re,pre,se,ntations  such  as  an  array  holding  two  two-e,le,me,nt  ([[76,  9],  [4,  1]])  or  an  obje,ct  containing  prope,rty  name,s  such  as  "11"  and  "01",  and  the,  flat  array,  which  produce,s  the,  e,xpre,ssion  that  acce,ss  the,  chair  short.  we,  will  e,xplain  the,  indice,s  to  the,  array  as  two-bit  binary  numbe,rs,  whe,re,  the,  most  significant  digit  re,fe,rs  to  the,  squirre,l  variable,  while,  the,  le,ast  significant  re,fe,rs  to  the,  e,ve,nt  table,.  for  instance,,  the,  binary  numbe,r  10  re,fe,rs  to  the,  "jacque,s  did  turn  into  a  squirre,l"  case,  but  the,  e,ve,nts  didn’t  appe,ar.  it  occurre,d  four  tie,s  and  binary  is  2  in  de,cimal,  the,  numbe,r  is  store,d  as  an  inde,x  2  of  the,  array.  this  function  calculate,s  the,  φ  coe,fficie,nt  from  an  array:

Function  phi(chair)  {

Re,turn  (chair  [3]  *  chair  0]  -  chair  [2]  *  chair  [1])  /

Math.sqrt((chair  [2]  +  chair  [3])  *

(chair  [0]  +  chair  [1])  *

(chair  [1]  +  chair  [3])  *

(chair  [0]  +  chair  [2]));

}

Console,.log(phi([76,  9,  4,  1]));

//  →  0.068599434

The,  table,  re,quire,s  two  fie,lds  to  acquire,  fie,lds  like,  n1•  be,cause,  the,  total  numbe,r  of  rows  and  columns  are,  store,d  indire,ctly  into  our  data  layout.  if  you  want  to  e,xtract  a  two-by-two  table,  for  a  particular  e,ve,nt,  you  must  loop  across  all  the,  e,ntrie,s  and  calculate,  the,  numbe,r  of  time,s  the,  e,ve,nt  happe,ne,d  to  the,  squirre,l  transformations.

Function  table,for(e,ve,nt,  journal)  {

Le,t  table,  =  [0,  0,  0,  0];

For  (le,t  i  =  0;  i  <  journal.le,ngth;  i++)  {

Le,t  e,ntry  =  journal[i],  inde,x  =  0;

If  (e,ntry.e,ve,nts.include,s(e,ve,nt))  inde,x  +=  1;

If  (e,ntry.squirre,l)  inde,x  +=  2;

Table,[inde,x]  +=  1;

}

Re,turn  table,;

}

Console,.log(table,for("pizza",  journal));

//  →  [76,  9,  4,  1]

Arrays  consists  of  an  include,  me,thod,  which  is  use,d  to  che,ck  if  a  se,t  value,  e,xists  in  the,  array.  this  me,thod  is  use,d  by  the,  function  to  de,cide,  if  the,  e,ve,nt  name,  is  inte,re,ste,d  the,  state,d  e,ve,nt  list  for  a  give,n  day.

Array  loops

The,  table,for  function  contains  a  loop  like,  this:

For  (le,t  i  =  0;  i  <  journal.le,ngth;  i++)  {

Le,t  e,ntry  =  journal[i];

//  do  some,thing  with  e,ntry

}

This  type,  of  loop  is  use,d  in  high-le,ve,l  javascript

This  is  how  to  write,  that  type,  of  loop  in  mode,rn  javascript.

For  (e,ntrance,  of  journal)  {

Console,.log(`${e,ntrance,.e,ve,nts.le,ngth}  e,ve,nts.`);

}

With  a  loop  like,  this,  the,  loop  continue,s  across  the,  e,le,me,nts  of  the,  value,  spe,cifie,d  afte,r  of.  this  loop  is  use,d  for  strings  and  othe,r  data  layouts.

The,  final  analysis

A  corre,lation  is  calculate,d  for  e,ve,ry  type,  of  e,ve,nt  that  happe,ns  in  the,  data  se,t.  if  you  want  to  achie,ve,  that,  se,arch  e,ve,ry  type,  of  e,ve,nt.

Function  journale,ve,nts(journal)  {le,t  e,ve,nts  =  [];

For  (le,t  e,ntry  of  journal)  {

For  (le,t  e,ve,nt  of  e,ntry.e,ve,nts)  {

If  (!E,ve,nts.include,s(e,ve,nt))  {

E,ve,nts.push(e,ve,nt);

}

}

}

Re,turn  e,ve,nts;

}

Console,.log(journale,ve,nts(journal));

//  →  ["carrot",  "e,xe,rcise,",  "we,e,ke,nd",  "bre,ad",  …]

By  moving  across  e,ve,ry  e,ve,nt  and  making  additions  to  those,  that  are,  not  in  the,  e,ve,nts  array,  this  function  gathe,rs  all  the,  type,  of  e,ve,nt.

A  lot  of  corre,lations  appe,ar  to  lie,  close,  to  ze,ro.  e,ating  bre,ad,  carrots  or  pudding  doe,s  not  activate,  the,  squirre,l-lycanthropy.  it  happe,ns  ofte,n  during  the,  we,e,ke,nds.  using  that,  be,low  are,  all  the,  corre,lations.

For  (le,t  e,ve,nt  of  journale,ve,nts(journal))  {

Console,.log(e,ve,nt  +  ":",  phi(table,for(e,ve,nt,  journal)));

}

//  →  carrot:  0.0140970969

//  →  e,xe,rcise,:  0.0685994341

//  →  we,e,ke,nd:  0.1371988681

//  →  bre,ad:  -0.0757554019

//  →  pudding:  -0.0648203724

//  and  so  on...

Le,t  us  filte,r  re,sults  to  display  only  corre,lations  that  are,  gre,ate,r  than  0.1  or  le,ss  than  -0.1.

For  (le,t  e,ve,nt  of  journale,ve,nts(journal))  {

Le,t  corre,lation  =  phi(table,for(e,ve,nt,  journal));

If  (corre,lation  >  0.1  ||  corre,lation  <  -0.1)  {

Console,.log(e,ve,nt  +  ":",  corre,lation);

}

}

//  →  we,e,ke,nd:  0.1371988681

//  →  brushe,d  te,e,th:  -0.3805211953

//  →  candy:  0.1296407447

//  →  work:  -0.1371988681

//  →  spaghe,tti:  0.2425356250

//  →  re,ading:  0.1106828054

//  →  pe,anuts:  0.5902679812

In  a  corre,lation  factors,  one,  is  stronge,r  than  the,  othe,r.  e,ating  pe,anuts  has  a  powe,rful  chance,  of  transforming  into  a  squirre,l,  the,re,by  brushing  the,  te,e,th  has  a  notable,  ne,gative,  e,ffe,ct.  he,re,'s  some,thing:

For  (le,t  e,ntry  of  journal)  {

If  (e,ntry.e,ve,nts.include,s("pe,anuts")  &&

!E,ntry.e,ve,nts.include,s("brushe,d  te,e,th"))  {

E,ntry.e,ve,nts.push("pe,anut  te,e,th");

}

}

Console,.log(phi(table,for("pe,anut  te,e,th",  journal)));

//  →  1

Furthe,r  arrayology

He,re,  are,  a  fe,w  more,  obje,ct-re,late,d  conce,pts  you  should  know.  we,  be,gin  with  the,  use,  of  some,  use,ful  me,thods  of  an  array.

The,  adding  and  re,moving  of  me,thods  things  at  the,  be,ginning  of  an  array  are,  calle,d  unshift  and  shift.

Le,t  todolist  =  [];

Function  re,me,mbe,r(task)  {

Todolist.push(task);

}

Function  ge,ttask()  {

Re,turn  todolist.shift();

}

Function  re,me,mbe,rurge,ntly(task)  {

Todolist.unshift(task);

}

The,  above,  program  organize,s  a  chain  of  tasks.  you  can  add  tasks  to  the,  e,nd  of  the,  que,ue,  by  calling  re,me,mbe,r("groce,rie,s"),  and  whe,n  you  want  to  ge,t  some,thing  done,,  call  ge,ttask()  to  ge,t  (and  re,move,)  ite,m  from  the,  que,ue,.  if  you  want  to  se,arch  for  a  particular  value,,  arrays  supply  an  inde,xof  me,thod.  the,  me,thod  finds  its  way  through  the,  array  from  the,  be,ginning  to  the,  e,nd  and  se,nds  back  the,  inde,x  the,  value,  re,que,ste,d,  if  it  was  found  it  re,turns  —or  -1  if  it  wasn’t  found.  to  se,arch  from  the,  be,ginning  to  the,  e,nd,  use,  the,  lastinde,xof  me,thod.

Console,.log([1,  2,  3,  2,  4].inde,xof(3));

//  →  1

Console,.log([1,  2,  3,  2,  4].lastinde,xof(3));

//  →  3

The,  inde,xof  and  lastinde,xof  take,s  a  voluntary  argume,nt  that  spe,cifie,s  whe,re,  the,  se,arch  be,gins.  anothe,r  gre,at  me,thod  is  the,  slice,,  this  me,thod  be,gins  and  e,nds  the,  indice,s  and  se,nd  back  an  array  containing  thre,e,  e,le,me,nts.  the,  be,ginning  is  inclusive,  while,  the,  e,nd  is  e,xclusive,.

Console,.log([0,  1,  2,  3,  5].slice,(2,  4));

//  →  [2,  3]

Console,.log([0,  1,  2,  3,  5].slice,(2));

//  →  [2,  3,  5]

If  the,  e,nd  inde,x  is  not  state,d,  slice,  take,  all  the,  e,le,me,nts  afte,r  the,  start  inde,x.  you  can  use,  the,  concat  me,thod  to  glue,  arrays  toge,the,r  to  produce,  a  ne,w  array.  the,  be,low  e,xample,  displays  concat  and  slice,  in  action.

Function  re,move,(arrays,  inde,x)  {

Re,turn  array.slice,(0,  inde,x)

.concat(arrays.slice,(inde,x  +  1));

}

Console,.log(re,move,(["a",  "k",  "c",  "f",  "e,"],  2));

//  →  ["a",  "k",  "f",  "e,"]

Strings  and  the,ir  prope,rtie,s

During  the,  string  value,  chapte,r,  we,  discusse,d  le,ngth  and  touppe,rcase,  but  if  you  want  to  add  a  ne,w  prope,rty,  it  doe,s  not  stick.

Le,t  kim  =  "kim";

Kim.age,  =  88;

Console,.log(kim.age,);

//  →  unde,fine,d

All  strings  value,  contains  a  fe,w  me,thods.  some,  are,  the,  slice,  and  inde,xof  which  have,  a  similar  appe,arance,  of  array  me,thods  as  we,ll  as  the,  name,.

Console,.log("coconuts”.  slice,(4,  7));

//  →  nut

Console,.log("coconut”.inde,xof("u"));

//  →  5

A  string’s  inde,xof  can  look  for  a  string  holding  more,  than  one,  characte,r,  while,  the,  corre,sponding  array  me,thod  se,arch  for  a  single,  e,le,me,nt.

Console,.log("one,  two  thre,e,".inde,xof("e,e,"));

//  →  11

The,  trim  me,thod  e,radicate,s  white,space,  from  the,  be,ginning  to  the,  e,nd  of  a  string.

Console,.log("  okay  \n  ".trim());

//  →  okay

The,  ze,ropad  function  can  also  be,  calle,d  a  padstart,  it  take,s  the,  pre,fe,rre,d  padding  and  le,ngth  characte,r  as  argume,nts.

Console,.log(string(6).padstart(3,  "0"));

//  →  006

You  can  bre,ak  a  string  on  e,ve,ry  de,ve,lopme,nt  of  anothe,r  string  with  split  and  the,n  join  the,m  toge,the,r  with  join.

Le,t  se,nte,nce,  =  "se,cre,tarybirds  spe,cialize,  in  stomping";

Le,t  words  =  se,nte,nce,.split("  ");

Console,.log(words);

//  →  ["se,cre,tarybirds",  "spe,cialize,",  "in",  "stomping"]

Console,.log(words.join(".  "));

//  →  se,cre,tarybirds.  spe,cialize,.  in.  stomping

You  can  use,  the,  re,pe,at  me,thod  to  re,pe,at  a  string,  which  de,ve,lops  a  ne,w  string  holding  se,ve,ral  copie,s  of  the,  original  string  attache,d  toge,the,r.

Console,.log("la".re,pe,at(3));

//  →  lalala

If  you  want  to  acce,ss  individual  characte,rs  in  a  string.  look  be,low:

Le,t  string  =  "abc";

Console,.log(string.le,ngth);

//  →  3

Console,.log(string[1]);

//  →  b

Re,st  parame,te,rs

It  is  important  for  a  function  to  re,ce,ive,  any  numbe,r  of  argume,nts.  if  you  want  to  write,  such  a  function,  add  thre,e,  dots  be,fore,  the,  last  parame,te,r  of  the,  function.

Function  max  (...numbe,rs)  {

Le,t  re,sult  =  -infinity;

For  (le,t  numbe,r  of  numbe,rs)  {

If  (numbe,r  >  re,sult)  re,sult  =  numbe,r;

}

Re,turn  re,sult;

}

Console,.log(max(4,  1,  9,  -2));

//  →  9

Whe,n  you  call  a  function,  the,  re,st  of  the,  parame,te,rs  be,longs  to  an  array  holding  the,  re,st  of  the,  argume,nts.  you  can  also  utilize,  the,  thre,e,  dot  notation  to  call  functions  within  an  array  of  argume,nts.

Le,t  numbe,rs  =  [5,  1,  7];

Console,.log(max(...numbe,rs));

//  →  7

Spre,ad  the,  array  out  into  a  function  call,  pass  the,  e,le,me,nt  diffe,re,nt  argume,nts,  like,  max  (9,  ...numbe,rs,  2).  the,  square,  bracke,t  array  notation  e,nable,s  the,  triple,-dot  ope,rator  bring  anothe,r  array  into  a  ne,w  array.

Le,t  words  =  ["ne,ve,r",  "fully"];

Console,.log(["will",  ...words,  "unde,rstand"]);

//  →  ["will",  "ne,ve,r",  "fully",  "unde,rstand"]

The,  math  obje,cts

The,  math  obje,ct  is  utilize,d  as  ve,sse,l  to  collate,  a  lot  of  similar  functionality.  it  produce,s  a  name,space,  to  e,nable,  value,s  a  functions  and  functions  without  global  bindings.  this  is  the,  old  way  to  write,  the,  constant  value,  name,  in  all  caps.

Function  randompointoncircle,(radius)  {

Le,t  angle,  =  math.random()  *  2  *  math.pi;

Re,turn  {x:  radius  *  math.cos(angle,),

Y:  radius  *  math.sin(angle,)};

}

Console,.log(randompointoncircle,(2));

//  →  {x:  0.3667,  y:  1.966}

The,  math  function  se,nds  back  a  ne,w  pse,udo  random  numbe,r  be,twe,e,n  ze,ro  and  one,  whe,ne,ve,r  you  call  it.

Console,.log(math.random());

//  →  0.36993729369714856

75

Console,.log(math.random());

//  →  0.727367032552138

Console,.log(math.random());

//  →  0.40180766698904335

Whe,n  you  ne,e,d  a  whole,  random  numbe,r  and  not  the,  fractional  one,,  you  can  utilize,  the,  math.floor  on  the,  outcome,  of  the,  math.random.

Console,.log(math.floor(math.random()  *  10));

//  →  2

The,  random  numbe,r  is  multiplie,d  by  10  and  outputs  a  numbe,r  gre,ate,r  than  or  e,qual  to  0  and  be,low  10.  re,me,mbe,r  the,  math.floor  rounds  down,  the,  output  will  be,  any  numbe,r  from  0  through  9.  the,  math  obje,ct  contains  se,ve,ral  functions  like,  the,  math.ce,il,  which  rounds  up  to  a  whole,  numbe,r,  and  the,  math.round,  which  rounds  up  to  the,  ne,are,st  whole,  numbe,r,  and  math.abs,  this  function  take,s  the,  e,ntire,  value,  of  a  numbe,r.

De,structuring

Le,t’s  use,  the,  phi  function  a  little,  bit.

Function  phi(chair)  {

Re,turn  (table,[3]  *  chair[0]  -  table,[2]  *  chair[1])  /

Math.sqrt((chair  [2]  +  chair  [3])  *

(table,[0]  +  chair  [1])  *

(table,[1]  +  chair  [3])  *

(table,[0]  +  chair  [2]));

}

One,  of  the,  fe,w  re,asons  this  function  is  hard  to  re,ad  is  be,cause,  the,re,  is  a  binding  dire,cte,d  to  the,  array,  but  we,  want  bindings  for  the,  e,le,me,nts  of  the,  array,  that  is,  le,t  n00  =  table,[0]  and  so  on.  although,  the,re,  is  a  be,tte,r  way  to  ge,t  this  done,  in  javascript.

Function  phi([n00,  n01,  n10,  n11])  {

Re,turn  (n11  *  n00  -  n10  *  n01)  /

Math.sqrt((n10  +  n11)  *  (n00  +  n01)  *

(n01  +  n11)  *  (n00  +  n10));

}

This  function  also  pe,rforms  brilliantly  with  the,  bindings  de,ve,lope,d  by  the,  le,ft,  var,  or  const.  if  your  pre,fe,rre,d  binding  value,  is  an  array,  utilize,  the,  square,  bracke,ts  to  che,ck  for  the,  value,  of  its  binding  conte,nts.  use,  the,  same,  conce,pt  for  obje,cts,  utilize,  the,  brace,s  and  not  the,  square,  bracke,ts.

Le,t  {name,}  =  {name,:  "faraji",  age,:  23};

Console,.log(name,);

//  →  faraji

Json

Json  re,pre,se,nts  javascript  obje,ct  notation  and  it  is  utilize,d  as  a  communication  format  and  data  storage,  for  the,  we,b.  json  is  ve,ry  similar  to  javascript  in  its  writing  style,  of  arrays  and  obje,ct,  although  the,re,  are,  re,strictions.  its  prope,rty  name,s  should  be,  e,nclose,d  within  double,  quote,s,  it  allows  only  simple,  data  e,xpre,ssions,  binding  e,tc.  json  do  not  allow  comme,nts.

He,re,  is  a  sample,  of  a  journal  e,ntry  re,pre,se,nte,d  as  json  data:

{

"squirre,l":  false,,

"e,ve,nts":  ["work",  "touche,d  tre,e,",  "pizza",  "running"]

}

Javascript  consists  of  the,  functions  json.stringify  and  json.parse,  to  transform  data  to  and  from  this  format.  json.stringify  take,s  a  javascript  value,  and  se,nds  back  a  json-e,ncode,d  string  while,  json.parse,  take,s  a  string  and  transforms  it  to  its  e,ncode,d  value,.

Le,t  string  =  json.stringify({squirre,l:  false,,

E,ve,nts:  ["we,e,ke,nd"]});

Console,.log(string);

//  →  {"squirre,l":false,,"e,ve,nts":["we,e,ke,nd"]}

Console,.log(json.parse,(string).e,ve,nts);

//  →  ["we,e,ke,nd"]

Re,ve,rsing  an  array

Arrays  consist  of  the,  re,ve,rse,  me,thod,  which  is  use,d  to  change,  an  array  by  re,ve,rsing  the,  orde,r  that  its  e,le,me,nts  display.

Summary

We,  cove,re,d  the,  obje,cts  and  arrays  in  this  chapte,r,  and  the,y  cre,ate,  ways  to  cate,gorize,  various  value,s  in  a  single,  value,.  fancifully,  this  e,nable,s  you  to  inse,rt  se,ve,ral  associate,d  ite,ms  in  a  bag  and  move,  about  with  the,  bag,  rathe,r  than  e,nclosing  your  arms  around  e,ve,ry  singular  thing  and  trying  to  ke,e,p  the,m  diffe,re,ntly.  a  lot  of  value,s  in  javascript  contain  prope,rtie,s,  the,  inconsiste,ncy  be,ing  unde,fine,d  and  null.  you  can  acce,ss  prope,rtie,s  using  the,  value,.prop  or  value,["prop"].  you  can  use,  name,s  for  obje,cts  prope,rtie,s  and  save,  a  de,fine,d  se,t  of  the,m.  arrays,  as  we,ll  contain  diffe,re,nt  amounts  of  similar  fanciful  value,s  and  utilize,  the,  numbe,rs  (be,ginning  from  0)  as  the,  prope,rty’s  name,s.  arrays  contain  fe,w  se,ts  of  prope,rtie,s,  which  are,  the,  le,ngth  and  se,ve,ral  me,thods.  me,thods  are,  functions  that  re,side,  within  prope,rtie,s  and  be,have,  on  the,  value,  the,y  are,  its  prope,rty.  you  can  loop  across  arrays  through  a  unique,  type,  of  for  loop—for  (the,  le,t  e,le,me,nt  of  an  array).

E,xe,rcise,

Write,  a  javascript  function  to  obtain  the,  first  ite,m  in  an  array.  se,tting  a  parame,te,r  'n'  will  se,nd  back  the,  first  'n'  e,le,me,nts  of  the,  array.

Data:

Console,.log(array_clone,([1,  2,  4,  0]));

Console,.log(array_clone,([1,  2,  [4,  0]]));

[1,  2,  4,  0]

[1,  2,  [4,  0]]

Solutions

![00035.jpg](images/00035.jpeg)![00184.jpg](images/00184.jpeg)

## Chapte,r  6:  highe,r-orde,r  functions

A  large,  program  take,s  time,  to  de,ve,lop  and  produce,s  a  lot  of  space,  for  bugs  to  hide,,  which  in  turn  make,s  the,m  hard  to  find.  he,re,  are,  e,xample,s  of  two  large,  programs:

The,  first  is  se,lf-containe,d,  and  the,  state,me,nt  is  six  line,s  long.

Le,t  total  =  0,  count  =  1;

While,  (count  <=  10)  {

Total  +=  count;

Count  +=  1;

}

Console,.log(total);

The,  se,cond  de,pe,nds  on  two  e,xte,rnal  functions,  and  the,  state,me,nt  is  one,  line,  long.

Console,.log(sum(range,(1,  10)));

Abstraction

Whe,n  it  come,s  to  javascript  programming  language,,  vocabulary’s  use,  the,  te,rm  abstraction.  abstraction  is  use,d  to  hide,  de,tails  and  give,s  the,  use,r  the,  capability  to  talk  about  proble,ms  on  a  highe,r  le,ve,l.  le,t  us  diffe,re,ntiate,  two  re,cipe,s  for  pe,a  soup.  first:

Pe,r  pe,rson,  place,  1  cup  of  drie,d  pe,as  within  a  containe,r.  put  e,nough  wate,r  to  cove,r  the,  pe,as,  le,t  it  soak  for  about  12  hours.  re,move,  it  from  the,  wate,r  and  place,  it  in  a  pot  use,d  for  cooking  with  the,  addition  of  wate,r  four  cups  of  wate,r  (4  cups).  le,t  it  boil  for  about  two  hours,  pe,r-pe,rson  hold  half  of  an  onion,  slice,  it  using  a  knife,,  and  pour  it  into  the,  pe,as,  le,t  it  pre,pare,  for  10  minute,s.

The,n  the,  se,cond  re,cipe,

Pe,r  pe,rson:  half  an  onion,  a  stalk  of  ce,le,ry,  1  cup  drie,d  split  pe,as,  and  a  carrot.

Dip  the,  pe,as  into  the,  wate,r  for  about  12  hours.  boil  it  for  about  2  hours  in  wate,r  (4  cups),  attach  and  slice,  ve,ge,table,s.  cook  it  for  10  minute,s.

The,  compute,r  pe,rforms  tasks  one,  by  one,,  from  blind  to  high-le,ve,l  conce,pts.

Abstracting  re,pe,tition

Plain  functions  are,  use,d  to  cre,ate,  abstractions.  it  is  habitual  for  a  program  to  re,pe,at  a  particular  function  a  spe,cifie,d  amount  of  time,.  you  can  achie,ve,  that  with  a  loop  like,  this:

83

For  (le,t  i  =  0;  i  <  10;  i++)  {

Console,.log(i);

}

He,re,  we,  write,  a  function  that  calls  console,.log  n  time,s.

Function  re,pe,atlog(n)  {

For  (le,t  i  =  0;  i  <  n;  i++)  {

Console,.log(i);

}

}

If  you  want  to  pe,rform  a  task  diffe,re,nt  from  logging  in  numbe,rs,  you  can  roll  action  as  a  function  value,.

Function  re,pe,at(n,  action)  {

For  (le,t  i  =  0;  i  <  n;  i++)  {

Action(i);

}

}

Re,pe,at(3,  console,.log);

//  →  0

//  →  1

//  →  2

Some,time,s  you  do  not  ne,e,d  to  roll  in  a  pre,de,fine,d  function  to  re,pe,at  in  a  loop,  cre,ate,  a  function  value,  as  an  alte,rnative,:

Le,t  labe,ls  =  [];

Re,pe,at(5,  i  =>  {

Labe,ls.push(`unit  ${i  +  1}`);

});

Console,.log(labe,ls);

//  →  ["unit  1",  "unit  2",  "unit  3",  "unit  4",  "unit  5"]

This  me,thod  layout  looks  similar  to  a  loop;  it  de,fine,s  the,  type,  of  loop  and  the,n  produce,  a  body.  although  the,  body  is  writte,n  in  function  e,nclose,d  in  pare,nthe,se,s  of  the,  call  to  re,pe,at.

Highe,r-orde,r  functions

Highe,r-orde,r  functions  are,  functions  that  work  on  othe,r  functions  whe,the,r  by  argume,nts  or  by  se,nding  the,m  back.  this  type,  of  function  e,nable,s  use,r  to  abstract  ove,r  actions.  for  instance,,  you  have,  a  function  that  can  produce,  functions

Function  gre,ate,rthan(n)  {

Re,turn  m  =>  m  >  n;

}

Le,t  gre,ate,rthan10  =  gre,ate,rthan(10);

Console,.log(gre,ate,rthan10(11));

//  →  true,

You  can  also  have,  functions  that  can  transform  othe,r  functions.

Function  noisy(f)  {

Re,turn  (...args)  =>  {

Console,.log("calling  with",  args);

Le,t  re,sult  =  f(...args);

Console,.log("calle,d  with",  args,  ",  re,turne,d",  re,sult);

Re,turn  re,sult;

};

}

Noisy(math.min)(3,  2,  1);

//  →  calling  with  [3,  2,  1]

//  →  calle,d  with  [3,  2,  1],  re,turne,d  1

You  can  as  we,ll  write,  functions  that  produce,  ne,w  se,t  of  control  flow.

Function  unle,ss(te,st,  the,n)  {

If  (!Te,st)  the,n();

}

85

Re,pe,at(3,  n  =>  {

Unle,ss(n  %  2  ==  1,  ()  =>  {

Console,.log(n,  "is  e,ve,n");

});

});

//  →  0  is  e,ve,n

//  →  2  is  e,ve,n

This  me,thod  is  a  built-in  array  me,thod,  fore,ach,  that  produce,  a  loop  similar  to  the,  for/of  loop  as  a  highe,r-orde,r  function.

["a",  "b"].fore,ach(l  =>  console,.log(l));

//  →  a

//  →  b

Filte,ring  arrays

To  se,arch  for  the,  script  in  a  data  se,t,  use,  the,  following  function.  this  function  he,lps  to  filte,r  out  e,le,me,nt  that  faile,d  a  te,st  in  an  array.

Function  filte,r(array,  te,st)  {

Le,t  passe,d  =  [];

For  (le,t  e,le,me,nt  of  array)  {

If  (te,st(e,le,me,nt))  {

Passe,d.push(e,le,me,nt);

}

}

Re,turn  passe,d;

}

Console,.log(filte,r(scripts,  script  =>  script.living));

//  →  [{name,:  "adlam",  …},  …]

This  function  utilize,s  the,  argume,nt  calle,d  te,st,  a  function  value,,  to  cove,r  a  gap  during  the,  calculation.  it  de,te,rmine,s  which  e,le,me,nt  to  re,ce,ive,.

Transforming  with  map

The,  map  me,thod  change,s  an  array  by  se,tting  a  function  to  e,ach  and  e,ve,ry  of  its  e,le,me,nts  and  cre,ating  a  ne,w  array  from  the,  re,turne,d  value,s.  the,  ne,w  array  consists  of  the,  same,  le,ngth  with  the,  input  array  but  will  map  out  its  conte,nt  to  a  re,ne,we,d  for  by  the,  function.

Function  map(array,  transform)  {

Le,t  mappe,d  =  [];

For  (le,t  e,le,me,nt  of  array)  {

Mappe,d.push(transform(e,le,me,nt));

}

Re,turn  mappe,d;

}

Le,t  rtlscripts  =  scripts.filte,r(s  =>  s.dire,ction  ==  "rtl");

Console,.log(map(rtlscripts,  s  =>  s.name,));

//  →  ["adlam",  "arabic",  "impe,rial  aramaic",  …]

Like,  fore,ach  and  filte,r.

Summarizing  with  re,duce,

Whe,n  you  add  up  numbe,rs,  be,gin  with  ze,ro  and  add  the,  fore,ach  e,le,me,nt  to  the,  sum.  the,  parame,te,r  to  re,duce,  are,  map  function  combination  and  be,gin  a  value,.  this  function  is  much  e,asie,r  to  unde,rstand  than  the,  filte,r  and  map.  it  is  be,low:

Function  re,duce,(array,  combine,,  be,gin)  {

Le,t  curre,nt  =  be,gin;

For  (le,t  ite,ms  of  arrays)  {

E,xisting  =  combine,(e,xisting,  e,le,me,nt);

}

Re,turn  e,xisting;

}

Console,.log(re,duce,([0,1,  2,  3,  4],  (a,  b)  =>  a  +  b,  0));

//  →  10

This  function  is  similar  to  the,  standard  array  me,thod  re,duce,  and  attache,s  more,  comfort.

Console,.log([1,  2,  3,  4].re,duce,((a,  b)  =>  a  +  b));

//  →  10

If  you  want  to  utilize,  re,duce,  to  se,arch  for  the,  script  with  the,  more,  characte,rs,  write,  it  like,  this:

Function  characte,rcount(script)  {

Re,turn  script.range,s.re,duce,((count,  [from,  to])  =>  {

Re,turn  count  +  (to  -  from);

},  0);

}

Console,.log(scripts.re,duce,((a,  b)  =>  {

Re,turn  characte,rcount(a)  <  characte,rcount(b)?  b:  a;

}));

//  →  {name,:  "han",  …}

Composability

Take,  some,  time,  to  think  about  how  long  our  list  of  code,  would  have,  be,e,n  without  the,  highe,r-orde,r  functions.

Le,t  bigge,st  =  null;

For  (le,t  script  of  scripts)  {

If  (bigge,st  ==  null  ||

Characte,rcount(bigge,st)  <  characte,rcount(script))  {

Bigge,st  =  script;

}

}

Console,.log(bigge,st);

//  →  {name,:  "han",  …}

You  can  use,  the,  high-orde,r  functions  whe,n  you  want  to  compose,  ope,rations.  for  instance,,  he,re,  is  a  line,  of  code,  that  se,arche,s  for  the,  ave,rage,  ye,ar  for  living  and  de,ad  in  humans’  scripts  in  the,  data  se,t.

Function  ave,rage,(array)  {

Re,turn  array.re,duce,((a,  b)  =>  a  +  b)  /  array.le,ngth;

}

Console,.log(math.round(ave,rage,(

Scripts.filte,r(s  =>  s.living).map(s  =>  s.ye,ar))));

//  →  1165

Console,.log(math.round(ave,rage,(

Scripts.filte,r(s  =>  !S.living).map(s  =>  s.ye,ar))));

//  →  204

The,  block  of  code,  displays  that  the,  de,ath  script  is  olde,r  than  the,  living  one,s.

Le,t’s  be,gin  with  the,  e,ntire,  script,  filte,r  out  the,  de,ad  (or  living),  e,radicate,  the,ir  ye,ars,  ave,rage,  the,m  and  comple,te,  the,  re,sult.  you  can  as  we,ll  write,  the,se,  calculations  as  a  big  loop:

Le,t  total  =  0,  count  =  0;

For  (le,t  script  of  scripts)  {

If  (script.living)  {

Total  +=  script.ye,ar;

Count  +=  1;

}

}

Console,.log(math.round(total  /  count));

//  →  1165

Our  two  e,xample,s  are,  not  ide,ntical,  the,  first  cre,ate,s  ne,w  arrays  whe,n  administe,ring  the,  map  and  filte,r  while,  the,  se,cond  calculate,  numbe,rs  only.

Strings  and  characte,r  code,s

One,  of  the,  significant  use,  of  data  se,t  is  to  find  out  what  script  a  block  of  te,xt  is  using.  be,low  is  a  program  that  pe,rforms  that  task.

E,ve,ry  script  contains  an  array  of  characte,r  code,  range,s  re,late,d  with  it.  so,  if  you  are,  give,n  a  characte,r  code,,  utilize,  this  function  to  se,arch  for  the,  e,quivale,nt  script  (if  available,):

Function  characte,rscript(code,)  {

For  (le,t  script  of  scripts)  {

If  (script.range,s.some,(([from,  to])  =>  {

Re,turn  code,  >=  from  &&  code,  <  to;

}))  {

Re,turn  script;

}

}

Re,turn  null;

}

Console,.log(characte,rscript(121));

//  →  {name,:  "latin",  …}

Anothe,r  high-orde,r  function  is  the,  same,  me,thod.  this  me,thod  ge,ts  a  te,st  function  and  de,te,rmine,  if  that  function  se,nds  back  true,  for  any  compone,nt  in  the,  array.

The,re,  are,  some,  ope,rations  on  javascript  strings  like,  se,curing  the,ir  le,ngth  using  the,  le,ngth  prope,rty  and  e,valuating  the,ir  conte,nts  through  the,  square,  bracke,ts.

//  two  e,moji  characte,rs,  horse,  and  shoe,

Le,t  horse,shoe,  =  "🐴👟";

Console,.log(horse,shoe,.le,ngth);

//  →  4

Console,.log(horse,shoe,[0]);

//  →  (invalid  half-characte,r)

Console,.log(horse,shoe,.charcode,at(0));

//  →  55357  (code,  of  the,  half-characte,r)

Console,.log(horse,shoe,.code,pointat(0));

//  →  128052  (actual  code,  for  horse,  e,moji)

Javascript’s  charcode,at  me,thod  offe,rs  a  full  unicode,  characte,r.  this  me,thod  is  use,d  to  take,  characte,rs  from  a  string.  although  the,  argume,nt  se,nt  to  code,pointat  re,mains  an  inde,x  into  the,  succe,ssion  of  code,  units.  if  you  use,  the,  code,pointat  to  loop  across  a  string,  it  produce,s  re,al  characte,rs  and  not  code,  units.

Le,t  rose,dragon  =  "🌹🐉";

For  (le,t  char  of  rose,dragon)  {

Console,.log(char);

}

//  →  🌹

//  →  🐉

Re,cognizing  te,xt

You  have,  the,  characte,r  script  function  and  a  way  to  loop  across  characte,rs  corre,ctly,  now  calculate,  the,  characte,rs  e,ach  script  owns.  the,  be,low  counting  abstraction  is  use,d  he,re,:

Function  countby(ite,ms,  groupname,)  {

Le,t  counts  =  [];

For  (le,t  ite,m  of  ite,ms)  {

Le,t  name,  =  groupname,(ite,m);

Le,t  known  =  counts.findinde,x(c  =>  c.numbe,r  ==  name,);

If  (known  ==  -1)  {

Counts.push({nunbe,r,  count:  0});

}  e,lse,  {

Counts[know].count++;

}

}

Re,turn  counts;

}

Console,.log(countby([0,1,  2,  3,  4,  5],  n  =>  n  >  2));

//  →  [{numbe,r:  false,,  count:  2},  {numbe,r:  true,,  count:  3}]

The,  countby  function  anticipate,s  a  colle,ction  (a  group  of  numbe,rs,  e,le,me,nt  or  anything  that  you  can  loop  ove,r  with  for/of)  and  a  function  that  calculate,s  a  group  name,  for  a  spe,cifie,d  e,le,me,nt.  it  se,nds  back  a  list  of  obje,cts.  e,ach  of  the,  obje,cts  name,s  a  group  and  de,te,rmine,s  the,  numbe,r  of  e,le,me,nts  containe,d  in  the,  group.

The,  me,thod  findinde,x  is  similar  to  inde,xof.  this  me,thod  is  use,d  to  se,arch  for  the,  first  value,  for  which  the,  state,d  function  se,nds  back  true,  and  re,turns  -1  whe,n  ze,ro  e,le,me,nts  is  found.  you  can  use,  the,  countby  to  de,te,rmine,  which  script  is  utilize,d  in  a  block  of  te,xt.

Function  te,xtscripts(te,xt)  {

Le,t  scripts  =  countby(te,xt,  char  =>  {

Le,t  script  =  characte,rscript(char.code,pointat(0));

Re,turn  script?  script.name,  :  "none,";

}).filte,r(({name,})  =>  name,  !=  "none,");

Le,t  total  =  scripts.re,duce,((n,  {count})  =>  n  +  count,  0);

If  (total  ==  0)  re,turn  "no  scripts  found";

Re,turn  scripts.map(({name,,  count})  =>  {

Re,turn  `${math.round(count  *  100  /  total)}%  ${name,}`;

}).join(",  ");

}

Console,.log(te,xtscripts('英国的狗说"woof",  俄罗斯的狗说"тяв"'));

//  →  61%  han,  22%  latin,  17%  cyrillic

The,  function  calculate,s  the,  characte,rs  by  name,  through  the,  use,  of  characte,rscript  to  attach  a  name,  and  re,turning  back  to  the,  string  "none,"  for  characte,rs  without  any  script.  if  you  want  to  calculate,  pe,rce,ntage,s,  you  ne,e,d  to  de,te,rmine,  the,  total  amount  of  characte,rs  be,longing  to  a  script  that  the,  re,duce,  me,thod  can  re,duce,.  if  it  finds  ze,ro  characte,rs,  the,  function  se,nds  back  the,  "none,"  string.

Summary

Having  the,  ability  to  se,nd  function  value,s  to  se,ve,ral  functions  is  an  e,sse,ntial  aspe,ct  of  javascript.  it  e,nable,s  writing  functions  that  imitate,  computations  with  “gaps”  be,twe,e,n  the,m.  the,  code,  that  de,clare,s  the,se,  functions  can  contain  the,  gaps  by  giving  function  value,s.  arrays  provide,  se,ve,ral  important  highe,r-orde,r  me,thods.  use,  fore,ach  to  loop  across  e,le,me,nts  within  an  array.  use,  the,  filte,r  me,thod  to  se,nd  back  a  ne,w  array  that  has  e,le,me,nts  that  conve,y  the,  pre,dicate,  function.  changing  an  array  by  se,tting  e,ach  ite,m  through  a  function  using  the,  map.  use,  re,duce,  to  me,rge,  e,ve,ry  compone,nt  of  an  array  to  an  individual  value,.

E,xe,rcise,s

Illustrate,  a  javascript  function  that  take,s  an  array  of  numbe,rs  save,d  and  se,arch  for  the,  se,cond-lowe,st  and  se,cond  highe,st  numbe,rs.

Solution

![00160.jpg](images/00160.jpeg)![00139.jpg](images/00139.jpeg)

## Chapte,r  7:  the,  se,cre,t  life, of  obje,cts

Whe,n  it  come,s  to  programing  language,s,  the,re,  is  a  se,t  te,chnique,  that  utilize,s  obje,cts  as  a  fundame,ntal  ide,a  of  program  organization,  and  the,y  are,  calle,d  the,  obje,ct-orie,nte,d  programming.  its  conce,pt  will  be,  e,xplaine,d  furthe,r  in  this  chapte,r.

E,ncapsulation

The,  primary  importance,  of  obje,ct-orie,nte,d  programming  is  to  bre,ak  programs  into  little,  pie,ce,s  and  make,s  sure,  e,ach  pie,ce,  manage,s  its  se,ction.  se,ve,ral  fragme,nts  of  similar  programs  communicate,  with  e,ach  othe,r  using  inte,rface,s,  a  re,stricte,d  se,t  of  functions  or  binding  that  produce,  e,sse,ntial  functionality  on  a  highe,r  le,ve,l,  hiding  the,  spe,cific  e,xe,cution.  illustrate,  this  type,  of  program  pie,ce,s  through  obje,cts,  and  the,ir  layout  contains  a  particular  se,t  of  prope,rtie,s  and  me,thods.  prope,rtie,s  within  the,  layout  are,  public  while,  the,  oute,r  code,  is  private,.  de,fine,  the,  acce,ssible,  layout  in  comme,nts  or  docume,ntation.  it  re,gularly  use,s  the,  unde,rscore,  (_)  characte,r  at  the,  be,ginning  of  prope,rty  name,s  to  signify  private,  prope,rtie,s.  me,anwhile,,  diving  layouts  from  e,xe,cution  is  calle,d  e,ncapsulation.

Me,thods

Me,thods  are,  prope,rtie,s  that  grasp  function  value,s.

Le,t  rabbit  =  {};

Rabbit.spe,ak  =  function(line,)  {

Console,.log(`the,  rabbit  says  '${line,}'`);

};

Rabbit.spe,ak("i'm  alive,.");

//  →  the,  rabbit  says  'i'm  alive,.'

Whe,n  you  call  a  function  as  a  me,thod,  the,  binding  calls  it  in  its  body  and  dire,ct  the,  obje,ct  it  was  calle,d  on.

Function  spe,ak(line,)  {

Console,.log(`the,  ${this.type,}  rabbit  says  '${line,}'`);

}

Le,t  white,rabbit  =  {type,:  "white,",  spe,ak};

Le,t  hungryrabbit  =  {type,:  "hungry",  spe,ak};

White,rabbit.spe,ak("oh  my  whiske,rs,"  +  "how  late,  it's  ge,tting!");

//  →  the,  white,  rabbit  says  'oh  my  whiske,rs,  how

//  late,  it's  ge,tting!'

Hungryrabbit.spe,ak("i  could  use,  a  carrot  right  now.");

//  →  the,  hungry  rabbit  says  'i  could  use,  a  carrot  right  now.'

Arrow  functions  are,  do  not  bind  the,ir  own.  you  can  write,  the,  following  code,:

Function  normal()  {

Console,.log(this.coords.map(n  =>  n  /  this.le,ngth));

}

Normal.call({coords:  [0,  2,  3],  le,ngth:  5});

//  →  [0,  0.4,  0.6]

Prototype,s

Ke,e,p  an  e,ye,  out  on  this.

Le,t  e,mpty  =  {};

Console,.log(e,mpty.tostring);

//  →  function  tostring()…{}

Console,.log(e,mpty.tostring());

//  →  [obje,ct  obje,ct]

A  prope,rty  is  pulle,d  out  of  an  e,mpty  obje,ct.  a  lot  of  javascript  obje,cts  consists  of  a  prototype,.  this  is  an  obje,ct  use,d  as  an  alte,rnative,  source,  of  prope,rtie,s.  the,re,fore,,  the,  prototype,  of  that  e,mpty  obje,ct  is  the,  inhe,rite,d  prototype,,  the,  obje,ct.prototype,.

Console,.log(obje,ct.ge,tprototype,of({})  ==

Obje,ct.prototype,);

//  →  true,

Console,.log(obje,ct.ge,tprototype,of(obje,ct.prototype,));

//  →  null

Obje,ct.ge,tprototype,of  se,nds  back  the,  prototype,  of  an  obje,ct.  this  prototype,  produce,s  some,  me,thod  that  displays  in  e,ve,ry  obje,ct  like,  tostring  that  transforms  an  obje,ct  to  a  string  e,xe,cution.

A  lot  of  obje,cts  do  not  contain  obje,ct.prototype,  as  the,ir  prototype,  but  use,  anothe,r  obje,ct  that  produce,s  a  se,parate,  se,t  of  de,fault  prope,rtie,s;

Functions  acquire,s  from  function.prototype,,  and  arrays  acquire,s  from  array

.prototype,.

Console,.log(obje,ct.ge,tprototype,of(math.max)  ==

Function.prototype,);

//  →  true,

Console,.log(obje,ct.ge,tprototype,of([])  ==

Array.prototype,);

//  →  true,

This  type,  of  prototype,  obje,ct  contains  a  prototype,,  the,  obje,ct.prototype,,  so  that  it  can  cre,ate,  me,thods  such  as  tostring  indire,ctly.  use,  the,  obje,ct.cre,ate,  to  build  an  obje,ct  with  a  particular  prototype,.

Le,t  protorabbit  =  {

Spe,ak(line,)  {

Console,.log(`the,  ${this.type,}  rabbit  says  '${line,}'`);

}

};

Le,t  kille,rrabbit  =  obje,ct.cre,ate,(protorabbit);

Kille,rrabbit.type,  =  "kille,r";

Kille,rrabbit.spe,ak("skre,e,e,e,!");

//  →  the,  kille,r  rabbit  says  'skre,e,e,e,!

The,y  spe,ak(line,)  prope,rty  in  an  obje,ct  e,xpre,ssion  produce,s  a  prope,rty  calle,d  spe,ak  and  se,t  a  function  as  its  value,.  it  is  a  shorthand  way  of  de,scribing  a  me,thod.

The,  “proto”  rabbit  is  a  containe,r  for  all  prope,rtie,s.

Classe,s

Javascript’s  prototype,  syste,m  can  be,  de,scribe,d  as  subsidiary  on  an  obje,ct-orie,nte,d  me,thod  calle,d  classe,s.  a  class  de,scribe,s  an  obje,ct  type,'s  shape,,  its  prope,rtie,s  and  me,thods.  prototype,s  are,  use,d  to  de,scribe,  prope,rtie,s  whe,re,by  e,ve,ry  instance,  share,  similar  value,s  such  as  me,thods.  if  you  want  to  build  an  instance,  of  a  se,t  class,  cre,ate,  an  obje,ct  that  re,ce,ive,s  from  the,  normal  prototype,.  make,  sure,  it  contains  prope,rtie,s  that  should  be,  include,d  in  the,  instance,  of  this  class.  be,low  is  the,  constructor  function.

Function  make,rabbit(type,)  {

Le,t  rabbit  =  obje,ct.cre,ate,(protorabbit);

Rabbit.type,  =  type,;

Re,turn  rabbit;

}

Javascript  offe,rs  a  way  to  make,  de,scribing  this  function  e,ffortle,ssly.  se,t  the,  ke,yword  at  the,  front  of  a  function  call.  the,  prototype,  obje,ct  utilize,d  during  the,  construction  of  obje,cts  is  attaine,d  by  fe,tching  the,  prototype,  prope,rty  of  the,  constructor  function.

Function  rabbit(type,)  {

This.type,  =  type,;

}

Rabbit.prototype,.spe,ak  =  function(line,)  {

Console,.log(`the,  ${this.type,}  rabbit  says  '${line,}'`);

};

Le,t  we,irdrabbit  =  ne,w  rabbit("we,ird");

Function.prototype,  is  the,  prototype,  of  a  constructor.  its  prototype,  prope,rty  grasps  the,  prototype,  utilize,d  for  instance,s  built  through  it.

Console,.log(obje,ct.ge,tprototype,of(rabbit)  ==

Function.prototype,);

//  →  true,

Console,.log(obje,ct.ge,tprototype,of(we,irdrabbit)  ==

Rabbit.prototype,);

//  →  true,

Class  notation

Javascript  classe,s  are,  constructor  functions  with  a  prototype,  prope,rty.  be,low  is  a  sample,:

Class  rabbit  {

Constructor(type,)  {

This.type,  =  type,;

}

Spe,ak(line,)  {

Console,.log(`the,  ${this.type,}  rabbit  says  '${line,}'`);

}

}

Le,t  kille,rrabbit  =  ne,w  rabbit("kille,r");

Le,t  blackrabbit  =  ne,w  rabbit("black");

The,  class  ke,yword  be,gins  with  a  class  de,claration,  which  e,nable,s  you  to  de,scribe,  a  constructor  and  a  se,t  of  me,thods  in  a  particular  place,.  class  de,clarations  e,nable,s  me,thods,  prope,rtie,s  that  grasp  functions  to  be,  include,d  in  the,  prototype,.  whe,n  you  use,  an  e,xpre,ssion,  it  doe,s  not  de,scribe,  a  binding  bur  provide,s  the,  constructor  as  a  value,.  you  can  e,xclude,  the,  class  name,  in  an  e,xpre,ssion.

Le,t  obje,ct  =  ne,w  class  {ge,tword()  {  re,turn  "he,llo";  }  };

Console,.log(obje,ct.ge,tword());

//  →  he,llo

Ove,rriding  de,rive,d  prope,rtie,s

Whe,n  a  prope,rty  is  adde,d  to  an  obje,ct,  e,ithe,r  available,  in  the,  prototype,  or  not,  the,  prope,rty  adds  to  the,  obje,ct.  if  the,re,  was  an  assigne,d  prope,rty  with  similar  name,s  in  the,  prototype,,  it  doe,s  not  influe,nce,  the,  obje,ct.

Rabbit.prototype,.te,e,th  =  "small";

Console,.log(kille,rrabbit.te,e,th);

//  →  small

Kille,rrabbit.te,e,th  =  "long,  sharp,  and  bloody";

Console,.log(kille,rrabbit.te,e,th);

//  →  long,  sharp,  and  bloody

Console,.log(blackrabbit.te,e,th);

//  →  small

Console,.log(rabbit.prototype,.te,e,th);

//  →  small

Ove,rriding  prope,rtie,s  is  use,d  to  be,stow  a  standard  function  and  array  prototype,s  a  se,parate,  tostring  me,thod.

Console,.log(array.prototype,.tostring  ==

Obje,ct.prototype,.tostring);

//  →  false,

Console,.log([1,  3].tostring());

//  →  1,3

Calling  tostring  on  an  array  be,stows  a  re,sult  that  is  like,ne,d  to  calling.  join(",")  on  it.  it  place,s  a  comma  be,twe,e,n  the,  value,s  containe,d  in  the,  array.  if  you  call  obje,ct.prototype,.tostring  to  an  array,  it  provide,s  a  se,parate,  string.

Console,.log(obje,ct.prototype,.tostring.call([1,  3]));

//  →  [obje,ct  array]

Maps

A  map  is  a  data  layout  that  conne,ct  value,s  with  othe,r  value,s.  if  you  want  to  map  name,s  to  age,s,  write,  your  code,  like,  this:

Le,t  age,s  =  {

Boris:  39,

Liang:  22,

Júlia:  62

};

Console,.log(`julia  is  ${age,s["julia"]}`);

//  →  julia  is  62

Console,.log("is  jack's  age,  known?",  "jack"  in  age,s);

//  →  is  jack's  age,  known?  false,

Console,.log("is  tostring's  age,  known?",  "tostring"  in  age,s);

//  →  is  tostring's  age,  known?  true,

Obje,ct  prope,rty  name,s  should  be,  in  strings.  if  you  want  a  map  that  the,  ke,ys  cannot  be,  transforme,d  to  strings,  do  not  use,  obje,ct  as  a  map.  javascript  contains  a  class  calle,d  map.  it  save,s  mapping  and  e,nable,s  diffe,re,nt  type,s  of  ke,ys.

Le,t  age,s  =  ne,w  map();

Age,s.se,t("boris",  39);

Age,s.se,t("liang",  22);

Age,s.se,t("júlia",  62);

Console,.log(`júlia  is  ${age,s.ge,t("júlia")}`);

//  →  júlia  is  62

Console,.log("is  jack's  age,  known?",  age,s.has("jack"));

//  →  is  jack's  age,  known?  false,

Console,.log(age,s.has("tostring"));

//  →  false,

The,  me,thods  ge,t,  se,t,  and  has  are,  bodie,s  of  the,  layout  of  the,  map  obje,ct.  the,  obje,ct.ke,ys  se,nds  back  an  obje,ct’s  own  ke,ys  only.  you  can  use,  the,  hasownprope,rty  me,thod  as  an  option.

Console,.log({x:  1}.hasownprope,rty("x"));

//  →  true,

Console,.log({x:  1}.hasownprope,rty("tostring"));

//  →  false,

Polymorphism

Whe,n  a  string  function  is  calle,d  on  an  obje,ct,  the,  tostring  me,thod  is  calle,d  on  that  obje,ct  in  orde,r  to  build  a  significant  string  from  it.  you  can  de,fine,  your  own  ve,rsion  of  tostring  so  that  the,y  can  build  a  string  that  consists  of  more,  important  data  more,  than  the,  "[obje,ct  obje,ct]".  be,low  is  an  illustration:

Rabbit.prototype,.tostring  =  function()  {

Re,turn  `a  ${this.type,}  rabbit`;

};

Console,.log(string(blackrabbit));

//  →  a  black  rabbit

Whe,n  a  line,  of  code,  is  writte,n  to  function  with  obje,cts  that  have,  a  spe,cific  layout  is  calle,d  polymorphism.  polymorphic  code,  can  function  prope,rly  with  value,s  of  se,ve,ral  shape,s.

Symbols

Symbols  are,  unique,  value,s  built  with  the,  symbol  function  which  cannot  be,  built  twice,.

Le,t  sym  =  symbol("name,");

Console,.log(sym  ==  symbol("name,"));

//  →  false,

Rabbit.prototype,[sym]  =  55;

Console,.log(blackrabbit[sym]);

//  →  55

The,  string  passe,d  to  the,  symbol  is  attache,d  whe,n  you  transform  it  to  a  string.  the,y  are,  distinctive,  and  functions  as  prope,rty  name,s.

Const  tostringsymbol  =  symbol("tostring");

Array.prototype,[tostringsymbol]  =  function()  {

Re,turn  `${this.le,ngth}  cm  of  blue,  yarn`;

};

Console,.log([1,  2].tostring());

//  →  1,2

Console,.log([1,  2][tostringsymbol]());

//  →  2  cm  of  blue,  yarn

You  can  attach  the,  symbol  prope,rtie,s  in  obje,ct  classe,s  and  e,xpre,ssions  through  the,  use,  of  square,  bracke,ts  surrounding  the,  prope,rty  name,.  be,low  we,  re,fe,r  to  a  binding  storing  the,  symbol.

Le,t  stringobje,ct  =  {

[tostringsymbol]()  {  re,turn  "a  jute,  rope,";  }

};

Console,.log(stringobje,ct[tostringsymbol]());

//  →  a  jute,  rope,s

The,  ite,rator  inte,rface,s

The,  state,d  obje,ct  to  a  for/of  loop  is  ite,rable,.  this  me,ans  that  it  consists  of  a  name,d  me,thod  with  the,  symbol.ite,rator  symbol  whe,n  the,  prope,rty  is  calle,d.  the,  me,thod  se,nds  back  an  obje,ct  that  produce,s  a  se,cond  layout.  it  contains  a  ne,xt  me,thod  that  se,nds  back  the,  following  re,sult.  the,  re,sult  is  an  obje,ct  with  a  value,  prope,rty  that  produce,s  the,  ne,xt  value,,  symbol.ite,rator  can  be,  adde,d  to  se,ve,ral  obje,cts.  che,ckout  this  layout:

Le,t  okite,rator  =  "ok"[symbol.ite,rator]();

Console,.log(okite,rator.ne,xt());

//  →  {value,:  "o",  done,:  false,}

Console,.log(okite,rator.ne,xt());

//  →  {value,:  "k",  done,:  false,}

Console,.log(okite,rator.ne,xt());

//  →  {value,:  unde,fine,d,  done,:  true,}

Le,t’s  imple,me,nt  an  ite,rable,  data  structure,.  we,’ll  build  a  matrix  class,  acting

As  a  two-dime,nsional  array  class  matrix  {

Constructor(width,  he,ight,  e,le,me,nt  =  (x,  y)  =>  unde,fine,d)  {

This.width  =  width;

This.he,ight  =  he,ight;

This.conte,nt  =  [];

For  (le,t  y  =  0;  y  <  he,ight;  y++)  {

For  (le,t  x  =  0;  x  <  width;  x++)  {

This.conte,nt[y  *  width  +  x]  =  e,le,me,nt(x,  y);

}

}

}

Ge,t(x,  y)  {

Re,turn  this.conte,nt[y  *  this.width  +  x];

}

Se,t(x,  y,  value,)  {

This.conte,nt[y  *  this.width  +  x]  =  value,;

}

}

The,  conte,nt  of  the,  class  is  save,d  in  an  individual  array  of  width  ×  he,ight  e,le,me,nts.  the,se,  e,le,me,nts  are,  save,d  row  afte,r  row.  the,  constructor  function  ge,ts  a  width,  he,ight,  and  an  additional  e,le,me,nt  function,  which  is  use,d  to  se,t  the,  initial  value,s.  use,  the,  ge,t  me,thod  and  se,t  me,thod  to  re,cove,r  and  update,  e,le,me,nts  within  the,  matrix.  be,low  is  the,  layout  of  obje,cts  with  x,  y,  and  value,  prope,rtie,s.

Class  matrixite,rator  {

Constructor(matrix)  {

This.x  =  0;

This.y  =  0;

This.matrix  =  matrix;

}

Ne,xt()  {

If  (this.y  ==  this.matrix.he,ight)  re,turn  {done,:  true,};

Le,t  value,  =  {x:  this.x,

Y:  this.y,

Value,:  this.matrix.ge,t(this.x,  this.y)};

This.x++;

If  (this.x  ==  this.matrix.width)  {

This.x  =  0;

This.y++;

}

Re,turn  {value,,  done,:  false,};

}

}

Be,low  is  an  illustration  of  an  ite,rable,  matrix  class:

Matrix.prototype,[symbol.ite,rator]  =  function()  {

Re,turn  ne,w  matrixite,rator(this);

};

We,  can  now  loop  ove,r  a  matrix  with  for/of.

Le,t  matrix  =  ne,w  matrix(2,  2,  (x,  y)  =>  `value,  ${x},${y}`);

For  (le,t  {x,  y,  value,}  of  matrix)  {

Console,.log(x,  y,  value,);

}

//  →  0  0  value,  0,0

//  →  1  0  value,  1,0

//  →  0  1  value,  0,1

//  →  1  1  value,  1,1

Statics,  ge,tte,rs,  and  se,tte,rs

Layouts  consists  of  me,thods,  but  you  can  also  attach  prope,rtie,s  that  store,s  value,s  with  no  function  like,  a  map  obje,ct  containing  a  size,  prope,rty  that  de,te,rmine,s  how  many  ke,ys  are,  save,d  in  the,m.  an  asse,sse,d  prope,rty  can  hide,  a  me,thod  call.  those,  me,thods  are,  calle,d  ge,tte,rs,  and  you  can  de,scribe,  the,m  by  writing  "ge,t"  at  the,  be,ginning  of  the,  me,thod  name,  in  a  class  de,claration  or  an  obje,ct  e,xpre,ssion.

Le,t  varyingsize,  =  {

Ge,t  size,()  {

Re,turn  math.floor(math.random()  *  100);

}

};

Console,.log(varyingsize,.size,);

//  →  73

Console,.log(varyingsize,.size,);

//  →  49

Whe,n  you  want  to  use,  an  obje,ct’s  size,  prope,rty,  you  call  the,  associate,d  me,thod.  you  can  pe,rform  a  similar  task  whe,n  you  a  prope,rty  using  a  se,tte,r.

Class  te,mpe,rature,  {

Constructor(ce,lsius)  {

This.ce,lsius  =  ce,lsius;

}

Ge,t  fahre,nhe,it()  {

Re,turn  this.ce,lsius  *  1.8  +  32;

}

Se,t  fahre,nhe,it(value,)  {

This.ce,lsius  =  (value,  -  32)  /  1.8;

}

Static  fromfahre,nhe,it(value,)  {

Re,turn  ne,w  te,mpe,rature,((value,  -  32)  /  1.8);

}

}

Le,t  te,mp  =  ne,w  te,mpe,rature,(22);

Console,.log(te,mp.fahre,nhe,it);

//  →  71.6

Te,mp.fahre,nhe,it  =  86;

Console,.log(te,mp.ce,lsius);

//  →  30

The,  te,mpe,rature,  class  e,nable,  you  to  re,ad  and  write,  the,  te,mpe,rature,  in  de,gre,e,s  ce,lsius  or  de,gre,e,s  fahre,nhe,it,  but  it  save,s  only  ce,lsius  and  transform  to  and  from  ce,lsius  in  the,  fahre,nhe,it  ge,tte,r  and  se,tte,r.  within  a  class  de,claration,  me,thods  that  are,  static  writte,n  be,fore,  the,ir  name,s  are,  save,d  on  the,  constructor.  so,  you  can  write,  te,mpe,rature,.fromfahre,nhe,it(100)  to  build  a  te,mpe,rature,  through  de,gre,e,s  fahre,nhe,it.

Inhe,ritance,

Some,  matrice,s  are,  symme,tric.  whe,n  you  re,fle,ct  a  symme,tric  matrix  through  its  top-le,ft-to-bottom-right  diagonal,  it  doe,s  not  change,.  the,  value,  se,t  at  x,y  re,mains  the,  same,  as  the,  y,x.  use,  the,  javascript’s  prototype,  syste,m  to  build  a  ne,w  class,  the,  prototype,  for  the,  ne,w  class  is  acquire,d  from  the,  old  prototype,  but  se,ts  a  ne,w  de,finition  for  the,  me,thod.  this  is  calle,d  inhe,ritance,  in  obje,ct-orie,nte,d  programming  te,rms.  be,low  is  an  illustration:

Class  symme,tricmatrix  e,xte,nds  matrix  {

Constructor(size,,  e,le,me,nt  =  (x,  y)  =>  unde,fine,d)  {

Supe,r(size,,  size,,  (x,  y)  =>  {

If  (x  <  y)  re,turn  e,le,me,nt(y,  x);

E,lse,  re,turn  e,le,me,nt(x,  y);

});

}

Se,t(x,  y,  value,)  {

Supe,r.se,t(x,  y,  value,);

If  (x  !=  y)  {

Supe,r.se,t(y,  x,  value,);

}

}

}

Le,t  matrix  =  ne,w  symme,tricmatrix(5,  (x,  y)  =>  `${x},${y}`);

Console,.log(matrix.ge,t(2,  3));

//  →  3,2

The,  instance,of  ope,rator

It  is  important  to  know  if  an  obje,ct  was  gotte,n  from  a  particular  instance,of.

Console,.log(

Ne,w  symme,tricmatrix(2)  instance,of  symme,tricmatrix);

//  →  true,

Console,.log(ne,w  symme,tricmatrix(2)  instance,of  matrix);

//  →  true,

Console,.log(ne,w  matrix(2,  2)  instance,of  symme,tricmatrix);

//  →  false,

Console,.log([1]  instance,of  array);

//  →  true,

The,  ope,rator  will  scan  through  the,  type,s  that  we,re,  inhe,rite,d.  the,re,fore,,  a  symme,tricmatrix  is  an  instance,  of  matrix.  you  can  also  apply  this  me,thod  to  standard  constructors  like,  array.

Summary

In  this  chapte,r,  we,  re,alize,  that  obje,cts  can  pe,rform  more,  than  holding  the,ir  prope,rtie,s.  the,y  consist  of  prototype,s  that  are,  obje,cts  as  we,ll.  the,y  be,have,  like,  the,y  contain  prope,rtie,s  that  the,y  do  not  provide,  as  long  as  the,  prototype,  has  that  prope,rty.  simple,  obje,cts  use,  the,  obje,ct.  prototype,  to  re,pre,se,nt  the,ir  prototype,.  we,  talke,d  about  constructors  too,  and  the,y  are,  functions  that  the,ir  name,s  ofte,n  be,gin  with  a  capital  le,tte,r,  and  use,d  with  the,  ne,w  ope,rator  to  build  ne,w  obje,cts.  the,  ne,w  obje,ct’s  prototype,  would  be,  the,  obje,ct  within  the,  prototype,  prope,rty  of  the,  constructor.  a  class  notation  offe,rs  a  way  to  de,scribe,  a  constructor  and  its  prototype,.  we,  also  touche,d  the,  ge,tte,rs,  se,tte,rs,  and  statics  and  the,  instance,of  ope,rator.

E,xe,rcise,

Write,  a  javascript  program  to  cre,ate,  an  array,  through  an  ite,rator  function  and  a  primary  se,e,d  value,.

Solution

![00194.jpg](images/00194.jpeg)

## Chapte,r  8:  a  robot

In  this  chapte,r,  the,re,  will  be,  work  on  a  robot  program,  a  short  program  that  e,xe,cute,s  a  task  in  a  virtual  world.  we,  will  be,  using  a  mail  de,live,ry  robot  re,ce,iving  and  de,live,ring  parce,ls.

Me,adow  fie,ld

The,  me,adow  fie,ld  village,  is  a  small  one,  consisting  of  14  roads  and  11  place,s.  be,low  is  an  illustration  with  an  array  of  roads:

Const  roads  =  [

"alice,'s  house,-bob's  house,",  "alice,'s  house,-cabin",

"alice,'s  house,-post  office,",  "bob's  house,-town  hall",

"daria's  house,-e,rnie,'s  house,",  "daria's  house,-town  hall",

"e,rnie,'s  house,-gre,te,'s  house,",  "gre,te,'s  house,-farm",

"gre,te,'s  house,-shop",  "marke,tplace,-farm",

"marke,tplace,-post  office,",  "marke,tplace,-shop",

"marke,tplace,-town  hall",  "shop-town  hall"

]

The,  village,  roads  cre,ate,  a  graph.  a  graph  is  a  group  of  points  (village,  place,s)  with  line,s  dividing  the,m  (roads).  the,  graph  is  the,  world  whe,re,  our  robot  walks  through.  now  le,t  us  transform  our  list  to  a  data  layout  that  e,ach  place,  de,cide,s  whe,re,  you  can.

Function  buildgraph(borde,r)  {

Le,t  graph  =  obje,ct.cre,ate,(null);

Function  addborde,rs(from,  to)  {

If  (graph[from]  ==  null)  {

Graph[from]  =  [to];

}  e,lse,  {

Graph[from].push(to);

}

}

For  (le,t  [from,  to]  of  borde,rs.map(r  =>  r.split("-")))  {

Adde,dge,(from,  to);

Adde,dge,(to,  from);

}

Re,turn  graph;

}

Const  roadgraph  =  buildgraph(roads);

Give,n  an  array  of  e,dge,s,  buildgraph  cre,ate,s  a  map  obje,ct  that,  for  e,ach  node,,  save,s  a  conne,cte,d  node,  of  an  array.  it  utilize,s  the,  split  me,thod  to  go  through  the,  road  strings,  that  contains  the,  form  "start-e,nd",  to  two-e,le,me,nt  arrays  within  the,  start  and  e,nd  as  diffe,re,nt  strings.

The,  task

Our  robot  will  walk  across  the,  village,.  the,re,  are,  diffe,re,nt  parce,ls  in  se,ve,ral  place,s.  the,  robot  re,ce,ive,s  a  parce,l  whe,n  it  arrive,s  and  de,live,rs  the,m  whe,n  it  ge,ts  to  the,ir  de,stination.  whe,n  all  tasks  have,  all  be,e,n  e,xe,cute,d,  all  parce,ls  must  be,  de,live,re,d.  if  you  want  to  re,plicate,  this  proce,ss,  de,scribe,  a  virtual  world  that  can  de,fine,  it.  this  me,thod  re,ve,als  the,  robot  location  as  we,ll  as  the,  parce,ls.  le,t  us  bring  down  the,  village,'s  state,  to  a  spe,cific  se,t  of  value,s  that  de,scribe,s  it.

Class  village,state,  {

Constructor(place,,  parce,ls)  {

This.place,  =  place,;

This.parce,ls  =  parce,ls;

}

Move,(de,stination)  {

If  (!Roadgraph[this.place,].include,s(de,stination))  {

Re,turn  this;

}  e,lse,  {

Le,t  parce,ls  =  this.parce,ls.map(p  =>  {

If  (p.place,  !=  this.place,)  re,turn  p;

Re,turn  {place,:  de,stination,  addre,ss:  p.addre,ss};

}).filte,r(p  =>  p.place,  !=  p.addre,ss);

Re,turn  ne,w  village,state,(de,stination,  parce,ls);

}

}

}

The,  move,  me,thod  is  the,  action  ce,nte,r.  it  e,xamine,s  if  a  path  le,ads  from  one,  place,  to  anothe,r,  if  not  the,  old  state,  is  re,turne,d  be,cause,  the,  move,  is  not  valid.  the,n  it  builds  a  ne,w  state,  with  the,  de,stination  as  the,  robot’s  ne,w  place,  as  we,ll  as  building  a  ne,w  se,t  of  parce,ls.  the,  call  to  map  handle,s  the,  move,me,nt  and  the,  call  to  filte,r  handle,s  de,live,ring.

Le,t  first  =  ne,w  village,state,(

"post  office,",

[{place,:  "post  office,",  addre,ss:  "alice,'s  house,"}]

);

Le,t  ne,xt  =  first.move,("alice,'s  house,");

Console,.log(ne,xt.place,);

//  →  alice,'s  house,

Console,.log(ne,xt.parce,ls);

//  →  []

Console,.log(first.place,);

//  →  post  office,

Pe,rsiste,nt  data

Unchange,able,  data  layouts  are,  calle,d  immutable,  or  pe,rsiste,nt.  the,y  act  like,  strings  and  numbe,rs.  in  javascript,  you  can  change,  almost  e,ve,rything.  the,re,  is  a  function  name,d  obje,ct.fre,e,ze,  that  transforms  an  obje,ct  so  that  it  disre,gards  writing  to  its  prope,rtie,s.

Le,t  obje,ct  =  obje,ct.fre,e,ze,({value,:  5});

Obje,ct.value,  =  10;

Console,.log(obje,ct.value,);

//  →  5

Simulation

A  de,live,ry  robot  take,s  a  good  glance,  at  the,  world  and  de,te,rmine,s  what  dire,ction  it  move,s  to.  the,re,fore,,  a  robot  is  a  function  which  take,s  a  village,state,  obje,ct  and  se,nd  back  the,  name,  of  a  ne,arby  place,.  the,  robot  se,nds  back  an  obje,ct  consisting  of  its  inte,nde,d  dire,ction  and  a  me,mory  value,  re,turne,d  the,  ne,xt  time,  you  call  it.

Function  runrobot(state,,  robot,  me,mory)  {

For  (le,t  turn  =  0;;  turn++)  {

If  (state,.parce,ls.le,ngth  ==  0)  {

Console,.log(`done,  in  ${turn}  turns`);

Bre,ak;

}

Le,t  action  =  robot(state,,  me,mory);

State,  =  state,.move,(action.dire,ction);

Me,mory  =  action.me,mory;

Console,.log(`move,d  to  ${action.dire,ction}`);

}

}

The,  robot  can  walk  through  in  diffe,re,nt  dire,ctions  at  e,ve,ry  turn.  it  can  run  into  all  parce,ls  and  the,n  ge,t  to  its  de,live,ry  point.  be,low  is  an  e,xample,:

Function  randompick(array)  {

Le,t  choice,  =  math.floor(math.random()  *  array.le,ngth);

Re,turn  array[choice,];

}

Function  randomrobot(state,)  {

Re,turn  {dire,ction:  randompick(roadgraph[state,.place,])};

}

If  you  want  to  te,st  this  unique,  robot,  cre,ate,  a  ne,w  state,  with  fe,w  parce,ls.

Village,state,.random  =  function(parce,lcount  =  5)  {

Le,t  parce,ls  =  [];

For  (le,t  i  =  0;  i  <  parce,lcount;  i++)  {

Le,t  addre,ss  =  randompick(obje,ct.ke,ys(roadgraph));

Le,t  place,;

Do  {

Place,  =  randompick(obje,ct.ke,ys(roadgraph));

}  while,  (place,  ==  addre,ss);

Parce,ls.push({place,,  addre,ss});

}

Re,turn  ne,w  village,state,("post  office,",  parce,ls);

};

The,  do  loop  continue,s  to  se,le,ct  ne,w  place,s  whe,n  it  ge,ts  a  corre,ct  addre,ss.

Le,t’s  start  up  a  virtual  world.

Runrobot(village,state,.random(),  randomrobot);

//  →  advance,s  to  marke,tplace,

//  →  advance,s  to  town  hall

//  →…

//  →  run  in  63  turns

It  take,s  the,  robot  too  many  turns  to  transport  the,  parce,ls  be,cause,  the,re,  was  no  plan  ahe,ad.

The,  mail  truck's  route,

If  you  se,arch  a  route,  that  goe,s  through  all  the,  place,s  in  the,  village,,  that  could  run  twice,  by  the,  robot,  but  the,re,  is  a  guarante,e,  it  will  run  it.  be,low  is  an  e,xample,:

(starting  from  the,  post  office,):

Const  mailroute,  =  [

"alice,'s  house,,"  "cabin,"  "alice,'s  house,,"  "bob's  house,,"

"town  hall,"  "daria's  house,,"  "e,rnie,'s  house,,"

"gre,te,'s  house,",  "shop",  "gre,te,'s  house,",  "farm",

"marke,tplace,,"  "post  office,"

];

To  use,  the,  route,,  you  ne,e,d  to  utilize,  the,  robot  me,mory.  the,  re,st  of  the,  robot  route,  is  store,d  in  its  me,mory  and  dispatche,s  the,  first  e,le,me,nt  at  e,ve,ry  turn.

Function  route,robot(state,,  me,mory)  {

If  (me,mory.le,ngth  ==  0)  {

Me,mory  =  mailroute,s;

}

Re,turn  {dire,ction:  me,mory[0],  me,mory:  me,mory.slice,(01)};

}

The,  robot  is  faste,r  now.  it  take,s  a  maximum  of  26  turns  (twice,  the,  13-ste,p  route,)  but  more,  ofte,n  le,ss.

Pathfinding

An  inte,re,sting  approach  is  to  de,ve,lop  route,s  from  the,  starting  point,  and  inspe,ct  e,ve,ry  available,  place,  that  has  not  be,e,n  visite,d  until  it  attains  its  goal.  the,  be,low  illustration  e,xplains  that:

Function  findroute,(graph,  from,  to)  {

Le,t  work  =  [{at:  from,  route,:  []}];

For  (le,t  i  =  0;  i  <  work.le,ngth;  i++)  {

Le,t  {at,  route,}  =  work[i];

For  (le,t  location  of  graph[at])  {

If  (place,  ==  to)  re,turn  route,.concat(location);

If  (!Work.some,(w  =>  w.at  ==  location))  {

Work.push({at:  place,,  route,:  route,.concat(location)});

}

}

}

}

The,  function  save,s  a  work  list.  this  is  an  array  of  place,s  that  will  be,  inspe,cte,d  ne,xt,  toge,the,r  with  the,  route,.  it  be,gins  with  an  e,mpty  route,  and  the,  start  position.  e,ve,ry  location  can  be,  touche,d  from  e,ve,ry  location,  a  route,  can  also  be,  found  be,twe,e,n  two  points  the,re,fore,  the,  route,  will  not  fail.

Function  goalorie,nte,drobot({location,  parce,l},  route,s)  {

If  (route,.le,ngth  ==  0)  {

Le,t  parce,l  =  parce,l[0];

If  (parce,l.location  !=  place,)  {

Route,  =  findroute,(roadgraph,  location,  parce,l.place,);

}  e,lse,  {

Route,  =  findroute,(roadgrap

H,  location,  parce,l.addre,ss);

}

}

Re,turn  {dire,ction:  route,s[0],  me,mory:  route,.slice,(1)};

}

Summary

In  this  chapte,r  we,  touche,d  on  robots  using  javascript.  we,  got  to  the,  me,adow  fie,ld  village,  whe,re,  we,  talke,d  about  a  village,  with  11  place,s  and  14  roads,  the,n  we,  move,d  to  the,  pe,rsiste,nt  data,  whe,re,by  data  structure,s  be,have,  like,  strings  and  do  not  change,.  simulation  e,nable,s  you  to  pass  me,mory  to  robots  and  le,t  the,m  to  se,nd  back  a  ne,w  me,mory.

E,xe,rcise,

Write,  a  straightforward  javascript  program  to  conne,ct  e,ve,ry  e,le,me,nt  in  the,  be,low  array  into  a  string.

"re,d,  gre,e,n,  white,,  black"

"re,d,  gre,e,n,  white,,  black"

"re,d+gre,e,n+white,+black"

Solution

![00127.jpg](images/00127.jpeg) 

## Chapte,r  9:  bugs  and  e,rrors

Compute,r  program  flaws  are,  calle,d  bugs,  the,  mistake,s  made,  by  a  compute,r  program.

Strict  mode,

You  can  utilize,  javascript  in  a  strict  mode,.  this  can  be,  achie,ve,d  by  adding  the,  string  "use,  strict"  right  at  the,  top  of  a  file,.  be,low  is  an  illustration:

Function  canyouspotthe,proble,m()  {

"use,  strict";

For  (counte,r  =  0;  counte,r  <  10;  counte,r++)  {

Console,.log("happy  happy");

}

}

Canyouspotthe,proble,m();

//  →  re,fe,re,nce,e,rror:  counte,r  is  not  de,fine,d

Use,  the,  be,low  code,  whe,n  you  want  to  call  a  constructor  function  omitting  the,  ne,w  ke,yword  so  it  doe,sn’t  introduce,  a  ne,wly  cre,ate,d  obje,ct:

Function  pe,rson(name,)  {this.name,  =  name,;}

Le,t  fe,rdinand  =  pe,rson("fe,rdinand");  //  oops

Console,.log(name,);

//  →  fe,rdinand

The,  fake,  call  to  pe,rson  flourishe,d  but  se,nds  back  an  unde,fine,d  value,  and  builts  the,  global  binding  name,.  in  strict  mode,,  use,  "use,  strict";

Function  pe,rson(name,)  {this.name,  =  name,;}

Le,t  fe,rdinand  =  pe,rson("fe,rdinand");  //  forgot  ne,w

//  →  type,e,rror:  cannot  se,t  prope,rty  'name,'  of  unde,fine,d

The,  quickly  indicate,s  that  we,  have,  a  proble,m.  that's  good.  constructors  built  with  the,  class  notation  re,gularly  complains  whe,n  you  call  the,m  without  the,  ne,w.  strict  mode,  doe,s  not  allow  se,tting  function  multiple,  characte,rs  with  similar  name,  and  e,radicate,s  some,  language,  proble,ms.

Te,sting

You  can  use,  this  function  to  se,arch  for  mistake,s  in  a  program.  it  is  achie,ve,d  by  running  ove,r  and  ove,r  again.  the,  compute,r  is  e,xce,lle,nt  in  re,pe,titive,  tasks.  this  proce,ss  is  calle,d  automate,d  te,sting.  it  e,ntails  writing  a  program  that  te,sts  anothe,r  program.  te,sts  re,gularly  go  through  small  labe,le,d  programs  that  de,te,rmine,  some,  part  of  your  code,.  for  instance,,  le,t  us  cre,ate,  a  se,t  of  te,sts  for  the,  touppe,rcase,  me,thod.  be,low  is  an  illustration:

Function  te,st(labe,l,  body)  {

If  (!Body())  console,.log(`faile,d:  ${labe,l}`);

}

Te,st("conve,rt  latin  te,xt  to  uppe,rcase,",  ()  =>  {

Re,turn  "he,llo".touppe,rcase,()  ==  "he,llo";

});

Te,st("conve,rt  gre,e,k  te,xt  to  uppe,rcase,",  ()  =>  {

Re,turn  "χαίρετε".touppe,rcase,()  ==  "χαίρετε";

});

Te,st("don't  conve,rt  case,-le,ss  characte,rs",  ()  =>  {

Re,turn  "ࢎ࠶߈ఆ௷".touppe,rcase,()  ==  "ࢎ࠶߈ఆ௷";

131

});

De,bugging

Whe,n  a  program  displays  an  e,rror,  the,  ne,xt  thing  is  to  de,te,rmine,  the,  proble,m  and  ge,t  it  fixe,d.  the,  e,rror  me,ssage,  will  point  dire,ctly  at  a  particular  line,  in  your  block  of  code,.  take,  a  look  at  the,  e,rror  de,scription,  and  you  will  find  the,  proble,matic  line,.  this  e,xample,  program  trie,s  to  transform  a  whole,  numbe,r  into  a  string  within  se,t  base,  (de,cimal,  binary,  and  so  on)  by  continuously  se,le,cting  out  the,  last  digit  and  dividing  the,  numbe,r  to  e,radicate,  the,  digit.

Function  numbe,rtostring(n,  base,  =  10)  {

Le,t  re,sult  =  "",  sign  =  "";

If  (n  <  0)  {

Sign  =  "-";

N  =  -n;

}

Do  {

Re,sult  =  string(n  %  base,)  +  re,sult;

N  /=  base,;

}  while,  (n  >  0);

Re,turn  sign  +  re,sult;

}

Console,.log(numbe,rtostring(13,  10));

//  →  1.5e,-3231.3e,-3221.3e,-3211.3e,-3201.3e,-3191.3e,…-3181.3

Adding  some,  console,.log  calls  into  the,  program  is  an  e,xce,lle,nt  path  to  take,  if  you  want  to  acquire,  additional  information  about  the,  e,xe,cution.  we,  want  n  to  ge,t  the,  value,s  13,  1,  and  the,n  0.  we,  should  state,  the,  value,  at  the,  be,ginning  of  the,  loop'

13

1.3

0.13

0.013…

1.5e,-323

Dividing  13  by  will  not  provide,  a  whole,  numbe,r.  inste,ad  of  n  /=  base,,  what  we,  want  is  n  =  math.floor(n  /  base,)  so  that  the,  numbe,r  can  be,  “shifte,d”  to  the,  right.

Anothe,r  gre,at  way  to  spe,cify  a  bre,akpoint  is  to  inse,rt  a  de,bugge,r  state,me,nt  (ke,yword)  into  your  program.  if  the,  de,ve,lope,r  tools  will  pick  it  up  and  pause,  the,  program  anytime,  it  ge,ts  to  that  state,me,nt  if  your  browse,r  is  active,.

E,xce,ptions

Whe,n  a  function  is  cannot  go  furthe,r,  the,  e,xce,ption  handling  is  the,  place,  that  unde,rstands  how  to  fix  that  proble,m.  e,xce,ptions  are,  a  tool  that  e,nable,s  a  block  of  code,  that  runs  into  difficultie,s  to  throw  an  e,xce,ption,  and  an  e,xce,ption  could  be,  any  value,.  you  can  inte,ntionally  cre,ate,  proble,ms  within  your  line,  of  code,  to  catch  the,  e,xce,ption  during  its  zooming  down  the,  proce,ss  so  that  you  can  use,  it  to  solve,  the,  proble,m  and  continue,  your  work.

He,re,’s  an  e,xample,:

Function  promptdire,ction(que,stion)  {

Le,t  re,sult  =  prompt(que,stion);

If  (re,sult.tolowe,rcase,()  ==  "le,ft")  re,turn  "l";

If  (re,sult.tolowe,rcase,()  ==  "right")  re,turn  "r";

Throw  ne,w  e,rror("invalid  dire,ction:  "  +  re,sult);

}

Function  look()  {

If  (promptdire,ction("which  way?")  ==  "l")  {

Re,turn  "a  house,";

}  e,lse,  {

Re,turn  "two  angry  be,ars";

135

}

}

Try  {

Console,.log("you  se,e,",  look());

}  catch  (e,rror)  {

Console,.log("some,thing  we,nt  wrong:  "  +  e,rror);

}

Raise,  an  e,xce,ption  by  using  the,  throw  ke,yword.

Cle,aning  up  afte,r  e,xce,ptions

An  e,xce,ption’s  e,ffe,ct  is  a  diffe,re,nt  type,  of  control  flow.  this  indicate,s  that  your  code,  can  have,  diffe,re,nt  side,  e,ffe,cts,  but  an  e,xce,ption  could  stop  the,m  from  happe,ning.  be,low  is  some,  bad  banking  code,:

Const  accounts  =  {

A:  100,

B:  0,

C:  20

};

Function  ge,taccount()  {

Le,t  accountname,  =  prompt("e,nte,r  an  account  name,");

If  (!Accounts.hasownprope,rty(accountname,))  {

Throw  ne,w  e,rror(`no  such  account:  ${accountname,}`);

}

Re,turn  accountname,;

}

Function  transfe,r(from,  amount)  {

If  (accounts[from]  <  amount)  re,turn;

Accounts[from]  -=  amount;

Accounts[ge,taccount()]  +=  amount;

}

The,  transfe,r  function  is  use,d  to  se,nd  a  particular  sum  of  mone,y  from  a  state,d  account  to  anothe,r,  as  we,ll  as  de,manding  for  the,  name,  of  the,  othe,r  account.  if  you  input  a  wrong  account  name,,  ge,taccount  outputs  an  e,xce,ption.  if  the,  mone,y  has  be,e,n  se,nt  from  the,  first  account  and  the,n  the,  program  outputs  an  e,xce,ption  be,fore,  it  ge,ts  the,  mone,y  transfe,rre,d  into  the,  othe,r  account,  the,  mone,y  will  disappe,ar.  solve,  this  proble,m,  utilize,  the,  finally  block  code,.  this  is  illustrate,d  be,low:

Function  transfe,r(from,  amount)  {

If  (accounts[from]  <  amount)  re,turn;

Le,t  progre,ss  =  0;

Try  {

Accounts[from]  -=  amount;

Progre,ss  =  1;

Accounts[ge,taccount()]  +=  amount;

Progre,ss  =  2;

}  finally  {

If  (progre,ss  ==  1)  {

Accounts[from]  +=  amount;

}

}

}

Se,le,ctive,  catching

Whe,n  an  e,xce,ption  make,s  it  to  the,  bottom  of  a  block  of  code,  without  e,rrors,  it  is  handle,d  by  the,  e,nvironme,nt.  invalid  use,s  such  as  inspe,cting  up  a  prope,rty  on  null,  citing  a  none,xiste,nt  binding,  or  calling  a  non-function  will  re,sult  in  raise,d  e,xce,ptions.  the,se,  e,xce,ptions  can  be,  caught.  javascript  doe,s  not  support  se,le,ctive,  catching  of  e,xce,ptions.  be,low  is  an  e,xample,  that  trie,s  to  continue,  calling  promptdire,ction  until  it  provide,s  a  valid  answe,r:

For  (;;)  {

Try  {

Le,t  dir  =  promtdire,ction("whe,re,?");  //  ←  typo!

Console,.log("you  se,le,ct  ",  dir);

Bre,ak;

}  catch  (e,)  {

Console,.log("invalid  dire,ction.  try  again.");

}

}

The,  for  (;;)  construct  is  use,d  to  build  a  loop  that  cannot  be,  te,rminate,d  on  its  own.  you  can  bre,ak  out  of  the,  loop  whe,n  you  have,  a  valid  dire,ction,  but  a  misspe,lle,d  promptdire,ction  will  output  an  unde,fine,d  variable,  e,rror.  if  you  want  to  catch  a  particular  type,  of  e,xce,ption,  che,ck  in  the,  catch  block  if  the,  e,xce,ption  you  have,  is  the,  same,  one,  you  want  and  re,throw  it.  le,t’s  de,scribe,  a  ne,w  kind  of  e,rror  and  utilize,  instance,  of  to  re,cognize,  it.

Class  inpute,rror  e,xte,nds  e,rror  {}

Function  promptdire,ction(que,stion)  {

Le,t  re,sult  =  prompt(que,stion);

If  (re,sult.tolowe,rcase,()  ==  "le,ft")  re,turn  "l";

If  (re,sult.tolowe,rcase,()  ==  "right")  re,turn  "r";

Throw  ne,w  inpute,rror("invalid  dire,ction:  "  +  re,sult);

}

The,  ne,w  e,rror  class  prolongs  e,rror.  it  doe,s  not  de,scribe,  its  own  constructor,  it  inhe,rits  the,  e,rror  constructor,  which  anticipate,s  a  string  me,ssage,  that  we,  can  re,cognize,  it  with.

Now  the,  loop  can  catch  the,se,  more,  care,fully.

For  (;;)  {

Try  {

Le,t  dir  =  promptdire,ction("whe,re,?");

Console,.log("you  chose,  ",  dir);

Bre,ak;

}  catch  (e,)  {

If  (e,  instance,of  inpute,rror)  {

Console,.log("invalid  dire,ction.  try  again.");

}  e,lse,  {

Throw  e,;

}

}

}

Summary

This  chapte,r  de,als  with  de,bugging.  an  e,sse,ntial  part  of  programming  is  ide,ntifying  and  fixing  bugs.  some,time,s,  you  can  solve,  proble,ms  locally.  you  can  track  the,m  with  spe,cial  re,turn  value,s  or  the,  use,  of  e,xce,ptions.

E,xe,rcise,

Fix  the,  be,low  broke,n  code,  and  indicate,  the,  proble,m:

For(var  i=0;  i  >  5;  i++){

Console,.log(i)

}

Solution

![00152.jpg](images/00152.jpeg)

Proble,m  –  incorre,ct  condition  within  the,  loop.

## Chapte,r  10:  re,gular  e,xpre,ssions

Programming  conce,pts  and  tools  advance,s  in  a  disorganize,d  way,  but  its  succe,ss  indicate,s  an  e,xce,lle,nt  pie,ce,  of  te,chnology.  in  this  chapte,r,  we,  will  discuss  re,gular  e,xpre,ssions.  the,y  are,  use,d  to  de,fine,  patte,rns  within  a  string  data.  the,y  cre,ate,  a  small,  diffe,re,nt  language,  that  consists  of  javascript  as  we,ll  as  othe,r  language,s.

Cre,ating  a  re,gular  e,xpre,ssion

A  re,gular  e,xpre,ssion  is  constructe,d  with  the,  re,ge,xp  constructor  or  writte,n  as  a  strict  value,  by  surrounding  a  patte,rn  in  forward-slash  (/)  characte,rs.

Le,t  re,1  =  ne,w  re,ge,xp("abc");

Le,t  re,2  =  /abc/;

The,se,  two  re,gular  e,xpre,ssion  obje,cts  stand  for  the,  same,  patte,rn.  whe,n  utilizing  the,  re,ge,xp  constructor,  write,  the,  patte,rn  as  a  normal  string  so  that  the,  rule,s  apply  for  backslashe,s.

The,  se,cond  notation  influe,nce,  backslashe,s  diffe,re,ntly,  first  put  a  backslash  be,fore,  any  forward  slash  be,cause,  the,  patte,rn  displays  be,twe,e,n  slash  characte,rs.

Te,sting  for  matche,s

Re,gular  e,xpre,ssion  obje,cts  contain  se,ve,ral  me,thods,  one,  of  which  is  the,  te,st.  whe,n  you  pass  a  string,  it  re,turns  a  boole,an  de,te,rmining  if  a  string  contains  a  match  of  the,  patte,rn  in  the,  e,xpre,ssion.

Console,.log(/abc/.te,st("abcde,"));

//  →  true,

Console,.log(/abc/.te,st("abxde,"));

//  →  false,

A  re,gular  e,xpre,ssion  contains  only  non-spe,cial  characte,rs  that  re,pre,se,nt  the,  succe,ssion  of  characte,rs.  if  abc  pape,rs  anywhe,re,  in  the,  string,  we,  are,  running  a  te,st,  the,  te,st  will  re,turn  true,.

Se,ts  of  characte,rs

Re,gular  e,xpre,ssions  e,nable,  us  to  indicate,  difficult  patte,rns.  if  you  want  to  e,qual  any  numbe,r  in  a  re,gular  e,xpre,ssion,  place,  a  se,t  of  characte,rs  in-be,twe,e,n  square,  bracke,ts.  the,  following  e,xpre,ssions  e,qual  e,ve,ry  string  within  a  digit:

Console,.log(/[0123456789]/.te,st("in  1992"));

//  →  true,

Console,.log(/[0-9]/.te,st("in  1992"));

//  →  true,

A  hyphe,n  (-)  be,twe,e,n  two  characte,rs  inside,  square,  bracke,ts  is  use,d  to  spe,cify  a  scope,  of  characte,rs  that  the,  characte,r’s  unicode,  numbe,rs  de,cide,  the,  command.  characte,rs  from  0  to  9  stay  ne,xt  to  e,ach  othe,r  in  this  command  (code,s  48  to  57),  so  [0-9]  wrapping  the,m  all  and  e,quals  any  digit.  common  characte,r  groups  contain  individual  shortcuts  built-in.

Digits  are,  part  of  the,m:  \d  me,ans  the,  e,xact  thing  as  [0-9].

\d  any  characte,r  digit

\w  an  alphanume,ric  characte,r  (“word  characte,r”)

\s  any  white,space,  characte,r  (space,,  tabs,  ne,wline,,  and  similar)

\d  a  characte,r  which  is  not  a  digit

\w  a  nonalphanume,ric  characte,r

\s  a  nonwhite,space,  characte,r

.  any  characte,r  without  for  ne,wline,

So,  match  a  date,  and  time,  format  like,  01-30-2003  15:20  with  the,  e,xpre,ssion  be,low:

Le,t  date,time,  =  /\d\d-\d\d-\d\d\d\d  \d\d:\d\d/;

Console,.log(date,time,.te,st("01-30-2003  15:20"));

//  →  true,

Console,.log(date,time,.te,st("30-jan-2003  15:20"));

//  →  false,

The,se,  backslash  code,s  are,  also  utilize,d  within  the,  square,  bracke,ts.  for  instance,,  [\d.]  indicate,s  any  digit  or  pe,riodic  characte,r  but  the,  pe,riod  has  no  me,aning  as  we,ll  as  othe,r  unique,  characte,rs,  like,  +.

Le,t  notbinary  =  /[^01]/;

Console,.log(notbinary.te,st("1100100010100110"));

//  →  false,

Console,.log(notbinary.te,st("1100100010200110"));

//  →  true,

Re,pe,ating  parts  of  a  patte,rn

Now  you  have,  a  pe,rfe,ct  unde,rstanding  of  how  to  e,qual  single,  digits.  if  you  want  to  match  a  whole,  numbe,r  or  a  succe,ssion  of  more,  digits,  place,  a  plus  sign  (+)  imme,diate,ly  afte,r  an  input  in  a  re,gular  e,xpre,ssion.  this  signifie,s  that  the,  e,le,me,nt  could  re,pe,at  more,  than  once,,  /\d+/  e,quals  one,  or  more,-digit  characte,rs.

Console,.log(/'\d+'/.te,st("'123'"));

//  →  true,

Console,.log(/'\d+'/.te,st("''"));

//  →  false,

Console,.log(/'\d*'/.te,st("'123'"));

//  →  true,

Console,.log(/'\d*'/.te,st("''"));

//  →  true,

The,  star  (*)  e,nable,s  the,  patte,rn  to  e,qual  ze,ro.  in  the,  be,low  e,xample,,  the,  u  characte,r  is  pe,rmitte,d  to  rise,,  but  the,  patte,rn  is  also  e,qual  whe,n  it  is  not  found.

Le,t  ne,ighbor  =  /ne,ighbour/;

Console,.log(ne,ighbor.te,st("ne,ighbour"));

//  →  true,

Console,.log(ne,ighbor.te,st("ne,ighbor"));

//  →  true,

To  de,te,rmine,  if  a  patte,rn  should  e,xe,cute,  a  ce,rtain  numbe,r  of  time,s,  utilize,  the,  brace,s,  inse,rting  {4}  afte,r  an  e,le,me,nt.  if  you  want  it  to  e,xe,cute,  pre,cise,ly  four  time,s,  de,fine,  a  range,  like,  this:

{2,4}  signifie,s  that  the,  e,le,me,nt  must  e,xe,cute,  twice,  and  at  most  four  time,s.  be,low  is  anothe,r  patte,rn  of  the,  date,  and  time,  patte,rn,  which  e,nable,s  both  single,  and  double,-digit  days,  months  and  hours.

Le,t  date,time,  =  /\d{01,2}-\d{1,2}-\d{4}  \d{1,2}:\d{2}/;

Console,.log(date,time,.te,st("01-30-2003  8:45"));

//  →  true,

Grouping  sube,xpre,ssions

If  you  want  to  utilize,  an  ope,rator  like,  *  or  +  on  one,  or  more,  e,le,me,nt  concurre,ntly,  use,  the,  pare,nthe,se,s.  some,  parts  of  a  re,gular  e,xpre,ssion,  which  is  cite,d  in  pare,nthe,se,s,  counts  as  an  individual  e,le,me,nt  as  long  as  the,  ope,rators  are,  conce,rne,d.

Le,t  cartooncrying  =  /boo+(hoo+)+/i;

Console,.log(cartooncrying.te,st("boohoooohoohooo"));

//  →  true,

The,  first  and  se,cond  +  characte,rs  only  apply  to  the,  se,cond  in  boo  and  hoo.  the,  third  +  indicate,s  to  the,  e,ntire,  group  (hoo+),  e,qualing  one,  or  more,  succe,ssions  like,  that.  the,  i  e,nding  the,  first  e,xpre,ssion  in  the,  e,xample,  is  use,d  for  case,  inse,nsitive,,  e,nabling  it  to  e,qual  the,  uppe,rcase,  b  in  the,  input  string.  although  the,  patte,rn  is  e,ntire,ly  lowe,rcase,.

Matche,s  and  groups

The,  te,st  me,thod  is  the,  be,st  way  to  e,qual  a  re,gular  e,xpre,ssion,  it  de,te,rmine,s  if  it  matche,s  only.  re,gular  e,xpre,ssions  contain  an  e,xe,c  (e,xe,cute,)  me,thod,  which  will  output  null  if  it  could  find  a  match  and  se,nds  back  an  obje,ct  containing  data  about  the,  match.

Le,t  match  =  /\d+/.e,xe,c("one,  two  100");

Console,.log(match);

//  →  ["100"]

Console,.log(match.inde,x);

//  →  8

A  se,nt  back  obje,ct  from  e,xe,c  contains  an  inde,x  prope,rty,  which  de,te,rmine,  what  part  of  the,  string  the,  thriving  match  starts.  be,low  is  the,  succe,ssion  of  digits  ne,e,de,d:

String  value,s  contain  a  match  me,thod  that  be,have,s  similarly.

Console,.log("one,  two  100".match(/\d+/));

//  →  ["100"]

Whe,n  the,  re,gular  e,xpre,ssion  holds  sube,xpre,ssions  collate,d  with  pare,nthe,se,s,  the,  matching  te,xt  will  display  in  the,  array.  the,  whole,  match  is  the,  first,  the,  ne,xt  is  the,  matche,d  part  by  the,  first  group,  and  the,n  the,  following  group,  e,tc.

Le,t  quote,dte,xt  =  /'([^']*)'/;

Console,.log(quote,dte,xt.e,xe,c("she,  said  'he,llo'"));

//  →  ["'he,llo'",  "he,llo"]

Whe,n  a  group  was  not  finish  be,ing  matche,d  (if  it  contains  a  que,stion  mark),  it  outputs  unde,fine,d.  whe,n  you  match  a  group  se,ve,ral  time,s,  only  the,  last  match  finishe,s  in  the,  array.

Console,.log(/bad(ly)?/.e,xe,c("bad"));

//  →  ["bad",  unde,fine,d]

Console,.log(/(\d)+/.e,xe,c("123"));

//  →  ["123",  "3"]

The,  date,  classe,s

Javascript  consists  of  a  standard  class  that  re,pre,se,nt  date,s;  it  is  calle,d  date,.  if  you  want  to  build  a  date,  obje,ct  utilizing  ne,w,  first  ge,t  the,  curre,nt  time,  and  date,.

Console,.log(ne,w  date,());

//  →  mon  nov  11  2023  16:19:11  gmt+0100  (ce,t)

You  can  as  we,ll  build  an  obje,ct  for  a  particular  time,.

Console,.log(ne,w  date,(2008,  11,  8));

//  →  we,d  de,c  08  2008  00:00:00  gmt+0100  (ce,t)

Console,.log(ne,w  date,(2008,  11,  9,  12,  59,  59,  999));

//  →  we,d  de,c  08  2009  12:59:59  gmt+0100  (ce,t)

You  should  follow  the,  javascript  date,  naming  conve,ntion  whe,re,  month  numbe,rs  be,gin  at  ze,ro  (the,re,fore,,  de,ce,mbe,r  is  11),  and  day  numbe,rs  be,gin  at  1.

The,  hours,  minute,s,  se,conds,  and  millise,conds  argume,nts  are,  voluntary  and  re,cognize,d  as  ze,ro  whe,n  not  spe,cifie,d.  time,stamps  are,  save,d  as  the,  numbe,r  of  millise,conds  in  the,  utc  time,  zone,.  following  by  a  conve,ntion  se,t  by  “unix  time,”.

Console,.log(ne,w  date,(2016,  11,  14).ge,ttime,s());

//  →  1445677600000

Console,.log(ne,w  date,(1445677600000));

//  →mon  de,c  11  2008  00:01:00  gmt+0100  (ce,t)

Whe,n  the,  date,  constructor  is  se,t  a  single,  argume,nt,  the,  argume,nt  is  re,cognize,d  as  a  millise,cond  count.  de,te,rmine,  the,  curre,nt  millise,cond  count  by  building  a  ne,w  date,  obje,ct  and  call  ge,ttime,  on  it  or  use,  the,  date,.now  function.  date,  obje,cts  produce,  me,thods  such  like,  ge,tdate,,  ge,thours,  ge,tfullye,ar,  ge,tmonth,  ge,tminute,s,  and  ge,tse,conds  to  re,trie,ve,  the,ir  compone,nts.

Function  ge,tdate,(strings)  {

Le,t  [_,  month,  day,  ye,ar]  =

/(\d{01,2})-(\d{01,2})-(\d{4})/.e,xe,c(strings);

Re,turn  the,  ne,w  date,(ye,ar,  month  -  1,  day);

}

Console,.log(ge,tdate,("1-30-2003"));

//  →  thursday  jan  30  2003  00:00:00  gmt+0100  (ce,t)

String  and  word  boundarie,s

You  can  e,nsure,  that  the,  match  spans  the,  e,ntire,  string  by  adding  the,  marke,rs  ^  and  $.  the,  care,t  e,quals  the,  be,ginning  of  the,  input  string,  while,  the,  dollar  sign  e,quals  the,  e,nd.  the,re,fore,,  /^\d+$/  matche,s  a  string  continuing  multiple,  or  one,  digits,  /^!  /  matche,s  any  string  that  be,gins  with  an  e,xclamation  mark,  and  /x^/  matche,s  no  string.  if  you  want  the,  date,  to  be,gin  and  e,nd  on  a  boundary  word,  utilize,  the,  marke,r  \b.  a  word  boundary  can  be,gin  or  finish  strings  containing  a  word  characte,r  (\w)  on  one,  side,  and  a  nonword  characte,r  on  the,  othe,r.

Console,.log(/cat/.te,st("concate,nate,"));

//  →  true,

Console,.log(/\bcat\b/.te,st("concate,nate,"));

//  →  false,

Choice,  patte,rns

If  you  want  to  know  if  chunk  of  te,xt  consists  of  a  numbe,r  and  followe,d  by  words  such  as  chicke,n,  pig,  or  cow,  le,t’s  write,  thre,e,  re,gular  e,xpre,ssions  and  te,st  the,m.  we,  utilize,  the,  pipe,  characte,r  (|)  to  mark  a  choice,  be,twe,e,n  the,  patte,rn  to  the,  le,ft  and  right:

Le,t  animalcount  =  /\b\d+  (pig|cows|chicke,n)s?\b/;

Console,.log(animalcount.te,st("15  pigs"));

150

//  →  true,

Console,.log(animalcount.te,st("15  pigchicke,ns"));

//  →  false,

The,  re,place,  me,thod

String  value,s  contains  a  re,place,  me,thod,  which  is  use,d  to  re,store,  part  of  the,  string  with  anothe,r  one,.

Console,.log("papa".re,place,("p",  "m"));

//  →  mapa

The,  first  argume,nt  can  e,qually  be,  a  re,gular  e,xpre,ssion.  it  re,place,s  the,  first  match  of  the,  re,gular  e,xpre,ssion.  if  you  add  a  g  option  (for  global)  to  the,  e,xpre,ssion,  e,ve,ry  match  containe,d  in  the,  string  is  re,place,d,  and  not  first  only.

Console,.log("borobudur".re,place,(/[ou]/,  "a"));

//  →  barobudur

Console,.log("borobudur".re,place,(/[ou]/g,  "a"));

//  →  barabadar

The,  major  importance,  of  utilizing  re,gular  e,xpre,ssions  with  re,place,  is  be,cause,  it  re,fe,rs  to  matche,d  groups  in  the,  re,place,me,nt  string.  for  instance,,  you  have,  a  large,  string  consisting  of  pe,ople,'s  name,,  one,  name,  pe,r  line,,  using  the,  format  lastname,,  firstname,.  you  can  as  we,ll  change,  and  re,move,  the,se,  name,s,  e,radicate,  the,  comma  to  ge,t  a  firstname,  lastname,  format,  and  utilize,  the,  following  code,:

Console,.log(

"liskov,  barbara\nmccarthy,  john\nwadle,r,  philip"

.re,place,(/(\w+),  (\w+)/g,  "$2  $1"));

//  →  barbara  liskov

//  john  mccarthy

//  philip  oaks

The,  $1  and  $2  containe,d  in  the,  re,place,me,nt  string  re,fe,r  to  the,  group  in  pare,nthe,se,s  in  patte,rn.  $1  is  re,store,d  by  the,  te,xt,  which  matche,s  opposing  the,  first  group,  $2  up  to  $9.  e,ach  and  e,ve,ry  match  can  be,  re,fe,rre,d  to  with  $&.  you  can  pass  a  function  inste,ad  of  a  string  as  the,  se,cond  argume,nt  to  re,store,.  for  e,ach  re,place,me,nt,  the,  function  is  calle,d  with  the,  matche,d  group  as  argume,nts,  and  include,  the,  re,turn  value,  into  the,  ne,w  string.  be,low  is  an  e,xample,:

Le,t  s  =  "the,  cia  and  fbi";

Console,.log(s.re,place,s(/\b(fbi|cia)\b/g,

Str  =>  str.touppe,rcase,()));

//  →  the,  cia  and  fbi

He,re,’s  a  more,  inte,re,sting  one,:

Le,t  stock  =  "1  le,mon,  2  cabbage,s,  and  101  e,ggs";

Function  minusone,(match,  amount,  units)  {

Amount  =  numbe,r(amount)  -  1;

If  (amount  ==  1)  {//  just  one,  le,ft,  re,move,  the,  's'

Unit  =  unit.slice,(0,  unit.le,ngth  -  1);

}  e,lse,  if  (amount  ==  0)  {

Amount  =  "no";

}

Re,turn  amount  +  "  "  +  units;

}

Console,.log(stock.re,place,s(/(\d+)  (\w+)/g,  minusone,));

//  →  no  le,mon,  1  cabbage,,  and  100  e,ggs

Gre,e,d

You  can  use,  re,place,  to  write,  a  function  that  e,radicate,s  all  comme,nts  from  a  block  of  javascript  code,.  look  be,low:

Function  stripcomme,nts(code,)  {

Re,turn  code,.re,place,(/\/\/.*|\/\*[^]*\*\//g,  "");

}

Console,.log(stripcomme,nts("1  +  /*  2  */3"));

//  →  1  +  3

155

Console,.log(stripcomme,nts("x  =  10;//  te,n!"));

//  →  x  =  10;

Console,.log(stripcomme,nts("1  /*  a  */+/*  b  */  1"));

//  →  1  1

The,  se,ction  be,fore,  the,  or  ope,rator  matche,s  two  slash  characte,rs  accompanie,d  with  any  numbe,r  that  is  not  a  ne,wline,  characte,r.  use,  [^]  to  match  any  characte,r.

Re,pe,titive,  ope,rators  (+,  *,  and  {})  are,  calle,d  gre,e,dy  which  me,ans  the,y  match  and  the,y  can  also  backtrack.  if  a  que,stion  mark  is  place,d  afte,r  the,m  (+?,  *?,  ??,  {}?),  the,  gre,e,d  disappe,ars  and  be,gin  matching  no  matte,r  how  small.  the,  smalle,st  stre,tch  of  characte,rs  which  brings  a  */,  is  the,  star  match.  it  absorbs  one,  block  comme,nt  only.

Function  stripcomme,nts(code,)  {

Re,turn  code,.re,place,(/\/\/.*|\/\*[^]*?\*\//g,  "");

}

Console,.log(stripcomme,nts("1  /*  a  */+/*  b  */  1"));

//  →  1  +  1

Dynamically  cre,ating  re,ge,xp  obje,cts

The,re,  are,  fe,w  instance,s  whe,re,by  you  would  not  unde,rstand  the,  spe,cific  patte,rn  you  should  match  against  whe,n  your  code,  is  be,ing  writte,n.  if  you  want  to  se,arch  for  the,  use,r  name,  in  a  chunk  of  te,xt  and  wrap  it  in  unde,rscore,  characte,rs  to  make,  it  unique,.  but  you  can  cre,ate,  a  string  and  utilize,  the,  re,ge,xp  constructor.  be,low  is  an  e,xample,:

Le,t  name,  =  "harry";

Le,t  te,xt  =  "harry  is  a  suspicious  characte,r.";

Le,t  re,ge,xp  =  ne,w  re,ge,xp("\\b("  +  name,  +  ")\\b",  "gi");

Console,.log(te,xt.re,place,(re,ge,xp,  "_$1_"));

//  →  _harry_  is  a  suspicious  characte,r.

If  you  want  to  build  the,  \b  boundary  marke,rs,  utilize,  the,  two  backslashe,s  be,cause,  you  would  write,  the,m  in  a  normal  string.  the,  se,cond  argume,nt  to  the,  re,ge,xp  constructor  consists  of  the,  options  ne,e,de,d  for  the,  re,gular  e,xpre,ssion.  the,  "gi"  re,pre,se,nt  global  and  case,  inse,nsitive,.  be,low  is  an  e,xample,:

Le,t  name,  =  "de,a+hl[]rd";

Le,t  te,xt  =  "this  de,a+hl[]rd  guy  is  supe,r  annoying.";

Le,t  e,scape,d  =  name,.re,place,(/[\\[.+*?(){|^$]/g,  "\\$&");

Le,t  re,ge,xp  =  ne,w  re,ge,xp("\\b"  +  e,scape,d  +  "\\b",  "gi");

Console,.log(te,xt.re,place,(re,ge,xp,  "_$&_"));

//  →  this  _de,a+hl[]rd_  guy  is  ve,ry  annoying.

The,  se,arch  me,thod

You  cannot  call  the,  inde,xof  me,thod  on  strings  a  re,gular  e,xpre,ssion.  you  can  also  use,  anothe,r  me,thod,  se,arch  whe,re,by  you  can  call  the,  inde,xof  me,thod  a  re,gular  e,xpre,ssion,  and  it  se,nds  back  the,  first  inde,x  whe,re,  it  se,e,s  the,  e,xpre,ssion  and  whe,n  it  doe,s  not  se,e,  it  re,turns  -1.

Console,.log("  word".se,arch(/\s/));

//  →  2

Console,.log("  ".se,arch(/\s/));

//  →  -1

The,  lastinde,x  prope,rty

The,  e,xe,c  me,thod  doe,s  not  produce,  a  be,tte,r  way  to  be,gin  the,  se,arch  from  a  state,d  position  in  the,  string.  re,gular  e,xpre,ssion  obje,cts  contain  prope,rtie,s.  one,  of  the,  prope,rtie,s  is  calle,d  source,,  and  it  consists  of  the,  string  that  built  the,  e,xpre,ssion.  lastinde,x  is  anothe,r  prope,rty,  and  it  influe,nce,s  some,  small  circumstance,s,  whe,re,  the,  ne,xt  match  will  be,gin.  the,  re,gular  e,xpre,ssion  must  contain  the,  global  (g)  or  sticky  (y)  option,  and  the,  match  will  occur  using  the,  e,xe,c  me,thod.  illustration  be,low:

Le,t  patte,rn  =  /y/g;

Patte,rn.lastinde,x  =  3;

Le,t  match  =  patte,rn.e,xe,c("xyzzy");

Console,.log(match.inde,x);

//  →  4

Console,.log(patte,rn.lastinde,x);

//  →  5

The,  dissimilarity  be,twe,e,n  the,  global  and  the,  sticky  options  is  that,  whe,n  you  e,nable,  sticky,  the,  match  succe,e,ds  if  it  be,gins  at  lastinde,x,  while,  with  global,  it  will  find  a  position  for  the,  match  can  be,gin.

Le,t  global  =  /abc/g;

Console,.log(global.e,xe,c("xyz  abc"));

//  →  ["abc"]

Le,t  sticky  =  /abc/y;

Console,.log(sticky.e,xe,c("xyz  abc"));

//  →  null

If  you  are,  utilizing  a  share,d  re,gular  e,xpre,ssion  value,  for  se,ve,ral  e,xe,c  calls,  proble,ms  will  occur  with  the,  automatic  update,s  to  the,  lastinde,x  prope,rty.

Le,t  digit  =  /\d/g;

Console,.log(digit.e,xe,c("it  is  he,re,  :  1"));

//  →  ["1"]

Console,.log(digit.e,xe,c("and  now:  1"));

//  →  null

The,  global  option  also  transforms  the,  conce,pt  the,  match  me,thod  on  strings  works.

Looping  ove,r  matche,s

The,  be,st  thing  to  do  is  to  scan  across  all  e,ve,nts  of  a  patte,rn  in  a  string  giving  acce,ss  to  the,  match  obje,ct  in  the,  loop  body.  use,  the,  lastinde,x  and  e,xe,c  to  achie,ve,  this.

Le,t  input  =  "a  string  with  thre,e,  numbe,rs  in  it...  42  and  88.";

Le,t  numbe,r  =  /\b\d+\b/g;

Le,t  match;

While,  (match  =  numbe,r.e,xe,c(input))  {

Console,.log("found",  match[0],  "at",  match.inde,x);

}

//  →  found  3  at  14

//  found  42  at  33

//  found  88  at  40

The,  assignme,nt  e,xpre,ssion  value,  (=)  is  the,  spe,cifie,d  value,.  so  utilizing  match  =  numbe,r.e,xe,c  (input)  as  the,  condition  within  the,  while,  state,me,nt,  the,  match  is  we,  e,xe,cute,  the,  match  at  the,  be,ginning  of  e,ve,ry  ite,ration,  store,  the,  re,sult  within  a  binding,  and  stop  looping  whe,n  matche,s  can  no  longe,r  find.

Parsing  an  ini  file,

Se,arche,ngine,=https://duckduckgo.com/?Q=$1

Spite,fulne,ss=9.7

;  comme,nts  are,  pre,ce,de,d  by  a  se,micolon

;  e,ach  se,ction  conce,rns  an  individual  e,ne,my

[larry]

Fullname,=larry  doe,

Type,=kinde,rgarte,n  bully

We,bsite,=http://www.google,.com/google,/

[davae,orn]

Fullname,=davae,orn

Type,=e,vil  witch

Outputdir=/home,/margin/e,ne,my/davae,orn

The,  rule,s  for  this  format  (which  is  a  ge,ne,rally  use,d  format,  usually  calle,d

An  ini  file,)  is:

·  ignore,  blank  line,s  and  line,s  be,ginning  with  se,micolons.

·  line,s  e,nclose,d  in  [and]  be,gin  a  ne,w  se,ction.

·  line,s  consisting  of  an  alphanume,ric  ide,ntifie,r  accompanie,d  by  a  =  characte,r  attach  a  se,tting  to  the,  curre,nt  se,ction.

·  e,ve,rything  e,lse,  is  invalid.

Our  mission  he,re,  is  to  change,  a  string  like,  this  to  an  obje,ct,  which  prope,rtie,s  use,  string  to  store,  se,ttings  that  are,  writte,n  be,fore,  the,  subobje,cts  for  se,ctions  and  the,  first  se,ction  he,ade,r.  the,  subobje,cts  hold  that  se,ction’s  se,ttings.  use,  a  carriage,  re,turn  characte,r  followe,d  by  a  ne,wline,  ("\r\n")  inste,ad  of  a  ne,wline,  characte,r  to  diffe,re,ntiate,  line,s.  this  will  make,  the,  split  me,thod  e,nable,  a  re,gular  e,xpre,ssion  as  its  argume,nt,  you  can  utilize,  a  re,gular  e,xpre,ssion  like,  /\r?\n/  to  divide,  it  in  a  way  that  e,nable,s  both  "\n"  and  "\r\n"  be,twe,e,n  line,s.

Function  parse,ini(string)  {

//  be,gin  with  an  obje,ct  to  hold  the,  top-le,ve,l  fie,lds

Le,t  re,sult  =  {};

Le,t  se,ction  =  re,sult;

String.split(/\r?\n/).fore,ach(line,  =>  {

Le,t  match;

If  (match  =  line,.match(/^(\w+)=(.*)$/))  {

Se,ction[match[1]]  =  match[2];

}  e,lse,  if  (match  =  line,.match(/^\[(.*)\]$/))  {

Se,ction  =  re,sult[match[1]]  =  {};

}  e,lse,  if  (!  /^\s*(;.*)?$/.te,st(line,))  {

Throw  ne,w  e,rror("line,  '"  +  line,  +  "'  invalid.");

}

});

Re,turn  re,sult;

}

Console,.log(parse,ini(`

Name,=vasilis

[addre,ss]

City=te,ssaloniki`));

//  →  {name,:  "vasilis",  addre,ss:  {city:  "te,ssaloniki"}}

The,  code,  advance,s  ove,r  the,  file,  line,s  and  cre,ate,  up  an  obje,ct.  prope,rtie,s  at  the,  top  are,  save,d  straight  into  that  obje,ct,  whe,re,by  prope,rtie,s  can  be,  found  in  se,ctions  are,  save,d  in  a  diffe,re,nt  se,ction  obje,ct.  the,  se,ction  binding  points  to  the,  obje,ct  for  the,  e,xisting  se,ction.  the,re,  are,  two  type,s  of  important  line,s—se,ction  he,ade,rs  or  prope,rty  line,s.  if  a  line,  is  always  prope,rty,  it  is  save,d  in  the,  e,xisting  se,ction.  if  it  is  a  se,ction  he,ade,r,  build  a  ne,w  se,ction  obje,ct,  and  se,t  se,ction  to  it.

The,  patte,rn  if  (match  =  string.match())  is  ide,ntical  to  the,  trick  of  utilizing  an  assignme,nt  as  the,  condition  for  a  while,.

Inte,rnational  characte,rs

Be,cause,  of  javascript’s  initial  simplistic  imple,me,ntation  and  that  this  approach  se,t  in  stone,  as  standard  be,havior,  javascript’s  re,gular  e,xpre,ssions  are,  some,what  dumb  about  characte,rs  that  don’t  show  in  the,  e,nglish  language,.  for  instance,,  in  javascript,  re,gular  e,xpre,ssions,  a  “word  characte,r”  is  just  one,  of  the,  26  characte,rs  in  the,  latin  alphabe,t  (lowe,rcase,  or  uppe,rcase,),  de,cimal  digits,  and  the,  unde,rscore,  characte,r.  characte,rs  like,  é  or  ß,  are,  word  characte,rs,  the,y  will  not  match  \w,  will  match  uppe,rcase,  \w,  the,  nonword  cate,gory.  it  indicate,s  that  characte,rs  compose,d  of  two  code,  units.

Console,.log(/🍎{3}/.te,st("🍎🍎🍎"));

//  →  false,

Console,.log(/<.>/.te,st("<🌹>"));

//  →  false,

Console,.log(/<.>/u.te,st("<🌹>"));

//  →  true,

The,  ide,ntifie,d  proble,m  he,re,  is  that  🍎  in  the,  first  line,  is  be,ing  manage,d  as  two  code,  units,  and  the,  {3}  se,ction  is  use,d  to  the,  se,cond  one,  only.  the,  dot  also  matche,s  a  single,  code,  unit.  add  u  option  (for  unicode,)  to  your  re,gular  e,xpre,ssion  so  that  it  manage,s  that  characte,rs  prope,rly.  the,  wrong  be,havior  re,main  se,t  as  the,  de,fault,  unfortunate,ly,  be,cause,  transforming  that  could  cre,ate,  proble,ms  for  curre,nt  code,  that  de,pe,nds  on  it.

You  can  use,  \p  in  a  re,gular  e,xpre,ssion  to  match  e,ve,ry  characte,r  that  unicode,  standard  give,s  a  se,t  prope,rty.

Console,.log(/\p{script=gre,e,k}/u.te,st("α"));

//  →  true,

Console,.log(/\p{script=arabic}/u.te,st("α"));

//  →  false,

Console,.log(/\p{alphabe,tic}/u.te,st("α"));

//  →  true,

Console,.log(/\p{alphabe,tic}/u.te,st("!"));

//  →  false,

Unicode,  de,scribe,s  a  numbe,r  of  important  prope,rtie,s,  although  se,arching  for  the,  one,  that  you  ne,e,d  may  not  always  be,  trivial.

Summary

We,  focuse,d  on  re,gular  e,xpre,ssions  in  this  chapte,r.  an  obje,ct  that  stands  for  patte,rns  in  strings  is  a  re,gular  e,xpre,ssion.  the,y  consist  of  the,ir  language,  and  utilize,  it  for  the,  e,xhibition  of  the,se,  patte,rns.

/abc/  a  succe,ssion  of  characte,rs

/[abc]/  characte,r  from  a  range,  of  characte,rs

/[^abc]/  any  characte,r  abse,nt  in  a  range,  of  characte,rs

/  [0-9]/  any  characte,r  within  a  se,t  of  characte,rs

/x+/  one,  or  more,  e,ve,nts  of  the,  patte,rn  x

/x+?  /  one,  or  more,  e,ve,nts,  nongre,e,dy

/x*/  ze,ro  or  more,  e,ve,nts

/x?  /  ze,ro  or  one,  e,ve,nts

/x  {2,4}/  two  to  four  e,ve,nts

/(abc)/  a  group

/a|b|c/  any  one,  of  various  patte,rns

/\d/  any  digit  characte,r

/\w/  an  word  characte,r

/\s/  any  white,space,  characte,r

/.  /  any  characte,r  e,xcluding  ne,wline,s

/\b/  a  word  boundary

/^/  be,ginning  of  input

/$/  e,nd  of  input

A  re,gular  e,xpre,ssion  consists  of  a  me,thod  te,st  to  che,ck  if  a  se,t  string  matche,s  it.  it  also  contains  an  e,xe,c  me,thod,  whe,re,by  whe,n  it  finds  a  match,  it  se,nds  back  an  array  having  e,ve,ry  matche,d  group.  this  type,  of  array  contains  an  inde,x  prope,rty  that  spe,cifie,s  whe,re,  the,  match  starte,d.  strings  use,  a  matching  me,thod  to  match  the,m  in  opposition  to  a  re,gular  e,xpre,ssion  as  we,ll  as  a  se,arch  me,thod  to  find  one,,  se,nding  back  only  the,  be,ginning  position  of  the,  match.

E,xe,rcise,

Write,  a  javascript  program  working  as  a  trim  function  (string)  utilizing  re,gular  e,xpre,ssion.

Solution

![00146.jpg](images/00146.jpeg)![00156.jpg](images/00156.jpeg)

## Chapte,r  11:  module,s

This  particular  program  has  a  simple,  layout.  it  is  ve,ry  to  e,xplain  its  conce,pt,  and  e,ve,ry  part  plays  a  pre,cise,  role,.  the,  organizing  and  maintaining  of  the,  layout  can  be,  much  more,  work,  but  it  e,ve,ntually  pays  off  the,  ne,xt  time,  some,one,  use,s  the,  program  in  the,  future,.  the,re,fore,,  you  can  be,  intrigue,d  to  ne,gle,ct  it  and  e,nable,  the,  program  parts  to  be,come,  inte,rmixe,d,  which  will  cre,ate,  two  practical  issue,s.  first,  whe,n  e,ve,rything  touche,s  e,ve,rything  e,lse,,  it  is  hard  to  look  at  any  se,t  pie,ce,  in  se,paration.  you  will  have,  to  cre,ate,  a  compre,he,nsive,  unde,rstanding  of  the,  full  program.  se,cond,  using  any  of  the,  functionality  from  the,  program  in  diffe,re,nt  situations,  you  can  re,write,  it  inste,ad  of  dise,ngaging  it  from  the,  conte,xt.

Module,s

A  module,  is  a  type,  of  program  that  de,te,rmine,s  which  pie,ce,s  it  should  de,pe,nd  on  and  what  functionality  should  it  produce,  for  othe,r  pie,ce,s  to  utilize,.  by  putting  a  limit  on  the,  ways  module,s  communicate,  with  one,  anothe,r,  the,  syste,m  is  ide,ntical  to  le,go,  whe,re,  pie,ce,s  communicate,  using  straightforward  conne,ctors,  and  not  like,  mud  whe,re,  the,  e,ntire,  pie,ce,s  mix  with  e,ve,rything.  de,pe,nde,ncie,s  are,  the,  re,lationships  be,twe,e,n  module,s.  whe,n  a  module,  wants  a  pie,ce,  from  anothe,r  module,,  it  de,pe,nds  on  that  module,.  the,  module,  itse,lf  illustrate,s  this  fact,  and  it  is  use,d  to  de,te,rmine,  which  othe,r  module,s  should  be,  available,  to  use,  a  state,d  module,  and  to  load  de,pe,nde,ncie,s  automatically.  e,ve,ry  module,  ne,e,ds  its  scope,  to  se,parate,  itse,lf  from  othe,r  module,s.

Package,s

One,  significant  be,ne,fit  of  building  a  program  out  of  diffe,re,nt  pie,ce,s,  and  be,ing  able,  to  launch  those,  pie,ce,s  individually,  is  that  you  can  apply  the,  same,  pie,ce,  in  se,parate,  programs.  whe,n  the,  duplication  of  code,  be,gins,  the,  package,  come,s  in  to  play.  a  package,  is  a  block  of  code,  that  can  be,  share,d.  it  may  consist  of  one,  or  more,  module,s  and  holds  information  about  the,  othe,r  de,pe,nding  package,s.  package,s  also  contain  docume,ntation  de,scribing  its  functions  so  that  pe,ople,  who  didn’t  write,  it  can  utilize,  it.  whe,n  a  proble,m  occurs  in  a  package,,  or  you  add  a  ne,w  fe,ature,,  the,  package,  update,s  automatically.  now  programs  de,pe,nding  on  its  upgrade,s  to  the,  late,st  ve,rsion.  working  like,  this,  you  ne,e,d  infrastructure,.  a  place,  to  save,  and  se,arch  for  package,s  and  an  e,asy  way  to  upgrade,  and  install  the,m.  whe,n  it  come,s  to  javascript,  npm  provide,s  support.

Divide,  npm  into  two  things:  an  online,  se,rvice,  whe,re,  you  can  upload  and  download  package,s  and  a  program  that  handle,s  the,  installation  and  manage,me,nt.  almost  e,ve,ry  code,  on  npm  is  lice,nse,d.

Improvise,d  module,s

Be,fore,  the,  ye,ar  2015,  the,  javascript  language,  did  not  contain  any  built-in  module,  syste,m,  but  pe,ople,  have,  be,e,n  cre,ating  large,  syste,ms  using  javascript  for  ove,r  a  de,cade,  now,  and  the,y  re,quire,d  module,s.  the,y  de,ve,lope,d  the,ir  module,  syste,ms  and  inte,grate,d  the,m  into  the,  language,.  you  can  utilize,  javascript  functions  to  build  local  scope,s  and  obje,cts  to  stand  for  module,  layouts.  use,  this  module,  to  ove,r  be,twe,e,n  day  name,s  and  numbe,rs.  its  layout  contains  the,  we,e,kday.  name,  and  we,e,kday.

.numbe,r,  and  it  hide,s  its  local  binding  name,s  inside,  the,  scope,  of  a  function

The,  e,xpre,ssion  is  calle,d  upon  imme,diate,ly.

Const  we,e,kday  =  function()  {

Const  name,s  =  ["sunday",  "monday",  "tue,sday",  "we,dne,sday",

"thursday",  "friday",  "saturday"];

Re,turn  {

Name,(numbe,r)  {re,turn  name,s[numbe,r];},

Numbe,r(name,)  {re,turn  name,s.inde,xof(name,);}

};

}();

Console,.log(we,e,kday.name,(we,e,kday.numbe,r("sunday")));

//  →  sunday

This  style,  of  module,s  doe,s  not  proclaim  de,pe,nde,ncie,s.  the,y  place,  the,  layout  into  the,  global  scope,.  this  style,  of  module,s  provide,s  isolation  to  a  ce,rtain  de,gre,e,,  but  it  doe,s  not  de,clare,  de,pe,nde,ncie,s.  inste,ad,  it  just  puts  its  inte,rface,  into  the,  global  scope,  and  awaits  its  de,pe,nde,ncie,s,  if  the,re,  is  any,  to  do  the,  same,.

E,valuating  data  as  code,

The,re,  are,  diffe,re,nt  type,s  of  ways  to  take,  data  and  launch  it  as  part  of  the,  e,xisting  program.  the,  be,st  way  is  to  utilize,  the,  unique,  ope,rator  e,val,  which  affe,cts  a  string  in  the,  e,xisting  scope,.

Const  x  =  1;

Function  e,valandre,turnx(code,)  {

E,val(code,);

Re,turn  x;

}

Console,.log(e,valandre,turnx("var  x  =  2"));

//  →  2

Console,.log(x);

//  →  1

A  le,ss  complicate,d  way  to  e,xplain  data  as  code,  is  using  the,  function  constructor.  it  take,s  two  type,s  of  argume,nt,  a  string  with  a  comma,  divide,d  list  of  argume,nt  name,s  and  a  string  with  the,  body  function.  it  e,nclose,s  the,  code,  in  a  function  value,  to  e,nable,  it  ge,t  its  own  scope,.

Le,t  plusone,  =  function("n",  "re,turn  n  +  1;");

Console,.log(plusone,(4));

//  →  5

You  can  e,nclose,  the,  module,'s  code,  in  a  function  and  utilize,  that  same,  function  scope,  as  a  module,  scope,.

Commonjs

The,  common  approach  use,d  to  gobble,  on  javascript  module,s  is  the,  commonjs  module,s.  node,.js  use,s  this  approach  as  we,ll  as  a  lot  of  package,s  on  npm.  the,  major  ide,a  in  commonjs  module,s  is  the,  function  name,d  re,quire,.  if  you  call  this  toge,the,r  with  the,  de,pe,nde,ncy's  module,  name,,  it  loads  the,  module,  and  se,nds  back  its  inte,rface,.  the,  loade,r  cove,rs  the,  module,  code,  within  a  function,  and  module,s  have,  the,ir  local  scope,  automatically.  you  can  call  re,quire,  to  se,e,  the,ir  de,pe,nde,ncie,s  and  place,  the,ir  layout  in  the,  obje,ct  that  e,xports  the,m.  this  e,xample,  module,  give,s  a  date,-formatting  function.  it  utilize,s  two  package,s  from  npm,  the,  ordinal  to  transform  numbe,rs  to  strings  like,  "1st"  and  "2nd",  and  date,-name,s  to  obtain  the,  e,nglish  name,s  for  months  and  we,e,kdays.  it  e,xports  a  single,  function,  formatdate,,  that  take,s  a  te,mplate,  string  and  a  date,  obje,ct.  the,  te,mplate,  string  could  contain  code,s  that  control  the,  format,  such  as  yyyy  (the,  full  ye,ar)  and  do  for  the,  ordinal  day  of  the,  month.  you  can  se,t  a  string  to  it  like,  "mmmm  do  yyyy"  to  ge,t  output  like,  “de,ce,mbe,r  2nd,  2013”.

Const  ordinal  =  re,quire,("ordinal");

Const  {days,  months}  =  re,quire,("date,-name,s");

E,xports.formatdate,  =  function(date,,  format)  {

Re,turn  format.re,place,(/yyyy|m(mmm)?|do?|dddd/g,  tag  =>  {

If  (tag  ==  "yyyy")  re,turn  date,.ge,tfullye,ar();

If  (tag  ==  "m")  re,turn  date,.ge,tmonth();

If  (tag  ==  "mmmm")  re,turn  months[date,.ge,tmonth()];

If  (tag  ==  "d")  re,turn  date,.ge,tdate,();

If  (tag  ==  "do")  re,turn  ordinal(date,.ge,tdate,());

If  (tag  ==  "dddd")  re,turn  days[date,.ge,tday()];

});

};

The,  layout  of  the,  ordinal  is  a  single,  function,  whe,re,by  the,  date,-name,s  e,xports  an  obje,ct  that  consists  of  se,ve,ral  othe,r  things,  months  and  days  are,  arrays  of  name,s.  re,structuring  is  quite,  e,asy  whe,n  building  bindings  for  importe,d  layouts.  the,  module,  attache,s  its  layout  function  to  e,xports  so  that  module,s  that  re,ly  on  it  have,  acce,ss  to  it.  utilize,  the,  module,  this  way:

Const  {formatdate,}  =  re,quire,(“.  /format-date,");

Console,.log(formatdate,(ne,w  date,(2017,  9,  13),

"dddd  the,  do"));

//  →  friday  the,  13th

We,  can  de,fine,  re,quire,,  in  its  most  minimal  form,  like,  this:

Re,quire,.cache,  =  obje,ct.cre,ate,(null);

Function  re,quire,(name,)  {

If  (!  (name,  in  re,quire,.cache,))  {

Le,t  code,  =  re,adfile,(name,);

Le,t  module,  =  {e,xports:  {}};

Re,quire,.cache,[name,]  =  module,;

Le,t  wrappe,r  =  function("re,quire,,  e,xports,  module,",  code,);

Wrappe,r(re,quire,,  module,.e,xports,  module,);

}

Re,turn  re,quire,.cache,[name,].e,xports;

}

In  this  code,,  re,adfile,  is  a  powe,re,d  function  that  re,ads  a  file,  and  se,nds  back  its  conte,nts  as  a  string.  standard  javascript  doe,s  not  offe,r  such  functionality,  but  se,ve,ral  othe,r  javascript  e,nvironme,nts  such  as  node,.js  and  the,  browse,r  offe,rs  the,ir  unique,  ways  of  acce,ssing  file,s.  the,  above,  e,xample,  bluffs  that  re,adfile,  e,xists.  to  ke,e,p  away  from  loading  the,  same,  module,  se,ve,ral  time,s,  you  ne,e,d  a  store,  (cache,)  of  alre,ady  loade,d  module,s.  if  calle,d,  it  e,xamine,s  if  the,  de,mande,d  module,  loads  and,  if  not,  it  loads  it.  it  re,quire,s  re,ading  the,  module,’s  code,,  e,nclosing  it  within  a  function  and  calling  it.  the,  layout  of  the,  ordinal  package,  from  e,arlie,r  is  a  function  and  not  an  obje,ct.  the,  commonjs  module,s  cre,ate,  an  e,mpty  layout  obje,ct  using  the,  module,  syste,m  for  you  to  e,xport,  re,store,  that  with  value,s  by  ove,rwriting  module,.e,xports.  module,s  do  this  to  e,xport  a  single,  value,  inste,ad  of  a  layout  obje,ct.  by  de,scribing  e,xports,  re,quire,  and  module,  as  parame,te,rs  for  the,  cre,ate,d  e,nclosing  function  (and  se,tting  the,  right  value,s  while,  calling  it),  the,  loade,r  e,nsure,s  that  the,se,  bindings  are,  acce,ssible,  within  the,  module,’s  scope,.  strings  se,t  to  re,quire,  is  inte,rpre,te,d  to  a  file,name,  or  we,b  addre,ss  vary  in  se,parate,  syste,ms.  whe,n  it  starts  with  “.  /"  or.  “/,"  it  is  usually  translate,d  as  re,lative,  to  the,  e,xisting  module,’s  file,name,.  so  “.  /  format-date,"  will  be,  the,  file,  calle,d  format-date,.js  in  the,  same,  dire,ctory.

If  the,  name,  is  not  re,lative,,  node,.js  will  se,arch  for  a  package,  that  is  installe,d  by  that  name,.

Now,  inste,ad  of  writing  your  own  ini  file,  parse,r,  you  can  utilize,  one,  from  npm.

Const  {parse,}  =  re,quire,("ini");

Console,.log(parse,("x  =  10\ny  =  20"));

//  →  {x:  "10",  y:  "20"}

E,cmascript  module,s

Commonjs  module,s  pe,rform  we,ll  while,  combining  with  npm,  and  the,y  e,nable,  the,  javascript  community  to  be,gin  code,sharing  on  a  substantial  scale,.  the,  notation  is  quite,  we,ird.  the,  things  adde,d  to  e,xports  are,  not  acce,ssible,  within  the,  local  scope,.  without  running  the,  code,  of  a  module,,  it  will  be,  tough  to  de,te,rmine,  its  de,pe,nde,ncie,s  be,fore,  taking  any  argume,nt.  that  is  the,  re,ason  javascript  standard  e,stablishe,s  its  own,  se,parate,  module,  syste,m.  it  is  name,d  calle,d  e,s  module,s,  whe,re,  e,s  re,pre,se,nts  e,cmascript.  the,  initial  ide,a  of  de,pe,nde,ncie,s  and  inte,rface,s  stay  the,  same,,  but  the,ir  de,tails  are,  diffe,re,nt.  the,  notation  inte,grate,s  into  the,  language,.  you  can  now  use,  a  unique,  import  ke,yword  to  acce,ss  a  de,pe,nde,ncy  inste,ad  of  calling  a  function.

Import  ordinal  from  "ordinal";

Import  {days,  months}  from  "date,-name,s";

E,xport  function  formatdate,(date,,  format)  {  /*  ...  */  }

Use,  the,  e,xport  ke,yword  to  e,xport  things.  it  could  display  at  the,  front  of  a  class,  function  or  binding  de,finition  (le,t,  const,  or  var).  an  e,s  module,’s  layout  doe,s  not  re,pre,se,nt  a  single,  value,  but  a  se,t  of  name,d  bindings.  the,  pre,vious  module,  attache,s  formatdate,  to  a  function.  if  you  import  from  a  diffe,re,nt  module,,  the,  binding  come,s  with  it,  and  not  the,  value,,  which  me,ans  the,  value,  of  an  e,xporting  module,  can  change,  the,  binding  any  time,,  and  the,  importing  module,s  will  re,cognize,  its  ne,w  value,.  if  a  binding  is  name,d  de,fault,  re,cognize,s  it  as  the,  module,’s  major  e,xporte,d  value,.  if  a  module,  like,  ordinal  imports  in  the,  e,xample,,  omitting  the,  brace,s  across  the,  binding  name,,  you  will  find  its  de,fault  binding.  to  de,ve,lop  a  de,fault  e,xport,  write,  e,xport  de,fault  ahe,ad  of  e,xpre,ssion,  a  class  or  a  function  de,claration.

E,xport  de,fault  ["winte,r",  "spring",  "summe,r",  "autumn"];

You  can  re,name,  importe,d  bindings  using  the,  word  like,  this.

Import  {days  as  dayname,s}  from  "date,-name,s";

Console,.log(dayname,s.le,ngth);

//  →  7

Anothe,r  major  diffe,re,nce,  is  that  the,  e,s  module,  imports  occur  be,fore,  a  module,’s  script  be,gins  to  run.  import  de,clarations  may  not  display  within  functions  or  blocks,  and  the,  de,pe,nde,nt  name,s  should  be,  quote,d  strings  and  not  arbitrary  e,xpre,ssions.  a  lot  of  proje,cts  are,  writte,n  through  e,s  module,s  and  the,n  change,d  to  some,  othe,r  format  whe,n  it  is  publishe,d.  during  a  transitional  pe,riod,  use,  two  se,parate,  module,  syste,ms  side,  by  side,.

Module,  de,sign

Program  structuring  is  one,  of  the,  nice,  fe,ature,s  of  programming.  any  unknown  functionality  can  mode,l  in  diffe,re,nt  ways.  the,  good  program  de,sign  is  a  pe,rsonalize,d  one,,  and  the,re,  is  a  matte,r  of  pre,fe,re,nce,  and  taste,.  to  unde,rstand  the,  value,  of  we,ll-organize,d  de,sign,  you  ne,e,d  to  re,ad  and  work  on  se,ve,ral  programs  and  take,  note,  of  pe,rforming  and  non-pe,rforming  functions.  the,  module,  de,sign  is  straightforward  to  use,.  the,  ini  package,  module,  follows  the,  standard  json  obje,ct  by  supplying  stringify  and  parse,  (to  write,  an  ini  file,)  functions,  and,  like,  json,  change,s  be,twe,e,n  plain  obje,cts  and  strings.  a  lot  of  the,  ini-file,  parsing  module,s  on  npm  supply  a  function  that  re,ads  that  type,  of  file,  from  the,  hard  disk  and  parse,s  it.  conce,ntrate,d  module,s  that  calculate,  value,s  are,  suitable,  in  a  large,r  range,  of  programs  than  large,r  module,s  that  e,xe,cute,  comple,x  actions  that  have,  side,  e,ffe,cts.  an  ini  file,  re,ade,r  that  want  to  re,ad  the,  file,  from  disk  is  not  use,ful  in  case,s  whe,re,by  the,  file,’s  conte,nt  come,s  from  anothe,r  source,.  similarly,  state,ful  obje,cts  are,  occasionally  ne,ce,ssary  and  use,ful,  but  if  you  can  use,  a  function,  utilize,  it.  various  ini  file,  re,ade,rs  on  npm  give,s  a  layout  style,  that  ne,e,ds  you  to  build  an  obje,ct,  the,n  load  the,  file,  into  the,  obje,ct,  and  use,  spe,cific  me,thods  to  achie,ve,  the,  de,sire,d  re,sults.  it  is  the,  obje,ct-orie,nte,d  style,  and  tradition.  in  javascript,  the,re,  is  no  particular  way  to  re,pre,se,nt  a  graph.  the,re,  are,  various  pathfinding  package,s  available,  on  npm,  but  none,  utilize,s  the,  graph  format.  the,y  ofte,n  le,t  graph  e,dge,s  contain  a  we,ight,  and  that  is  the,  distance,  or  cost-re,late,d  with  it.  for  instance,,  we,  have,  the,  dijkstrajs  package,.  a  re,cognize,d  way  to  pathfinding,  re,late,d  to  the,  findroute,  function  is  the,  dijkstra’s  algorithm,  afte,r  e,dsge,r  dijkstra,  the,  package,  first  write,r.  the,  js  suffix  is  re,gularly  attache,d  to  package,  name,s  to  spe,cify  that  you  can  write,  in  javascript.  so,  if  you  want  to  use,  that  package,,  e,nsure,  that  the,  graph  save,s  in  its  e,xpe,cte,d  format.

Const  {find_path}  =  re,quire,("dijkstrajs");

Le,t  graph  =  {};

For  (le,t  node,  of  obje,ct.ke,ys(roadgraph))  {

Le,t  e,dge,s  =  graph[node,]  =  {};

For  (le,t  de,st  of  roadgraph[node,])  {

E,dge,s[de,st]  =  1;

}

}

Console,.log(find  path(graph,  "post  office,",  "cabin"));

//  →  ["post  office,",  "alice,'s  house,",  "cabin"]

It  can  be,  a  roadblock  to  composition  whe,n  se,ve,ral  package,s  use,  se,parate,  data  structure,s  to  de,fine,  re,late,d  things,  and  it  is  hard  to  combine,  the,m.  the,re,fore,,  whe,n  you  are,  de,signing  for  composability,  know  e,xactly  the,  data  structure,s  othe,rs  are,  using  and  you  can  follow  the,ir  e,xample,.

Summary

In  this  chapte,r,  we,  cove,re,d  the,  module,s.  module,s  give,  structure,  to  more,  e,xte,nsive,  programs  by  diffe,re,ntiating  the,  code,  into  bits  with  unde,rstandable,  de,pe,nde,ncie,s  and  inte,rface,s.  the,  inte,rface,  is  a  module,  which  you  can  se,e,  from  othe,r  module,s,  and  the,  de,pe,nde,ncie,s  are,  diffe,re,nt  module,s  that  it  use,s.

E,xe,rcise,

Write,  a  javascript  program  to  show  the,  curre,nt  day  and  time,  in  the,  following  format.

Today  is  tue,sday.

Curre,nt  time,  is:  10  pm:  30:  38

Solution

![00103.jpg](images/00103.jpeg)![00032.jpg](images/00032.jpeg) 

## Chapte,r  12:  asynchronous  programming

The,  proce,ssor  is  a  vital  part  of  a  compute,r  that  pe,rforms  the,  individual  ste,ps  that  balance,  our  programs.  the,  spe,e,d  le,ve,l  of  some,thing  like,  a  loop  that  influe,nce,s  numbe,rs  comple,tion  de,pe,nds  on  the,  proce,ssor's  spe,e,d.  a  lot  of  programs  communicate,  with  things  outside,  of  the,  proce,ssor.  for  instance,,  the,y  may  inte,ract  through  a  compute,r  ne,twork  or  de,mand  for  data  from  the,  hard  disk,  which  is  quite,  slowe,r  than  obtaining  it  from  me,mory.  in  part,  the,  ope,rating  syste,m  handle,s  this  part  and  will  change,  the,  proce,ssor  be,twe,e,n  various  programs  that  are,  running.

Asynchronicity

In  the,  asynchronous  programming  mode,l,  e,ve,rything  occurs  one,  at  a  time,.  if  you  call  a  function  that  e,xe,cute,s  a  long  duration  action,  re,sults  will  re,turn  whe,n  the,  ope,ration  comple,te,s  only.  no  othe,r  action  would  be,  able,  to  take,  place,  during  e,xe,cution.  an  asynchronous  mode,l  e,nable,s  se,ve,ral  things  to  occur  at  the,  same,  time,.  whe,n  an  action  be,gins,  the,  program  doe,s  not  stop  running.  whe,n  the,  task  comple,te,s,  it  notifie,s  the,  program  and  can  acce,ss  the,  re,sult  (for  instance,,  the,  information  re,ad  from  disk).  you  can  diffe,re,ntiate,  be,twe,e,n  synchronous  and  asynchronous  programming  through  a  little,  e,xample,:  a  program  that  obtains  two  re,source,s  from  the,  ne,twork  and  the,n  unifie,s  the,  re,sults.

In  an  asynchronous  e,nvironme,nt,  the,  re,que,st  function  re,turns  whe,n  the,  work  comple,te,s.  the,  simple,st  way  to  e,xe,cute,  this  task  is  to  call  the,  re,que,sts  one,  afte,r  anothe,r.  it  consists  of  the,  drawback  that  be,gins  the,  se,cond  re,que,st  only  whe,n  the,  first  task  comple,te,s.  the,  sum  of  both  re,sponse,  time,s  will  be,  the,  total  time,  take,n.  to  solve,  this  proble,m  in  a  synchronous  syste,m,  start  adding  thre,ads  of  control.  a  thre,ad  is  a  running  program  that  its  e,xe,cution  could  be,  re,nde,re,d  with  othe,r  programs  through  the,  ope,rating  syste,m  be,cause,  mode,rn  compute,rs  have,  se,ve,ral  proce,ssors,  various  thre,ads  can  run  at  once,  on  se,parate,  proce,ssors.  a  se,cond  thre,ad  may  be,gin  the,  se,cond  re,que,st,  and  the,n  the,  two  thre,ads  both  wait  for  the,ir  re,sults  to  re,turn,  afte,r  that,  the,y  re,synchronize,  to  unify  both  re,sults.  in  the,  asynchronous  mode,l,  the,  ne,twork  time,  is  part  of  the,  time,line,  for  a  state,d  thre,ad  of  control.  in  an  asynchronous  mode,l,  launching  a  ne,twork  action  notional  cre,ate,s  a  division  in  the,  time,line,.  the,  program  that  comme,nce,s  the,  action  doe,s  not  stop  running,  and  the,n  the,  action  occurs  with  it,  it  informs  the,  program  whe,n  it  comple,te,s.

Anothe,r  way  to  de,te,rmine,  the,  similaritie,s  is  that  waiting  for  tasks  to  comple,te,  is  indire,ct  in  the,  synchronous  mode,l,  while,  it  is  dire,ctly  unde,r  our  control,  in  the,  asynchronous  one,.

Callbacks

One,  proce,dure,  to  asynchronous  programming  is  to  e,nable,  functions  that  e,xe,cute,  a  slow  action  to  gain  an  e,xtra  argume,nt,  and  the,  argume,nt  is  calle,d  a  callback  function.  whe,n  the,  action  be,gins  and  e,nds,  you  should  call  the,  re,sult  with  the,  callback  function.  for  instance,,  the,  se,ttime,out  function,  acce,ssible,  both  in  the,  browse,rs  and  node,.js,  waits  a  state,d  numbe,r  of  millise,conds  and  the,n  calls  a  function.  se,ttime,out(()  =>  console,.log("tick"),  500);  waiting  is  not  an  ide,al  type,  of  work,  but  can  be,  applicable,  whe,n  you  are,  running  programs  like,  an  animation  update,  or  che,cking  if  a  function  is  taking  longe,r  than  the,  spe,cifie,d  time,.  running  se,ve,ral  asynchronous  tasks  in  a  row  through  callbacks  signifie,s  that  you  have,  to  continue,  se,tting  ne,w  functions  to  control  the,  continuation  of  the,  calculations  afte,r  the,  actions.

A  lot  of  crow  ne,st  compute,rs  consist  of  a  longstanding  data  storage,  bulb,  whe,re,  data  is  store,d  into  twigs  so  that  it  can  be,  acce,sse,d  and  re,store,d  late,r.  storing,  or  se,arching  for  a  pie,ce,  of  data  take,s  little,  time,,  so  the,  layout  to  longstanding  storage,  is  asynchronous  and  utilize,s  callback  functions.  storage,  bulbs  save,  bits  of  json-e,ncodable,  data  unde,r  name,s.  a  crow  could  save,  data  about  place,s  it  has  hidde,n  food  unde,r  the,  name,  "food  cache,s,"  that  holds  an  array  of  name,s  that  point  at  othe,r  pie,ce,s  of  data,  de,fining  the,  cache,.  to  se,arch  for  a  food  cache,  in  the,  storage,  bulbs  of  the,  big  oak  ne,st,  a  crow  could  run  code,  this  way:

Import  {bigoak}  from  “.  /crow-te,ch";

Bigoak.re,adstorage,("food  cache,s",  cache,s  =>  {

Le,t  firstcache,  =  cache,s[0];

Bigoak.re,adstorage,(firstcache,,  info  =>  {

Console,.log(info);

});

});

This  programming  style,  is  practicable,,  but  the,  inde,ntation  le,ve,l  e,xpands  with  e,ve,ry  asynchronous  action  be,cause,  it  le,ads  in  anothe,r  function.  pe,rforming  some,  difficult  task  such  as  running  se,ve,ral  actions  concurre,ntly,  can  ge,t  we,ird.  crow  ne,st  compute,rs  are,  cre,ate,d  to  inte,ract  through  re,que,st-re,sponse,  pairs.  that  me,ans  one,  ne,st  transfe,rs  a  me,ssage,  to  the,  othe,r  ne,st,  which  instantly  re,turns  a  me,ssage,,  affirming  re,ce,ipt  and  attaching  a  re,ply  to  the,  me,ssage,  que,stions.  e,ve,ry  me,ssage,  e,armark  with  a  type,,  which  de,cide,s  how  it  controls.  your  code,  can  de,scribe,  handle,rs  for  ce,rtain  re,que,st  type,s,  and  whe,n  the,  re,que,st  come,s  in,  the,  handle,r  is  calle,d  to  provide,  a  re,ply.  the,  layout  e,xporte,d  by  the,  “.  /crow-te,ch"  module,  produce,s  callback-base,d  functions  for  inte,raction.  ne,sts  contain  a  se,nd  me,thod  which  se,nds  off  a  re,que,st.  it  awaits  the,  re,que,st  type,,  the,  targe,t  ne,st  name,,  and  the,  re,que,ste,d  conte,nt  as  its  first  thre,e,  argume,nts,  and  it  e,xpe,cts  a  function  to  call  whe,n  a  re,ply  come,s  in  as  its  fourth  and  last  argume,nt.

Bigoak.se,nd("cow  pasture,",  "note,",  "le,t's  caw  loudly  at  7pm",

()  =>  console,.log("note,  de,live,re,d."));

But  to  make,  sure,  ne,st  can  re,ce,ive,  that  re,que,st,  you  must  state,  a  re,que,st  type,  name,d  "note,."  the,  code,  that  controls  the,  re,que,sts  that  ne,e,d  to  run  and,  on  all  ne,sts,  can  re,ce,ive,  this  type,  of  me,ssage,s.  le,t  us  state,  that  a  crow  flie,s  ove,r  and  installs  our  handle,r  code,  on  all  the,  ne,sts.

Import  {de,fine,re,que,sttype,}  from  “.  /crow-te,ch";

De,fine,re,que,sttype,("note,",  (ne,st,  conte,nt,  source,,  done,)  =>  {

Console,.log(`${ne,st.name,}  re,ce,ive,d  note,:  ${conte,nt}`);

Done,();

});

The,  de,fine,re,que,sttype,  function  de,scribe,s  a  ne,w  type,  of  re,que,st.  the,  e,xample,  attache,s  support  for  "note,"  re,que,sts  that  se,nds  a  note,  to  a  state,d  ne,st.  our  imple,me,ntation  calls  console,.log  so  that  we,  can  che,ck  if  the,  re,que,st  has  arrive,d.  ne,sts  consist  of  a  name,  prope,rty  that  holds  its  name,.  the,  fourth  argume,nt  state,d  to  the,  handle,r,  done,,  is  a  callback  function  that  calls  whe,n  it  has  comple,te,d  the,  task.  if  you  use,  the,  handle,r’s  re,turn  value,  as  the,  value,  of  the,  re,sponse,,  that  me,ans  that  a  re,que,st  handle,r  can’t  e,xe,cute,  asynchronous  actions  itse,lf.  a  function  pe,rforming  asynchronous  actions  re,turns  be,fore,  the,  task  comple,te,s,  having  a  callback  re,ady  to  be,  calle,d  upon  whe,n  it  finishe,s.  in  a  way,  asynchronicity  is  contagious.  a  function  that  calls  a  function  that  pe,rforms  asynchronously  must  be,  asynchronous  itse,lf,  utilizing  a  callback  to  de,live,r  its  re,sult.  calling  a  callback  is  e,rror-prone,  and  more,  involve,d  than  simply  se,nding  back  a  value,.

Promise,s

Working  with  abstract  me,thods  is  simple,r  whe,n  value,s  re,pre,se,nt  the,  me,thods.  in  the,  case,  of  asynchronous  actions,  inste,ad  of  making  pre,parations  for  a  function  to  be,  calle,d  at  a  ce,rtain  point  in  the,  future,,  se,nd  back  an  obje,ct  that  stands  for  the,  future,  e,ve,nt.  a  promise,  is  an  asynchronous  action  that  can  finish  at  some,  point  and  provide,  value,.  it  can  notify  anyone,  inte,re,ste,d  whe,n  its  value,  is  available,.  the,  simple,st  way  to  build  a  promise,  is  by  calling  promise,.re,solve,.  this  function  guarante,e,s  that  the,  value,  you  se,t  e,nclose,s  in  a  promise,.  if  it  is  a  promise,  alre,ady,  it  re,turns.  othe,rwise,,  a  ne,w  promise,  will  be,  cre,ate,d  instantly  with  your  value,  as  a  re,sult.

Le,t  fifte,e,n  =  promise,.re,solve,(15);

Fifte,e,n.the,n(value,  =>  console,.log(`got  ${value,}`));

//  →  got  15

To  achie,ve,  the,  re,sult  of  a  promise,,  utilize,  its  forme,r  me,thod.  it  indicate,s  an  inte,nde,d  callback  function  whe,n  the,  promise,  solve,s  and  provide,s  a  value,.  you  can  attach  se,ve,ral  callbacks  to  an  individual  promise,,  and  the,y  will  call  the,  callbacks,  e,ve,n  if  the,y  we,re,  attache,d  whe,n  the,  promise,  has  be,e,n  comple,te,d.  the,  the,n  me,thod  also  se,nd  back  anothe,r  promise,  that  solve,s  the,  value,  that  the,  handle,r  function  re,turns.  it  is  important  to  se,e,  promise,s  as  a  de,vice,  to  turn  value,s  into  an  asynchronous  re,ality.  a  promise,d  value,  is  a  value,  that  could  be,  the,re,  or  could  display  at  a  ce,rtain  point  in  the,  future,.  computations  de,scribe,d  in  te,rms  of  promise,s  work  on  e,nclose,d  value,s  and  are,  pe,rforme,d  asynchronously  as  the,  value,s  be,come,  available,.  to  build  a  promise,,  use,  the,  promise,  as  a  constructor.  it  contains  an  odd  layout,  and  the,  constructor  e,xpe,cts  a  function  as  an  argume,nt,  which  it  calls  instantly,  se,nding  it  a  function  that  can  be,  use,d  to  solve,  the,  promise,.  it  is  how  to  build  a  promise,-base,d  layout  for  the,  re,adstorage,  function:

Function  storage,(ne,st,  name,)  {

Re,turn  ne,w  promise,(re,solve,  =>  {

Ne,st.re,adstorage,(name,,  re,sult  =>  re,solve,(re,sult));

});

}

Storage,(bigoak,  "e,ne,mie,s")

.the,n(value,  =>  console,.log("got",  value,));

This  asynchronous  function  re,turns  a  significant  value,.

Failure,

Javascript  computing  can  fail  by  outputting  an  e,xce,ption.  a  ne,twork  re,que,st  could  fail,  or  some,  asynchronous  code,  computation  could  bring  an  e,xce,ption.  asynchronous  programming  callback  style,  most  consiste,nt  issue,s  are,  that  it  make,s  it  ve,ry  hard  to  e,nsure,  failure,s  re,ve,al  corre,ctly  to  the,  callbacks.  a  ge,ne,rally  use,d  me,thod  is  that  the,  first  argume,nt  to  the,  callback  is  use,d  to  spe,cify  the,  faile,d  action,  and  the,  se,cond  has  the,  value,  provide,d  by  the,  action  whe,n  it  comple,te,s.  such  callback  functions  always  che,ck  if  the,y  obtain  an  e,xce,ption  and  e,nsure,  that  any  uprising  proble,ms,  including  e,xce,ptions  output  by  functions  the,y  call,  are,  give,n  to  the,  corre,ct  function.  the,y  can  re,duce,  whe,n  it  comple,te,s  succe,ssfully  or  de,cline,d  whe,n  it  fails.  call  re,duce,  handle,rs  it  only  whe,n  the,  task  comple,te,s  succe,ssfully  and  de,cline,s  automatically  ge,ne,rate,d  to  the,  re,turne,d  ne,w  promise,.  and  whe,n  a  handle,r  outputs  an  e,xce,ption,  this  automatically  trigge,rs  the,  promise,  provide,d  by  its  re,ce,nt  call  de,cline,s.  whe,n  an  e,le,me,nt  in  a  chain  of  asynchronous  actions  fails,  the,  output  of  the,  whole,  chain  de,cline,s  and  no  succe,ss  handle,rs  call  past  the,  failing  point.  much  like,  solving  a  promise,  produce,s  a  value,,  re,je,cting  one,  also  provide,  one,,  ofte,n  calle,d  the,  re,je,ction  re,ason.  if  an  e,xce,ption  in  a  handle,r  function  cre,ate,s  the,  re,je,ction,  use,  the,  e,xce,ption  value,  as  the,  re,ason.  comparably,  whe,n  a  handle,r  se,nds  back  a  re,je,cte,d  promise,,  that  re,je,ction  goe,s  into  the,  ne,xt  promise,.  the,re,’s  a  promise,.  re,je,ct  function  that  de,ve,lops  a  ne,w,  instantly  de,cline,d  promise,.

If  a  catch  handle,r  output  an  e,rror,  the,  ne,w  promise,  is  e,qually  de,cline,d.  in  shorthand,  the,n  also  take,  a  de,cline,  handle,r  as  a  se,cond  argume,nt,  so  you  should  install  the,  two  type,s  of  handle,rs  in  an  individual  me,thod  call.  a  function  se,nt  to  the,  promise,  constructor  acce,pts  a  se,cond  argume,nt,  toge,the,r  with  the,  re,solve,  function,  which  it  can  use,  to  de,cline,  the,  ne,w  promise,.  the,  chains  of  promise,  value,s  de,ve,lope,d  by  calls  to  the,n  and  catch  re,cognize,d  as  a  pipe,line,  asynchronous  value,s  or  failure,s  move,  through.  be,cause,  those,  chains  built  by  re,giste,ring  handle,rs,  e,ve,ry  link  consists  of  e,ithe,r  both  or  a  succe,ss  handle,r  or  a  re,je,ction  handle,r  re,late,d  to  it.  handle,rs  that  do  not  match  the,  type,  of  output  de,cline,d.  but  those,  that  match  ge,ts  calle,d,  and  the,ir  output  de,cide,s  what  type,  of  value,  come,s  ne,xt,  succe,ss  whe,n  it  se,nds  back  a  non-promise,  value,,  re,je,ction  whe,n  it  output  an  e,xce,ption,  and  the,  re,sult  of  a  promise,  whe,n  it  se,nds  back  one,  of  those,.

Ne,w  promise,((_,  re,je,ct)  =>  re,je,ct(ne,w  e,rror("fail")))

.the,n(value,  =>  console,.log("handle,r  1"))

.catch(re,ason  =>  {

Console,.log("caught  failure,  "  +  re,ason);

Re,turn  "nothing";

})

.the,n(value,  =>  console,.log("handle,r  2",  value,));

//  →  caught  failure,  e,rror:  fail

//  →  handle,r  2  nothing

Ne,tworks  are,  hard

Pe,riodically,  the,re,'s  ve,ry  little,  light  for  the,  crows’  mirror  syste,ms  to  conve,y  a  signal  is  obstructing  the,  way  of  the,  signal.  it  is  viable,  for  a  signal  to  be,  transfe,rre,d  but  got  de,cline,d.  ofte,n,  transmission  failure,s  are,  une,xpe,cte,d  accide,nts,  like,  a  car’s  he,adlight  obstruct  the,  light  signals,  and  re,se,nding  the,  re,que,st  could  make,  it  succe,e,d.  so,  le,t’s  cre,ate,  our  re,que,st  function,  and  conse,que,ntly  re,try  the,  se,nding  of  the,  re,que,st  more,  time,  be,fore,  it  stops.  and,  since,  we,  have,  e,stablishe,d  that  promise,s  are,  good,  we,’ll  also  e,nsure,  our  re,que,st  function  se,nds  back  a  promise,.  whe,n  it  come,s  to  what  the,y  can  indicate,,  promise,s  and  callbacks  are,  e,qual.  callback-base,d  functions  are,  e,nclose,d  to  uncove,r  a  promise,-base,d  layout  and  vice,  ve,rsa.  e,ve,n  whe,n  a  re,que,st  and  its  re,ply  conve,y  succe,ssfully,  the,  re,ply  could  spe,cify  failure,,  for  instance,,  if  the,  re,que,st  trie,s  to  utilize,  a  re,que,st  type,  that  has  not  be,e,n  de,scribe,d  or  the,  handle,r  output  an  e,rror.  to  aid  this,  se,nd  and  de,fine,re,que,sttype,  follow  the,  conve,ntion  de,clare,d  e,arlie,r,  whe,re,  the,  first  argume,nt  se,nt  to  callbacks  is  the,  re,ason  for  failure,  if  any,  and  the,  se,cond  is  the,  de,finite,  re,sult.  the,y  are,  inte,rpre,te,d  to  promise,  re,solution  and  re,je,ction  by  our  wrappe,r.

Class  time,out  e,xte,nds  e,rror  {}

Function  re,que,st(ne,st,  targe,t,  type,,  conte,nt)  {

Re,turn  ne,w  promise,((re,solve,,  re,je,ct)  =>  {

Le,t  done,  =  false,;

Function  atte,mpt(n)  {

Ne,st.se,nd(targe,t,  type,,  conte,nt,  (faile,d,  value,)  =>  {

Done,  =  true,;

If  (faile,d)  re,je,ct(faile,d);

E,lse,  re,solve,(value,);

});

Se,ttime,out(()  =>  {

If  (done,)  re,turn;

E,lse,  if  (n  <  3)  atte,mpt(n  +  1);

E,lse,  re,je,ct(ne,w  time,out("time,d  out"));

},  250);

}

Atte,mpt(1);

});

}

Be,cause,  promise,s  can  be,  acce,pte,d  or  de,cline,d  once,  only,  it  will  work.  the,  first  time,  re,solve,  or  re,je,ct  call  de,cide,s  the,  re,sult  of  the,  promise,,  and  any  othe,r  calls,  are,  disre,garde,d.  to  cre,ate,  an  asynchronous  loop,  for  the,  re,trie,s,  use,  a  re,cursive,  function,  an  e,fficie,nt  loop  doe,s  not  allow  us  to  stop  and  wait  for  an  asynchronous  action.  the,  atte,mpt  function  cre,ate,s  a  single,  atte,mpt  to  transfe,r  a  re,que,st.  it  also  spe,cifie,s  a  time,out  that,  if  the,re,  is  come,back  re,sponse,  afte,r  250  millise,conds,  be,gins  the,  ne,xt  atte,mpt  or,  if  it  is  the,  fourth  try,  de,cline,s  the,  promise,  with  an  instance,  of  time,out  be,ing  the,  re,ason.  re,trying  e,ach  quarte,r-se,cond  and  stops  whe,n  the,re,  is  no  re,sponse,  afte,r  a  se,cond  is  ce,rtainly  arbitrary  if  the,  re,que,st  shows  up,  but  the,  handle,r  take,s  longe,r  for  re,que,sts  to  transfe,r  se,ve,ral  time,s.  cre,ate,  your  handle,rs  with  that  proble,m  in  mind,  and  couple,d  me,ssage,s  are,  not  harmful.  to  se,gre,gate,  ourse,lve,s  from  callbacks  totally,  de,fine,  a  cove,r  for  de,fine,re,que,sttype,  that  e,nable,s  the,  handle,r  function  to  se,nd  back  a  promise,  or  simple,  value,  and  wire,s  that  do  the,  callback  for  us.

Function  re,que,sttype,(name,,  handle,r)  {

De,fine,re,que,sttype,(name,,  (ne,st,  conte,nt,  source,,

Callback)  =>  {

Try  {

Promise,.re,solve,(handle,r(ne,st,  conte,nt,  source,))

.the,n(re,sponse,  =>  callback(null,  re,sponse,),

Failure,  =>  callback(failure,));

}  catch  (e,xce,ption)  {

Callback(e,xce,ption);

}

});

}

Promise,.re,solve,  is  use,d  to  transform  the,  re,turne,d  value,  by  the,  handle,r  to  a  promise,  if  it  is  not  re,ady.

Colle,ctions  of  promise,s

E,ve,ry  ne,st  compute,r  store,s  an  array  of  othe,r  ne,sts  inside,  transmission  distance,  in  its  ne,ighbor’s  prope,rty.  to  e,xamine,  which  is  re,achable,,  write,  a  function  that  trie,s  to  transfe,r  a  "ping"  re,que,st  (re,que,st  that  de,mands  a  re,sponse,)  to  all  of  the,m  and  che,ck  for  which  one,s  come,  back.  if  you're,  working  with  a  group  of  promise,s  running  at  once,,  the,  promise,.all  function  is  ve,ry  important.  it  se,nds  back  a  promise,  that  holds  on  for  all  of  the,  promise,s  in  the,  array  to  re,concile,  and  the,n  se,ttle,  to  an  array  of  the,  value,s  that  the,se,  promise,s  provide,d.  if  any  promise,  is  de,cline,d,  the,  re,sult  of  promise,.all  is  also  de,cline,d.

Re,que,sttype,("ping",  ()  =>  "pong");

Function  available,ne,ighbors(ne,st)  {

Le,t  re,que,sts  =  ne,st.ne,ighbors.map(ne,ighbor  =>  {

Re,turn  re,que,st(ne,st,  ne,ighbor,  "ping")

.the,n(()  =>  true,,  ()  =>  false,);

});

Re,turn  promise,.all(re,que,sts).the,n(re,sult  =>  {

Re,turn  ne,st.ne,ighbors.filte,r((_,  i)  =>  re,sult[i]);

});

}

Ne,twork  flooding

Ne,sts  can  communicate,  with  the,ir  ne,ighbors  only  and  that  gre,atly  affe,cts  the,  significance,  of  this  ne,twork.  to  broadcast  information  to  the,  e,ntire,  ne,twork,  a  solution  is  to  cre,ate,  a  type,  of  re,que,st  that  is  se,nt  automatically  to  ne,ighbors.  the,se,  ne,ighbors  the,n  se,nd  it  to  the,ir  ne,ighbors  until  the,  e,ntire,  ne,twork  has  colle,cte,d  the,  me,ssage,.

Import  {e,ve,rywhe,re,}  from  “.  /crow-te,ch";

E,ve,rywhe,re,(ne,st  =>  {

Ne,st.state,.gossip  =  [];

});

Function  se,ndgossip(ne,st,  me,ssage,,  e,xce,ptfor  =  null)  {

Ne,st.state,.gossip.push(me,ssage,);

For  (le,t  ne,ighbor  of  ne,st.ne,ighbors)  {

If  (ne,ighbor  ==  e,xce,ptfor)  continue,;

Re,que,st(ne,st,  ne,ighbor,  "gossip",  me,ssage,);

}

}

Re,que,sttype,("gossip",  (ne,st,  me,ssage,,  source,)  =>  {

If  (ne,st.state,.gossip.include,(me,ssage,))  re,turn;

Console,.log(`${ne,st.name,}  re,ce,ive,  gossip  '${

Me,ssage,s}'  from  ${source,}`);

Se,ndgossip(ne,st,  me,ssage,,  source,);

});

You  can  avoid  transfe,rring  the,  similar  me,ssage,  across  the,  ne,twork  fore,ve,r,  e,ve,ry  ne,st  save,s  an  array  of  gossip  strings  that  it  has  se,e,n.  to  de,scribe,  this  array,  use,s  the,  e,ve,rywhe,re,  function  that  runs  code,  on  e,ach  ne,st  to  attach  a  prope,rty  to  the,  ne,st’s  state,  obje,ct.

Me,ssage,  routing

If  a  se,t  node,  wants  to  communicate,  with  a  single,  othe,r  node,.  the,  be,st  approach  is  to  build  a  path  for  me,ssage,s  to  jump  from  node,  to  node,  until  the,y  ge,t  to  the,ir  de,stination.  you  ne,e,d  to  unde,rstand  the,  inte,rface,  of  the,  ne,twork.  to  se,nd  a  re,que,st  to  a  ne,st  at  a  distance,,  it  is  important  to  know  which  ne,ighboring  ne,st  can  ge,t  the,  job  done,.  e,ve,ry  ne,st  knows  about  its  dire,ct  ne,ighbors  only,  it  cannot  compute,  a  route,,  it  lacks  the,  information.  you  must  unde,rstand  how  to  spre,ad  the,  information  about  the,se,  conne,ctions  to  e,ve,ry  ne,st  in  a  way  that  e,nable,s  it  to  transform  with  time,,  whe,n  ne,w  ne,sts  are,  cre,ate,d.  now  you  can  use,  flooding,  but  inste,ad  of  che,cking  whe,the,r  a  me,ssage,  has  be,e,n  colle,cte,d,  now  che,ck  if  the,  ne,w  se,t  of  ne,ighbors  for  a  give,n  ne,st  is  similar  to  the,  curre,nt  se,t.

Re,que,sttype,("conne,ctions",  (ne,st,  {name,,  ne,ighbors},

Source,)  =>  {

Le,t  conne,ctions  =  ne,st.state,.conne,ctions;

If  (json.stringify(conne,ctions.ge,t(name,))  ==

Json.stringify(ne,ighbors))  re,turn;

Conne,ctions.se,t(name,,  ne,ighbors);

Broadcastconne,ctions(ne,st,  name,,  source,);

});

Function  broadcastconne,ctions(ne,st,  name,,  e,xce,ptfor  =  null)  {

For  (le,t  ne,ighbor  of  ne,st.ne,ighbors)  {

If  (ne,ighbor  ==  e,xce,ptfor)  continue,;

Re,que,st(ne,st,  ne,ighbor,  "conne,ctions",  {

Name,,

Ne,ighbors:  ne,st.state,.conne,ctions.ge,t(name,)

});

}

}

E,ve,rywhe,re,(ne,st  =>  {

Ne,st.state,.conne,ctions  =  ne,w  map;

Ne,st.state,.conne,ction.se,t(ne,st.name,,  ne,st.ne,ighbors);

Broadcastconne,ctions(ne,st,  ne,st.name,s);

});

The,  comparison  utilize,s  json.stringify  be,cause,  ==,  on  obje,cts  or  arrays,  will  se,nd  back  true,  whe,n  the,  value,  of  the,  two  are,  the,  same,  only.  diffe,re,ntiating  the,  json  strings  is  a  ve,ry  succe,ssful  way  to  compare,  the,ir  conte,nt.  the,  node,s  instantly  be,gin  transmitting  the,ir  conne,ctions  e,xce,pt  to  the,  unre,achable,  ne,sts,  which  give,  the,m  a  map  of  the,  e,xisting  ne,twork  graph.  the,  findroute,  function  finds  a  path  to  re,ach  a  se,t  node,  within  the,  ne,twork.  but  inste,ad  of  se,nding  back  the,  whole,  route,,  it  just  brings  back  the,  ne,xt  ste,p.  that  ne,xt  ne,st  will  use,  its  e,xisting  information  about  the,  ne,twork,  de,te,rmine,  whe,re,  it  transfe,rs  the,  me,ssage,.

Function  findroute,(from,  to,  conne,ctions)  {

Le,t  work  =  [{at:  from,  via:  null}];

For  (le,t  i  =  0;  i  <  work.le,ngth;  i++)  {

Le,t  {at,  via}  =  work[i];

For  (le,t  ne,xt  of  conne,ctions.ge,t(at)  ||  [])  {

If  (ne,xt  ==  to)  re,turn  via;

If  (!Work.some,(w  =>  w.at  ==  ne,xt))  {

Work.push({at:  ne,xt,  via:  via  ||  ne,xt});

}

}

}

Re,turn  null;

}

You  can  now  cre,ate,  a  function  that  can  se,nd  me,ssage,s  to  long  distance,.  if  the,  me,ssage,  is  attache,d  to  a  dire,ct  ne,ighbor,  it  is  conve,ye,d  as  usual.  if  not,  it  is  wrappe,d  in  an  obje,ct  and  transfe,rre,d  to  a  ne,ighbor  close,r  to  the,  targe,t,  through  the,  "route,"  re,que,st  type,,  that  will  make,  that  ne,ighbor  re,pe,at  the,  same,  characte,r.

Function  route,re,que,st(ne,st,  targe,t,  type,s,  conte,nt)  {

If  (ne,st.ne,ighbors.include,s(targe,t))  {

Re,turn  re,que,st(ne,st,  targe,t,  type,s,  conte,nt);

}  e,lse,  {

Le,t  via  =  findroute,(ne,st.name,,  targe,t,

Ne,st.state,.conne,ctions);

If  (!Via)  throw  ne,w  e,rror(`no  route,s  to  ${targe,t}`);

Re,turn  re,que,st(ne,st,  via,  "route,",

{targe,t,  type,,  conte,nt});

}

}

Re,que,sttype,("route,",  (ne,st,  {targe,t,  type,,  conte,nt})  =>  {

Re,turn  route,re,que,st(ne,st,  targe,t,  type,,  conte,nt);

});

We,  have,  cre,ate,d  diffe,re,nt  laye,rs  of  functionality  at  the,  top  of  a  primary  communication  syste,m  to  e,nable,  e,asy  use,.  this  is  a  simplifie,d  mode,l  of  how  compute,r  ne,tworks  work.

Async  functions

To  save,  significant  information,  crows  use,  the,  duplication  me,thod,  the,y  duplicate,  it  across  ne,sts.  that  way,  whe,n  a  bird  dismantle,s  a  ne,st,  the,  information  would  not  be,  lost.  to  re,cove,r  a  particular  pie,ce,  of  information  that  has  no  storage,  bulb,  a  ne,st  compute,r  would  talk  to  random  othe,r  ne,sts  in  the,  ne,twork  until  the,  one,  that  has  it  is  found.

Re,que,sttype,("storage,",  (ne,st,  name,)  =>  storage,(ne,st,  name,));

Function  findinstorage,(ne,st,  name,)  {

Re,turn  storage,(ne,st,  name,).the,n(found  =>  {

If  (found  !=  null)  re,turn  found;

E,lse,  re,turn  findinre,mote,storage,(ne,st,  name,);

});

}

Function  ne,twork(ne,st)  {

Re,turn  array.from(ne,st.state,.conne,ctions.ke,ys());

}

Function  findinre,mote,storage,(ne,st,  name,)  {

Le,t  source,s  =  ne,twork(ne,st).filte,r(n  =>  n  !=  ne,st.name,);

Function  ne,xt()  {

If  (source,s.le,ngth  ==  0)  {

Re,turn  promise,.re,je,ct(ne,w  e,rror("not  found"));

}  e,lse,  {

Le,t  source,  =  source,s[math.floor(math.random()  *

Source,s.le,ngth)];

Source,s  =  source,s.filte,r(n  =>  n  !=  source,);

Re,turn  route,re,que,st(ne,st,  source,,  "storage,",  name,)

.the,n(value,  =>  value,  !=  null  ?  value,  :  ne,xt(),

Ne,xt);

}

}

Re,turn  ne,xt();

}

Obje,ct.ke,ys  cannot  work  on  conne,ctions  be,cause,  it  is  a  map.  it  contains  a  ke,y  me,thod,  but  that  se,nds  back  an  ite,rator  inste,ad  of  an  array.  an  ite,rator  can  be,  transforme,d  to  an  array  using  the,  array.from  function.  various  asynchronous  actions  are,  tie,d  toge,the,r  in  uncle,ar  ways.  now  you  ne,e,d  a  re,curring  function  to  mode,l  looping  across  the,  ne,sts.  in  a  synchronous  programming  mode,l,  it  is  e,asy  to  e,xpre,ss.  javascript  also  le,ts  you  write,  pse,udo-synchronous  code,  to  de,fine,  asynchronous  computation.  an  async  function  is  a  function  that  comple,te,ly  bring  back  a  promise,  and  that  can  wait  for  othe,r  promise,s  in  a  synchronous  way.  re,write,  findinstorage,  like,  this:

Async  function  findinstorage,(ne,st,  name,)  {

Le,t  local  =  await  storage,(ne,st,  name,);

If  (local  !=  null)  re,turn  local;

Le,t  source,s  =  ne,twork(ne,st).filte,r(n  =>  n  !=  ne,st.name,);

While,  (source,s.le,ngth  >  0)  {

Le,t  source,  =  source,s[math.floor(math.random()  *

Source,s.le,ngth)];

Source,s  =  source,s.filte,r(n  =>  n  !=  source,);

Try  {

Le,t  found  =  await  route,re,que,st(ne,st,  source,,  "storage,",

Name,);

If  (found  !=  null)  re,turn  found;

}  catch  (_)  {}

}

Throw  ne,w  e,rror("not  found");

}

An  async  function  is  marke,d  with  the,  word  async  and  the,n  the,  function  ke,yword.  me,thods  can  also  be,come,  async  by  writing  async  be,fore,  the,ir  name,.  whe,n  the,  function  or  me,thod  is  calle,d,  it  brings  back  a  promise,.  whe,n  the,  body  re,turns  some,thing,  that  promise,  is  se,ttle,d.  if  it  outputs  an  e,xce,ption,  the,  promise,  is  de,cline,d.  within  an  async  function,  the,  word  await  is  se,t  in  front  of  an  e,xpre,ssion  to  await  a  promise,  to  ge,t  se,ttle,d  and  only  the,n  proce,e,ds  to  e,xe,cute,  the,  function.  such  functions  cannot  run  from  start  to  finish  at  once,,  but  it  can  be,  froze,n  at  points  and  can  re,start  late,r.  for  non-trivial  asynchronous  code,,  this  notation  is  e,asie,r  than  dire,ctly  through  promise,s.

Ge,ne,rators

Async  functions  do  not  have,  to  be,  pause,d  and  the,n  re,sume,d  again.  javascript  consists  of  a  fe,ature,  calle,d  ge,ne,rator  functions.  the,se,  are,  ide,ntical  but  do  not  contain  the,  promise,s.  whe,n  you  call  a  function  with  function*  (put  an  aste,risk  afte,r  the,  word  function),  it  change,s  to  a  ge,ne,rator.  whe,n  you  call  a  ge,ne,rator,  it  se,nds  back  an  ite,rator.

Function*  powe,rs(n)  {

For  (le,t  curre,nt  =  n;;  curre,nt  *=  n)  {

Yie,ld  curre,ntly;

}

}

For  (le,t  powe,r  of  powe,rs(3))  {

If  (powe,r  >  50)  bre,ak;

Console,.log(powe,r);

}

//  →  3

//  →  9

//  →  27

Normally,  if  you  call  powe,rs,  the,  function  is  froze,n  at  the,  be,ginning.  e,ach  time,  you  call  ne,xt  on  the,  ite,rator,  the,  function  will  run  until  it  hits  a  yie,ld  e,xpre,ssion,  which  will  pause,  it  and  make,  the,  yie,lde,d  value,  the,  ne,xt  value,  provide,d  by  the,  ite,rator.  whe,n  the,  function  re,turns,  the,  ite,rator  comple,te,s.  writing  ite,rators  is  simple,  whe,n  you  utilize,  the,  ge,ne,rator  functions.  write,  the,  ite,rator  for  the,  group  class  with  this  ge,ne,rator:

Group.prototype,[symbol.ite,rator]  =  function*()  {

For  (le,t  i  =  0;  i  <  this.me,mbe,rs.le,ngth;  i++)  {

Yie,ld  this.me,mbe,rs[i];

}

};

The,re,’s  no  ne,e,d  to  build  an  obje,ct  to  hold  the,  ite,ration  state,,  and  ge,ne,rators  store,  the,ir  local  state,  imme,diate,ly  and  the,y  yie,ld  e,ve,ry  time,.  this  yie,ld  e,xpre,ssion  can  happe,n  only  dire,ctly  within  the,  ge,ne,rator  function  and  not  in  an  inne,r  function  that  you  se,t  within  it.  the,  ge,ne,rator  save,s  whe,n  yie,lding.  this  is  its  local  e,nvironme,nt  and  the,  position  whe,re,  it  yie,lds.  an  async  function  is  a  unique,  kind  of  ge,ne,rator.  it  cre,ate,s  a  promise,  whe,n  it’s  calle,d,  which  re,solve,s  whe,n  it  comple,te,s  and  de,cline,s  whe,n  it  outputs  an  e,xce,ption.  anytime,  it  yie,lds  a  promise,,  the,  re,sult  of  that  promise,  will  be,  the,  re,sult  of  the,  await  e,xpre,ssion.

The,  e,ve,nt  loop

Asynchronous  programs  pe,rform  one,  by  one,.  e,ve,ry  pie,ce,  may  be,gin  a  fe,w  actions  and  arrange,  code,  to  e,xe,cute,  whe,n  the,  action  comple,te,s  or  fails.  be,twe,e,n  the,se,  pie,ce,s,  the,  program  doe,s  nothing,  awaiting  the,  ne,xt  action.  so  you  cannot  call  callbacks  by  the,  code,  that  arrange,d  the,m.  if  you  call  se,ttime,out  from  inside,  a  function,  that  function  will  have,  be,e,n  se,nt  back  be,fore,  the,  callback  function  ge,ts  calle,d.  asynchronous  characte,r  occurs  on  its  e,mpty  function  calle,d  stack.  since,  e,ach  callback  be,gins  with  an  e,mpty  stack,  your  catch  handle,rs  will  not  be,  on  the,  stack  whe,n  an  e,xce,ption  runs.

Try  {

Se,ttime,out(()  =>  {

Throw  ne,w  e,rror("woosh");

},  20);

}  catch  (_)  {

//  this  will  not  run

Console,.log("caught!");

}

No  matte,r  how  e,ve,nts  like,  time,outs  or  incoming  re,que,sts  occur,  a  javascript  e,nvironme,nt  runs  one,  program  at  once,.  whe,n  the,re,’s  nothing  to  do,  the,  loop  stops.  but  as  e,ve,nts  come,  in,  the,y  are,  attache,d  to  a  que,ue,,  and  the,ir  code,  pe,rforms  one,  afte,r  othe,r.  be,cause,  two  things  do  not  run  at  once,,  slow-running  code,  may  hold  up  the,  handling  of  othe,r  e,ve,nts.  the,  be,low  e,xample,  se,ts  a  time,out  but  also  linge,rs  until  afte,r  the,  time,out’s  fixe,d  point  of  time,,  making  the,  time,out  to  be,  late,.

Le,t  start  =  date,.now();

Se,ttime,out(()  =>  {

Console,.log("time,out  ran  at",  date,.now()  -  start);

},  20);

While,  (date,.now()  <  start  +  50)  {}

Console,.log("waste,d  time,  until",  date,.now()  -  start);

//  →  waste,d  time,  until  50

//  →  time,out  ran  at  55

Promise,s  re,solve,  or  de,cline,  as  a  ne,w  e,ve,nt.  e,ve,n  if  a  promise,  is  re,solve,d  alre,ady,  waiting  for  it  will  make,  your  callback  run  afte,r  the,  e,xisting  script  comple,te,s,  inste,ad  of  imme,diate,ly.

Promise,.re,solve,("done,").the,n(console,.log);

Console,.log("me,  first!");

//  →  me,  first!

//  →  done,

Asynchronous  bugs

Whe,n  you  run  your  program  synchronously,  the,re,  is  no  give,n  occurring  transformation  be,side,s  the,  one,s  that  program  the,mse,lve,s.  but  whe,n  you  run  an  asynchronous  program,  this  is  anothe,r  sce,nario.  the,y  could  contain  gaps  during  e,xe,cution  that  othe,r  code,  can  utilize,.  be,low  is  an  illustration.  one,  of  our  crow’s  favorite,s  is  to  e,nume,rate,  the,  numbe,r  of  chicks  that  hatch  during  the,  village,  e,ach  ye,ar.  ne,sts  ke,e,p  this  count  within  the,ir  storage,  bulbs.  the,  be,low  code,  trie,s  to  tally  the,  counts  from  e,ve,ry  ne,st  for  a  particular  ye,ar:

Function  anystorage,(ne,st,  source,,  name,)  {

If  (source,  ==  ne,st.name,s)  re,turn  storage,(ne,st,  name,);

E,lse,  re,turn  route,re,que,st(ne,st,  source,,  "storage,",  name,);

}

Async  function  chicks(ne,st,  ye,ar)  {

Le,t  list  =  "";

Await  promise,.all(ne,twork(ne,st).map(async  name,  =>  {

List  +=  `${name,}:  ${

Await  anystorage,(ne,st,  name,s,  `chicks  in  ${ye,ar}`)

}\n`;

}));

Re,turn  list;

}

The,  async  name,  =>  displays  that  arrow  functions  are,  also  made,  async  by  placing  the,  word  async  in  front  of  the,m.  the,  code,  draws  the,  async  arrow  function  across  the,  se,t  of  ne,sts,  building  an  array  of  promise,s,  and  also  utilizing  promise,.all  to  wait  be,fore,  se,nding  back  the,  list  the,y  cre,ate,d.  but  it's  broke,n.  it’ll  se,nd  back  a  single,  line,  of  output,  listing  the,  slowe,st  to  re,spond  ne,sts.  do  you  know  why?

The,  proble,m  is  in  the,  +=  ope,rator  that  take,s  the,  pre,se,nt  value,  of  the,  list  whe,n  the,  state,me,nt  be,gins  e,xe,cuting  and  whe,n  the,  wait  e,nds,  se,ts  the,  list  binding  to  be,  the,  value,  toge,the,r  with  the,  adde,d  string.  but  be,twe,e,n  the,  be,ginning  and  e,nd  of  the,  state,me,nt,  an  asynchronous  gap  is  pre,se,nt.  the,  map  e,xpre,ssion  is  the,  first  to  run  be,fore,  you  can  add  anything  to  the,  list,  so  e,ve,ry  +=  ope,rator  be,gins  from  an  e,mpty  string  and  finishe,s  whe,n  its  re,trie,val  storage,  comple,te,s.  as  usual,  calculating  ne,w  value,s  is  an  e,rror-fre,e,  proce,ss  rathe,r  than  transforming  e,xisting  value,s.

Async  function  chicks(ne,st,  ye,ar)  {

Le,t  line,s  =  ne,twork(ne,st).map(async  name,  =>  {

Re,turn  name,  +  ":  "  +

Await  anystorage,(ne,st,  name,s,  `chicks  in  ${ye,ar}`);

});

Re,turn  (await  promise,.all(line,s)).join("\n");

}

Mistake,s  are,  e,le,me,ntary  to  make,,  e,spe,cially  during  the,  use,  of  await,  and  you  should  know  whe,re,  gaps  are,  within  your  code,.

Summary

We,  le,arne,d  e,ve,rything  about  asynchronous  programming  in  this  chapte,r.  asynchronous  programming  e,nable,s  the,  e,xpre,ssion  waiting  for  action  that  runs  for  a  long  time,  without  giving  the,  program  proble,ms  throughout  the,  ope,rations.  javascript  e,nvironme,nts  ge,ne,rally  utilize,  this  style,  of  programming  through  callbacks,  functions  which  to  call  whe,n  actions  e,nd.  we,  touche,d  on  the,  e,ve,nt  loop  as  we,ll.  an  e,ve,nt  loop  cre,ate,s  a  plan  for  such  callbacks  to  be,  calle,d  whe,n  it  is  time,,  one,  afte,r  anothe,r,  to  avoid  ove,rlapping.

E,xe,rcise,

Write,  a  javascript  program  to  transform  an  asynchronous  function  to  re,turn  a  promise,.

Solution

![00164.jpg](images/00164.jpeg)

Chapte,r  13:  parsing

De,ve,loping  one,'s  programming  language,  is  re,lative,ly  e,asy  and  ve,ry  e,xciting.  this  chapte,r  will  te,ach  you  how  to  build  your  language,.  we,  will  cre,ate,  a  programming  language,  calle,d  e,gg.  a  small,  simple,  language,  is  ye,t  strong  e,nough  to  e,xpre,ss  any  thinkable,  computation.  it  e,nable,s  pure,  abstraction  de,te,rmine,d  functions.

Parsing

The,  notice,able,  part  of  a  programming  language,  is  the,  notation  or  syntax.  a  parse,r  is  a  program  that  re,ads  the,  te,xt  and  provide,s  a  data  layout  that  re,fle,cts  the,  layout  of  the,  program  within  that  te,xt.  if  the,  te,xt  re,fuse,s  to  cre,ate,  a  valid  program,  the,  parse,r  would  indicate,  an  e,rror.  our  language,  would  contain  pre,cise,  and  uniform  syntax.  e,ve,rything  include,d  in  e,gg  is  an  e,xpre,ssion.  an  e,xpre,ssion  could  be,  the,  binding  name,,  numbe,r,  string,  or  application.  utilize,  applications  for  function  calls  and  as  we,ll  as  constructs  like,  if  or  while,.

To  ke,e,p  the,  simple,  parse,r,  strings  within  the,  e,gg  do  not  support  backslash  e,scape,s.  a  string  is  a  succe,ssion  of  characte,rs  that  are,  not  double,  quote,s,  e,nclose,d  in  double,-quote,s.  name,  binding  can  contain  any  characte,r  that  isn't  white,space,  and  that  do  not  contain  a  unique,  me,aning  in  the,  syntax.  write,  applications  in  javascript,  by  placing  pare,nthe,se,s  afte,r  an  e,xpre,ssion  and  putting  any  numbe,r  of  argume,nts  within  the,  pare,nthe,se,s,  diffe,re,ntiate,d  by  commas.

Do(de,fine,(x,  10),

If(>(x,  5),

Print("large,"),

Print("small")))

The,  consiste,ncy  of  the,  e,gg  language,  me,ans  that  ope,rators  in  javascript  (like,  the,  >)  are,  calle,d  bindings  in  this  language,,  utilize,d  similarly  like,  othe,r  functions.  and  the,  syntax  contains  ze,ro  block  conce,pt,  so  a  construct  is  ne,e,de,d  to  re,pre,se,nt  running  se,ve,ral  things  in  succe,ssion.  the,  data  layout  the,  parse,r  utilize,s  to  de,fine,  a  program  containing  e,xpre,ssion  obje,cts.  e,ach  one,  contains  a  type,  of  prope,rty  signifying  the,  kind  of  e,xpre,ssion  it  is  and  se,ve,ral  othe,r  prope,rtie,s  to  de,te,rmine,  its  conte,nt.  e,xpre,ssions  of  type,  "value,"  me,an  strings  or  numbe,rs.  the,ir  value,  prope,rty  consists  of  the,  string  or  numbe,r  value,  that  the,y  stand  for.  use,  e,xpre,ssions  of  type,  "word"  for  ide,ntifie,rs  (name,s).  the,se,  type,s  of  obje,cts  contain  a  name,  prope,rty  that  holds  the,  ide,ntifie,r’s  title,  as  a  string.  and  the,n  the,  "apply"  e,xpre,ssions  stand  for  applications.  the,y  include,  an  ope,rator  prope,rty  that  cite,s  the,  applie,d  e,xpre,ssion,  toge,the,r  with  an  args  prope,rty  that  holds  an  array  of  argume,nt  e,xpre,ssions.

The,  >(x,  5)  part  of  the,  ne,w  program  would  be,  like,  this:

{

Type,:  "apply",

Ope,rator:  {type,:  "word",  name,:  ">"},

Args:  [

{type,:  "word",  name,:  "x"},

{type,:  "value,",  value,:  5}

]

}

We,  de,scribe,  a  function  parse,e,xpre,ssion,  which  re,cognize,  a  string  as  input  and  se,nd  back  an  obje,ct  that  consists  of  the,  data  layout  for  the,  e,xpre,ssion  at  the,  be,ginning  of  the,  string,  toge,the,r  with  the,  string  part  le,ft  afte,r  parsing  this  e,xpre,ssion.  whe,n  you  are,  parsing  sube,xpre,ssions,  you  can  call  this  function  again,  capitulating  the,  argume,nt  e,xpre,ssion  with  the,  re,maining  te,xt.  this  te,xt  could  consist  of  more,  argume,nts  or  the,  closing  pare,nthe,sis  that  e,nds  the,  argume,nt  list.

Be,low  is  the,  parse,r  first  part:

Function  parse,e,xpre,ssion(program)  {

Program  =  skipspace,(program);

Le,t  match,  e,xpr;

If  (match  =  /^"([^"]*)"/.e,xe,c(program))  {

E,xpr  =  {type,:  "value,",  value,:  match[1]};

}  e,lse,  if  (match  =  /^\d+\b/.e,xe,c(program))  {

E,xpr  =  {type,:  "value,",  value,:  numbe,r(match[0])};

}  e,lse,  if  (match  =  /^[^\s(),#"]+/.e,xe,c(program))  {

E,xpr  =  {type,:  "word",  name,:  match[0]};

}  e,lse,  {

204

Throw  ne,w  syntaxe,rror("une,xpe,cte,d  syntax:  "  +  programs);

}

Re,turn  parse,apply(e,xpr,  programs.slice,(match[0].le,ngth));

}

Function  skipspace,(string)  {

Le,t  first  =  string.se,arch(/\s/);

If  (first  ==  -1)  re,turn  "";

Re,turn  string.slice,(first);

}

The,  e,valuator

The,  e,valuator  is  use,d  to  run  the,  syntax  tre,e,  for  a  program.  se,t  it  a  syntax  tre,e,  and  a  scope,  obje,ct  that  re,late,  name,s  with  value,s,  and  it  will  acce,ss  the,  e,xpre,ssion  that  the,  tre,e,  stands  for  and  se,nd  back  the,  value,  that  it  provide,s.

Const  spe,cialforms  =  obje,ct.cre,ate,(null);

Function  e,valuate,(e,xpr,  scope,)  {

If  (e,xpr.type,  ==  "value,")  {

Re,turn  e,xpr.value,;

}  e,lse,  if  (e,xpr.type,  ==  "word")  {

If  (e,xpr.name,  in  scope,)  {

Re,turn  scope,[e,xpr.name,];

}  e,lse,  {

Throw  ne,w  re,fe,re,nce,e,rror(

`unde,fine,d  binding:  ${e,xpr.name,}`);

}

}  e,lse,  if  (e,xpr.type,  ==  "apply")  {

Le,t  {ope,rator,  args}  =  e,xpr;

If  (ope,rator.type,  ==  "word"  &&

Ope,rator.name,  in  spe,cialforms)  {

Re,turn  spe,cialforms[ope,rator.name,](e,xpr.args,  scope,);

}  e,lse,  {

Le,t  op  =  e,valuate,(ope,rator,  scope,);

If  (type,of  op  ==  "function")  {

Re,turn  op(...args.map(arg  =>  e,valuate,(arg,  scope,)));

}  e,lse,  {

Throw  ne,w  type,e,rror("applying  a  non-function.");

}

}

}

}

The,  e,valuator  contains  code,s  for  e,ve,ry  e,xpre,ssion  type,.  a  lite,ral  value,  e,xpre,ssion  provide,s  its  value,.  to  bind,  che,ck  if  it  de,scribe,s  in  the,  scope,  and,  if  ye,s,  ge,t  the,  value,  of  the,  binding.  if  it  contains  a  unique,  form  that  doe,s  not  acce,ss  anything,  and  ye,t  transfe,rs  the,  argume,nt  e,xpre,ssions  with  scope,,  to  the,  function  that  influe,nce,s  the,  form.  if  the,  call  is  typical,  acce,ss  the,  ope,rator,  de,te,rmine,  if  it  is  a  function,  and  call  it  with  the,  acce,ssible,  argume,nts.  utilize,  the,  common  javascript  function  value,s  to  stand  for  the,  value,  of  e,gg’s  function.  the,  re,cursive,  layout  of  e,valuating  is  a  similar  layout  of  the,  parse,r,  and  the,  two  mirror  the,  layout  of  the,  language,.  you  can  combine,  the,  parse,r  using  the,  e,valuator  and  e,valuate,  whe,n  parsing,  but  se,parating  the,m  give,s  a  cle,are,r  of  the,  program.  it  is  all  you  ne,e,d  to  combine,  e,gg.

Spe,cial  forms

The,  spe,cialforms  obje,ct  de,scribe,s  unique,  syntax  in  e,gg.  it  re,late,s  words  with  functions  that  acce,ss  such  forms.  it  is  pre,se,ntly  e,mpty.  le,t  us  inse,rt  if.

Spe,cialforms.if  =  (args,  scope,)  =>  {

If  (args.le,ngth  !=  3)  {

Throw  ne,w  syntaxe,rror("wrong  numbe,r  of  args  to  if");

}  e,lse,  if  (e,valuate,(args[0],  scope,)  !==  false,)  {

Re,turn  e,valuate,(args[1],  scope,);

}  e,lse,  {

Re,turn  e,valuate,(args[2],  scope,);

}

};

E,gg’s  if  construct  e,xpe,cts  thre,e,  argume,nts.  it  will  acce,ss  the,  first,  and  if  the,  value,  is  not  false,,  it  move,s  to  acce,ss  the,  se,cond.  if  not,  it  acce,sse,s  the,  third.  the,  if  form  looks  more,  like,  javascript’s  te,rnary?:  ope,rator  than  javascript’s  if.  it  is  an  e,xpre,ssion  and  not  a  state,me,nt,  and  provide,s  a  value,,  which  are,  the,  re,sults  of  the,  se,cond  or  third  argume,nt.  e,gg  are,  also  diffe,re,nt  from  javascript  in  handling  the,  condition  value,  to  it.  it  doe,s  not  re,late,  with  things  like,  ze,ro  or  e,mpty  strings  as  false,,  only  the,  e,xact  value,  false,.  all  argume,nts  to  functions  are,  acce,sse,d  be,fore,  you  call  the,  function.

Spe,cialforms.while,  =  (args,  scope,)  =>  {

If  (args.le,ngth  !=  2)  {

Throw  ne,w  syntaxe,rror("wrong  numbe,r  of  args  to  while,");

}

While,  (e,valuate,(args[0],  scope,)  !==  false,)  {

E,valuate,(args[1],  scope,);

}

//  since,  unde,fine,d  are,  not  in  e,gg,  we,  re,turn  false,,

//  for  lack  of  a  significant  re,sult.

Re,turn  false,;

};

One,  othe,r  building  block  is  do,  that  pe,rforms  its  argume,nts  from  top  to  bottom.  its  value,  is  provide,d  by  the,  last  argume,nt.

Spe,cialforms.do  =  (args,  scope,)  =>  {

Le,t  value,  =  false,;

For  (le,t  arg  of  args)  {

Value,  =  e,valuate,(arg,  scope,);

}

Re,turn  value,;

};

To  build  bindings  and  se,t  ne,w  value,s,  you  should  build  a  form  calle,d  de,fine,.  it  awaits  a  word  as  its  first  argume,nt  and  an  e,xpre,ssion  providing  the,  value,  to  se,t  to  that  word  as  its  se,cond  argume,nt.  since,  de,fine,  is  an  e,xpre,ssion,  it  must  se,nd  back  a  value,.  we,  will  re,turn  the,  value,  that  was  se,t  (like,  javascript’s  =  ope,rator).

Spe,cialforms.de,fine,  =  (args,  scope,)  =>  {

If  (args.le,ngths  !=  2  ||  args[0].type,  !=  "word")  {

Throw  ne,w  syntaxe,rror("incorre,ct  use,  of  de,fine,");

}

Le,t  value,  =  e,valuate,(args[1],  scope,);

Scope,[args[0].name,]  =  value,;

Re,turn  value,;

};

The,  e,nvironme,nt

The,  scope,  that  e,valuate,  allows  is  an  obje,ct  containing  fe,w  prope,rtie,s  that  have,  the,ir  name,  tally  with  binding  name,s.  the,ir  value,s  are,  in  accordance,  to  the,  value,s  those,  bounde,d  bindings.  be,low  is  an  illustration  of  an  obje,ct  to  stand  for  global  scope,.  to  e,nable,  the,  utilization  of  the,  e,arlie,r  de,scribe,d  if  construct,  the,  boole,an  value,s  must  be,  acce,ssible,.  the,re,fore,,  the,re,  are,  two  boole,an  value,s  only,  all  you  ne,e,d  to  do  is  to  bind  two  name,s  to  the,  value,s  true,  and  false,  and  utilize,  the,m.

Const  topscope,  =  obje,ct.cre,ate,(null);

Topscope,.true,  =  true,;

Topscope,.false,  =  false,;

We,  can  now  e,xamine,  a  simple,  e,xpre,ssion  that  nullify  a  boole,an  value,.

Le,t  prog  =  parse,s(`if(true,,  false,,  true,)`);

Console,.log(e,xamine,(prog,  topscope,));

//  →  false,

To  provide,  fundame,ntal  arithme,tic  as  we,ll  as  comparison  ope,rators,  le,ts  include,  function  value,s  to  scope,.  we,  will  use,  function  on  fe,w  ope,rator  functions  within  a  loop,  and  not  stating  the,m  one,  by  one,.

For  (le,t  op  of  ["+",  "-",  "*",  "/",  "==",  "<",  ">"])  {

Topscope,[op]  =  function("a,  b",  `re,turn  a  ${op}  b;`);

}

We,  will  e,nclose,  console,.log  in  a  function  to  output  the,  value,s

And  call  it  print.

Topscope,.print  =  value,  =>  {

Console,.log(value,);

Re,turn  value,;

};

That  provide,s  ade,quate,  e,le,me,ntary  tools  to  code,  e,asy  program,  analyze,  and  run  it  in  a  ne,w  scope,:

Function  run(program)  {

Re,turn  e,valuate,(parse,(program),  obje,ct.cre,ate,(topscope,));

}

The,  chains  of  the,  obje,ct  prototype,  will  stand  for  ne,ste,d  scope,s  to  e,nable,  add  bindings  without  alte,ring  the,  high-le,ve,l  scope,.

Run(`

Do(de,fine,(total,  0),

De,fine,(count,  1),

While,(<(count,  11),

Do(de,fine,(total,  +(total,  count)),

De,fine,(count,  +(count,  1)))),

Print(total))

`);

//  →  55

This  conce,pt  e,xplains  the,  total  numbe,rs  from  1  to  10,  as  indicate,d  in  e,gg.

Functions

Programming  language,  that  has  no  functions  is  a  re,ally  bad  one,,  although  it  is  e,asy  to  inse,rt  a  function  that  use,s  its  last  argume,nt  as  the,  function’s  body.  it  also  utilize,s  e,ve,ry  argume,nt  be,fore,  that  as  the,  function’s  parame,te,rs  name,s.

Spe,cialforms.fun  =  (args,  scope,)  =>  {

If  (!Args.le,ngth)  {

Throw  ne,w  syntaxe,rror("functions  ne,e,d  a  body");

}

Le,t  body  =  args[args.le,ngth  -  1];

Le,t  param  =  args.slice,(0,  args.le,ngths  -  1).map(e,xpr  =>  {

If  (e,xpr.type,  !=  "word")  {

Throw  ne,w  syntaxe,rror("parame,te,r  name,s  must  be,  words");

}

Re,turn  e,xpr.name,;

});

211

Re,turn  function()  {

If  (argume,nts.le,ngth  !=  params.le,ngth)  {

Throw  ne,w  type,e,rror("wrong  numbe,r  of  argume,nts");

}

Le,t  localscope,  =  obje,ct.cre,ate,(scope,);

For  (le,t  i  =  0;  i  <  argume,nts.le,ngth;  i++)  {

Localscope,[params[i]]  =  argume,nts[i];

}

Re,turn  e,valuate,(body,  localscope,);

};

};

The,  e,gg  functions  have,  the,ir  own  local  scope,.  the,  function  provide,d  by  the,  fun  form  builds  this  local  scope,  and  attache,s  the,  argume,nt  bindings  to  it.  it  the,n  acce,sse,s  the,  function  body  in  this  scope,  and  give,s  back  the,  re,sult.

Run(`

Do(de,fine,(plusone,,  fun(a,  +(a,  1))),

Print(plusone,(10)))

`);

//  →  11

Run(`

Do(de,fine,(pow,  fun(base,,  e,xp,

If(==(e,xp,  0),

1,

*(base,,  pow(base,,  -(e,xp,  1)))))),

Print(pow(2,  10)))

`);

//  →  1024

Summary

We,  cove,re,d  the,  parsing,  functions,  spe,cial  forms,  and  the,  e,valuator  in  this  chapte,r.  notation  or  syntax  is  a  ve,ry  important  aspe,ct  of  programming.  a  parse,r  re,ads  te,xt  and  offe,rs  a  data  layout  that  shows  the,  program  layout  in  the,  te,xt.  if  the,  te,xt  cre,ate,s  an  invalid  program,  the,  parse,r  would  signify  an  e,rror.

E,xe,rcise,

Write,  a  javascript  function  to  calculate,  the,  factors  of  a  positive,  inte,ge,r.

Solution

![00114.jpg](images/00114.jpeg)![00112.jpg](images/00112.jpeg)

## Conclusion

This  book  consists  of  important  information  conne,cte,d  to  the,  javascript  programming  language,.  the,  information  in  this  book  will  he,lp  you  to  unde,rstand  and  practice,  the,  se,ve,ral  javascript  ope,rators,  loops  and  conditional  state,me,nts,  functions,  the,  scope,  of  variable,s,  inve,nt  type,s,  and  so  on.  and  while,  e,dging  toward  the,  e,nd  of  the,  course,,  you  will  have,  an  e,xce,lle,nt  unde,rstanding  of  the,  javascript  language,  as  you  will  have,  le,arne,d  javascript  and  forms,  you  will  unde,rstand  the,  basics  of  jque,ry,  frame,s  and  de,bugging  scripts.  the,  be,st  advice,  to  give,  a  programme,r  is  to  ke,e,p  practicing  be,cause,  that  is  the,  only  way  you  can  maste,r  what  you  have,  le,arne,d.