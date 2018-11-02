# functiompiler
functions' compiler

este será un compilador utilizado como herramienta de aprendizaje.

Compilará código con la siguiente forma:

nombre_funcion1(par1,par2,...,parN) {
  return expr;
}

...
nombre_funcionN(...
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

.una operación que implique más de un parámetro podrá venir o no entre paréntesis -
dentro de dicho paréntesis (o ninguno) es imprescindible que los parámetros de cualquier operación
estén bien separados, respetando el órden de los paréntesis y escribiendo correctamente cada operación

EJ. ERRÓNEO: return par1 * par2 *
;
EJ.ERRÓNEO2: return (par1 + par2 +) * (par3/par3);

EJ.CORRECTO: return par1 * par2;
EJ.CORRECTO2: return (par1 + par2) * (par3/par3);
