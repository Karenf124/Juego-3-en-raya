Juego-3-en-raya
===============

Javascript
<!DOCTYPE html>
<html>

<head>

<title>tres en raya grupo 
 </title>

<script type="text/javascript">

 

 var img='x.PNG';
 var turno=1;
 var arreglo = new Array();
 var jug1=0;//acumula los puntos del jugador 1
 var jug2=0;//acumula los puntos del jugador 2

 for(i=0; i<=8; i++){

  arreglo[i]=-1;

 }

 function box(pos){

    if(arreglo[pos]==-1){//si la posicion está vacia
     
     if(turno==1){
      if(img=='x.PNG'){
        document.getElementById('c'+pos).src=img;
	arreglo[pos]=1;
        turno=2;
	img='bola.PNG';
      }
      
     }else if(turno==2){ 
      if(img=='bola.PNG'){
       document.getElementById('c'+pos).src=img;
       arreglo[pos]=0;
       turno=1;
       img='x.PNG';
      }

     }

    }else{ alert('Posicion ocupada!'); }
    


  //-------------define el ganador en la fila 1------
  if(arreglo[0]==1 && arreglo[1]==1 && arreglo[2]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[0]==0 && arreglo[1]==0 && arreglo[2]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------



  //-------------define el ganador en la fila 2------
  if(arreglo[3]==1 && arreglo[4]==1 && arreglo[5]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[3]==0 && arreglo[4]==0 && arreglo[5]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la fila 3------
  if(arreglo[6]==1 && arreglo[7]==1 && arreglo[8]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[6]==0 && arreglo[7]==0 && arreglo[8]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la columna 1------
  if(arreglo[0]==1 && arreglo[3]==1 && arreglo[6]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[0]==0 && arreglo[3]==0 && arreglo[6]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la columna 2------
  if(arreglo[1]==1 && arreglo[4]==1 && arreglo[7]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[1]==0 && arreglo[4]==0 && arreglo[7]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la columna 3------
  if(arreglo[2]==1 && arreglo[5]==1 && arreglo[8]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[2]==0 && arreglo[5]==0 && arreglo[8]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la diagonal \------
  if(arreglo[0]==1 && arreglo[4]==1 && arreglo[8]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[0]==0 && arreglo[4]==0 && arreglo[8]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------


  //-------------define el ganador en la diagonal /------
  if(arreglo[2]==1 && arreglo[4]==1 && arreglo[6]==1){
	alert('gano X');
        jug1=jug1+1;
	limpiar();
  }

  if(arreglo[2]==0 && arreglo[4]==0 && arreglo[6]==0){
	alert('gano O');
        jug2=jug2+1;
	limpiar();
  }
  //-------------------------------------

 document.getElementById('ptsjug1').innerHTML=jug1;
 document.getElementById('ptsjug2').innerHTML=jug2;

 }//box()
  

 function limpiar(){

  document.getElementById('reset').src="limpiar_pre.png";//unde el boton

  for(i=0; i<=8; i++){
     document.getElementById('c'+i).src="fondo.PNG";
  }

  //reseteo el arreglo
  for(i=0; i<=8; i++){
     arreglo[i]=-1;
  }

 }

 function suelta(){
  document.getElementById('reset').src="limpiar.png";
 }

 

</script>

</head>

<body><center>
tres en raya grupo: </p>
Franco Mero Karen Vanessa</p>
Holguin cedeño Edison Ariel
</center>
<center>


<table border="0">


 <tr>
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c0" onclick="box(0)" /></td>  
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c1" onclick="box(1)" /></td>  
    <td style="border-style:solid;border-right-color:#ffffff;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c2" onclick="box(2)" /></td>  
 </tr>

 <tr>
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c3" onclick="box(3)" /></td>  
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c4" onclick="box(4)" /></td>  
    <td style="border-style:solid;border-right-color:#ffffff;border-left-color:#ffffff;border-top-color:#ffffff;"><img src="fondo.PNG" id="c5" onclick="box(5)" /></td>  
 </tr>

 <tr>
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;border-bottom-color:#ffffff;"><img src="fondo.PNG" id="c6" onclick="box(6)" /></td>  
    <td style="border-style:solid;border-left-color:#ffffff;border-top-color:#ffffff;border-bottom-color:#ffffff;"><img src="fondo.PNG" id="c7" onclick="box(7)" /></td>  
    <td style="border-style:solid;border-right-color:#ffffff;border-left-color:#ffffff;border-top-color:#ffffff;border-bottom-color:#ffffff;"><img src="fondo.PNG" id="c8" onclick="box(8)" /></td>  
 </tr>

 <tr>
    <td>--------------</td>  
    <td>--------------</td>  
    <td>--------------</td>  
 </tr>

 <tr>
    <th>Jugador 1</th>  
    <td>&nbsp;</td>  
    <th>Jugador 2</th>  
 </tr>

 <tr>
    <td><img src="x.PNG" /></td>  
    <td><img src="limpiar.png" id="reset" onclick="limpiar()" onmouseout="suelta()" /></td>  
    <td><img src="bola.PNG" /></td>  
 </tr>

 <tr>
    <td><div id="ptsjug1" style="font-weight:bold;text-align:center;">0</div></td>  
    <td>&nbsp;</td>  
    <td><div id="ptsjug2" style="font-weight:bold;text-align:center;">0</div></td>  
 </tr>

</table>

<br />


</center>

</body>

</html>
