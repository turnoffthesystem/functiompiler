# functiompiler
functions' compiler

este será un compilador utilizado como herramienta de aprendizaje.

Compilará código con la siguiente forma:

nombre_funcion1(par1,par2,...,parN) {
  RETURN expr;
}

...
nombre_funcionN(...

%

RETURN funcioni(ct1,...,ctN);
RETURN funcionj(ct1,...,ctN);

%

DONDE "expr" tomará la forma de una operación entre los parámetros u OPERANDOS EN GENERAL (EN EL CASO DE LA GRAMÁTICA, SE VERÁ QUE YA SE TRATA LA POSIBILIDAD DE CONSTANTES Y MAYOR VARIEDAD DE OPERANDOS), permitiendo:
-     par1 + par2 + ... parN
-     - par1 - par2 - ... parN
-     par1 * par2 * ... parN
-     par1/par2
-     par1^par2
-     par1 log par2 --- nos sirve situando al primer operando en el papel de la base i al segundo en el papel del elemento principal de cálculo

Ello implica, teniendo en cuenta que dichas operaciones también deben permitir el uso de paréntesis
por ende de poder combinarse adecuadamente, que ciertos conflictos a tratar son:

.es imprescindible que, por motivos de temprano diseño, se respeten de manera absoluta e impoluta las reglas de precedencia utilizando paréntesis para ello.

EJ. ERRÓNEO: RETURN par1 * par2 *
;
EJ.ERRÓNEO2: RETURN (par1 + par2 +) * (par3/par3);

EJ.CORRECTO: RETURN (par1*par2);
EJ.CORRECTO2: RETURN ((par1 + par2)*(par3/par3));
