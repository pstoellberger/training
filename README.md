IT4biz Training
========

Updated: 20 Jan 2014

Downloads Pentaho BI Suite

Links Pentaho:
http://sourceforge.net/projects/pentaho/

PRD 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Report%20Designer/5.0.1-stable/

PDI 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Data%20Integration/5.0.1-stable/

PME 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Pentaho%20Metadata/5.0.1-stable/

BI Server 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.0.1-stable/

PSW 3.6.1 Stable
http://sourceforge.net/projects/mondrian/files/schema%20workbench/3.6.1-stable/

PAD 5.0.1 Stable
http://sourceforge.net/projects/mondrian/files/aggregation%20designer/5.0.1-stable/

PDS 4.0.0 Stable
http://sourceforge.net/projects/pentaho/files/Design%20Studio/4.0.0-stable/

Links Mondrian:
http://sourceforge.net/projects/mondrian/

Mondrian 3.6.1
http://sourceforge.net/projects/mondrian/files/mondrian/mondrian-3.6.1/

Infos:

BI Server 5.0.1
http://localhost:8080/
user: admin
password: password

Administration
Home -> Administration

Pentaho BI Server 5.0.1CE MySQL installation guide
http://anonymousbi.wordpress.com/2013/12/15/pentaho-bi-server-5-0-1ce-mysql-installation-guide/

Personalização básica para colocar em produção

https://github.com/it4biz/training/blob/master/pentaho-5.0-personalizacao.txt


http://www.science.co.il/Language/Locale-codes.asp

Links visualizadores OLAP:

Saiku Chart Plus
http://it4biz.github.io/SaikuChartPlus/

Saiku
http://meteorite.bi/saiku

Pivot4J
http://mysticfall.github.io/pivot4j/
http://www.pivot4j.org/

Pivot
http://jpivot.sourceforge.net/

STPivot
https://code.google.com/p/stpivot/

OLAP4J
http://www.olap4j.org/

http://www.science.co.il/Language/Locale-codes.asp

Como logar sem pedir usuario e senha no Pentaho BI Server 5.0.1?

Até a versão 4.8 funciona colocar userid=admin&password=password em qualquer URL.

A partir da versão 5.0.1 somente é aceito na página Home conforme exemplo abaixo:
Home aceita
http://localhost:8080/pentaho/Home?userid=admin&password=password

Direto no Relatório não aceita userid e password
http://172.16.1.6:8080/pentaho/api/repos/:public:IT4biz:Reports:ClientsReport.prpt/viewer?ts=1390324489461&userid=admin&password=password

Infos:
http://jira.pentaho.com/browse/BISERVER-10354
http://jira.pentaho.com/browse/BISERVER-10708


MDX
 select NON EMPTY(TopCount({Descendants([Produto].[Todos] ,[Produto].[Nome do Produto])}, 5, [Measures].[Valor])) on ROWS, 
 NON EMPTY({[Measures].[Valor]}) on Columns 
 from [Vendas]
 WHERE {${filtroAnoVendasParameter}}
          
          


