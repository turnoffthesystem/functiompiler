# functiompiler
functions' compiler

este será un compilador utilizado como herramienta de aprendizaje.

Compilará código con la siguiente forma:

nombre_funcion1(par1,par2,...,parN) {
  return expr;
}

...
nombre_funcionN(...

;

RETURN funcioni(ct1,...,ctN);
RETURN funcionj(ct1,...,ctN);
;;

DONDE "expr" tomará la forma de una operación entre los parámetros, permitiendo:
-     par1 + par2 + ... parN
-     - par1 - par2 - ... parN
-     par1 * par2 * ... parN
-     par1/par2
-     par1^par2
-     log b par

Ello implica, teniendo en cuenta que dichas operaciones también deben permitir el uso de paréntesis
por ende de poder combinarse adecuadamente, que ciertos conflictos a tratar son:

.es imprescindible que, por motivos de temprano diseño, se respeten de manera absoluta e impoluta las reglas de precedencia utilizando paréntesis para ello.

EJ. ERRÓNEO: return par1 * par2 *
;
EJ.ERRÓNEO2: return (par1 + par2 +) * (par3/par3);

EJ.CORRECTO: return par1 * par2;
EJ.CORRECTO2: return (par1 + par2) * (par3/par3);
