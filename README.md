# The-inception
idk what its the function of this, but it looks cool

**Crear dos redes, para mabas VM**
----

*Creaciòn de la Primer red*
![image](https://user-images.githubusercontent.com/86898578/126699334-114cd396-177b-4acb-95bd-b6f64cb674e5.png)
*Se crea la primer red, eliminé la subred de default y agregré una nueva 10.0.0.0/24*

---

*Creaciòn de la segunda red con los mismos pasos*
![image](https://user-images.githubusercontent.com/86898578/126700031-af23415c-4683-48a3-8ff5-852b967caa2e.png)
*subred2 10.1.0.0/24*

---

*Realizar el emparejamiento de ambas redes*
grupo de recursos/red/emparejamientos/agregar/
![image](https://user-images.githubusercontent.com/86898578/126700876-9577bd5d-c10d-4c00-acca-840451810c4f.png)
*Aquí se agrega el vinculamiento, el segundo apartado es de la vinculaciòn de la otra red, de la 2 a la 1 (red2), al final se tiene que colocar la red a la que se vincula*

---

*Creación de la Máquina virtual*
![image](https://user-images.githubusercontent.com/86898578/126702413-dbf816c5-7b47-464b-94c3-6f7e733ee160.png)
*Se concecta a las redes antes creadad, la VM1 -> red1, y la VM2, a la red 2*

---

*Si se tiene windows pro, entonces el paso a realizar sobra, sino hay que descargar de la tienda el siguiente recurso:*
![image](https://user-images.githubusercontent.com/86898578/126703698-c89a1b70-204d-4780-94ac-ed650eeb5609.png)

---

*Concectando ambas máquinas virtuales, VM1/concectar/RDP/descargar archivo RDP*
![image](https://user-images.githubusercontent.com/86898578/126703758-f042ae43-a0bb-4cb2-9b1a-9728c607647d.png)
---
![image](https://user-images.githubusercontent.com/86898578/126704405-d31c31b8-2a2f-446f-ad52-6319f3884e63.png)
---
![image](https://user-images.githubusercontent.com/86898578/126704937-91ec4239-14cd-4b5a-9fe9-15853bcb43d7.png)
---
![image](https://user-images.githubusercontent.com/86898578/126705180-083b318e-d4ed-40c2-aa79-1cc15d2fe9c9.png)

*Ahora ya nos hemos conectado a la VM1*
![image](https://user-images.githubusercontent.com/86898578/126705224-d81249af-a32b-46a8-9689-89d7a52e2d7d.png)

---

*En el escritorio de la máquina virtual, hay que abrir el power shell, o el cmd*
![image](https://user-images.githubusercontent.com/86898578/126705363-d77bf54f-e4df-48db-8598-40c4c9ecb10a.png)
![image](https://user-images.githubusercontent.com/86898578/126706568-c5de7c4a-d442-44c1-bc04-bcc63c4b55bc.png)

*Escribir el siguiente comando:*
`New-NetFirewallRule -Display "Allow ICMPv4" -Protocol ICMPv4`

*Encontrar en el apartado de redes cual es la ip privada de la vm2 (a la que queremos conectarnos), en este caso 10.1.0.4*
*máquinas virtuales/MV1/redes/copiar la ip privada

` Ping 10.1.0.4`

(Se puede ver que cometí el error de poner la ip de la misma VM1 y no el de la 2, por lo cual me marcaba un error, que se me denegaba el acceso xd)

![image](https://user-images.githubusercontent.com/86898578/126707534-922f85b3-14f8-4592-8bf4-bcb4b28d0570.png)

*Ahora sólo toca conectarnos con el siguiente comando:*
`mstsc /v:10.1.0.4`

![image](https://user-images.githubusercontent.com/86898578/126707955-14436426-d830-4fb7-a36b-f099214dad63.png)

*Ahora se tiene el inception, y se cerrò xd*
![image](https://user-images.githubusercontent.com/86898578/126708056-d65e35ef-b05d-4065-b8b2-8e83530cac2c.png)

