# Tp_en_JSP
# exerciec1.jsp
<%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<body>
<%! String[] articlesEnInventaire = {"qcm123", "ads234", "qwerty456", "azerty567", "cap789", "down345", "top765", "jungle432", "fire876", "hi234"};
String articlesCherches = "down345"; boolean trouve = false;
int trouveIndex = -­‐1;%>
<H1>Recherche de <%=articlesCherches%> au niveau de la base:
</H1>
<UL>
<% int i = 0;
while (!trouve && i < articlesEnInventaire.length) {%>
<LI> Recherche index <%= i%>: <%= articlesEnInventaire[i]%>
<% if (articlesEnInventaire[i] == articlesCherches) { trouve = true;
trouveIndex = i;
} i++;
 
} %>
</UL>
<H2>
<% if (trouve) {%>
Trouvé à index = <%=trouveIndex%>
<% } else {%>
Désolé, <%=articlesCherches%> ne se trouve pas dans la base
<% }%>
</H2>
</body>
</html>
  
  
  
  
  
  
  # exerciec2.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<body>
<H1 ALIGN="center">An Order Form</H1>
<%! String article[] = {"toaster", "CD", "diskette"}; double prix[] = {19.99, 12.99, 1.99};
int quantite[] = {2, 9, 24};
%>
<TABLE ALIGN="center" BGCOLOR="yellow" BORDER="1" WIDTH="75%">
<TR><TD>Article</TD>
 
<TD>Prix</TD>
<TD>Quantite</TD>
<TD>Prix Total</TD>
</TR>
<% for (int i = 0; i < 3; i++) {%>
<TR><TD><%= article[i]%></TD>
<TD><%= prix[i]%></TD>
<TD><%= quantite[i]%></TD>
<TD><%= prix[i] * quantite[i]%></TD>
</TR>
<% } //end for loop %>
</TABLE>
</body>
</html>







  # exerciec3.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<body>
<%! String nom = new String("Ali Hassan"); Integer cnss = new Integer(111223333); Double salaire = new Double(65432.10); Vector employe = new Vector();
 
%>
<% employe.addElement(nom); employe.addElement(cnss); employe.addElement(salaire);
%>
Nom Employe : <%= (Object) employe.elementAt(0)%> CNSS Employe : <%= (Object) employe.elementAt(1)%> Salaire Employe : <%= (Object) employe.elementAt(2)%>
</body>
</html>




  
  # exerciec4.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<%@include file='./Header.jsp' %>
<p align="center">Le Contenu on le place ici...</p>
<%@include file='./Footer.jsp' %>
Page Header.jsp
<%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<body style="font-­‐family:verdana,arial;font-­‐size:10pt;">
<table width="100%" height="100%">
<tr bgcolor="#99CCCC">
 
<td align="right" height="15%">Bienvenue dans cet exemple...</td>
</tr>
<tr>
<td height="75%">
#Page Footer.jsp
<%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
</td>
</tr>
<tr bgcolor=" #99CC99">
<td align="center" height="10%">Copyright AKYA Media 2015</td>
</tr>
</table>
</body>
</html>

  
  
  
  
  # exerciec5.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
 
</head>
<body>
<% if (Math.random() > .5) { %>
<jsp:forward page="Fibonacci.jsp"/>
<% }else { %>
<jsp:forward page="Factorielle.jsp"/>
<% } %>
</body>
</html>





  # exerciec6.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<body>
<body bgcolor="white">
<%!
String randomColor() {
java.util.Random random = new java.util.Random(); int red = (int) (random.nextFloat() * 255);
int green = (int) (random.nextFloat() * 255); int blue = (int) (random.nextFloat() * 255); return "#"
+ Integer.toString(red, 16)
 
+ Integer.toString(green, 16)
+ Integer.toString(blue, 16);
}
%>
<h1>Random Color</h1>
<table bgcolor="<%= randomColor()%>" >
<tr><td width="100" height="100">&nbsp;</td></tr>
</table>
</body>
</body>
</html>







  # exerciec7.jsp
  <%@page contentType="text/html" pageEncoding="UTF-­‐8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-­‐equiv="Content-­‐Type" content="text/html; charset=UTF-­‐8">
<title>JSP Page</title>
</head>
<%
String bgColor = request.getParameter("bgColor"); if (bgColor == null) {
bgColor = "WHITE";
}
%>
<%! private int accessCount = 0;%>

  

  
