Man bruger implements i stedet for extends

Grunden til at man bruger interfaces i stedet for abstrakte klasser er at man kan nedarve fra flere interfaces

Ofte ville navnene på interfaces slutte med able, eksempelvis consumeable

man laver et interface istedet for en class så:

interface name {

}

man kan så lave en class der implementerer det her interface:

class name2 implements name {

}

man kan implementere flere klasser:


class name3 implements name, makeable {

}

de ting der implementerer et interface skal have de metoder som bliver givet i de interfaces som den arver fra.