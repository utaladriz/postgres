#Ejercicio 6

##Creación de Indices

Cree un índice sobre la tabla nodo en el campo nombre de tipo Btree  
Utilizando EXPLAIN y haciendo un Select por nombre anote los resultados  
Luego bote el índice y cree un ÍNDICE de tipo GIST   
Utilizando EXPLAIN y haciendo un Select por nombre anote los resultados  
Luego bote el índice y cree un ÍNDICE de tipo GIN   
Utilizando EXPLAIN y haciendo un Select por nombre anote los resultados  

Ahora lo mismo pero para el campo jsonb.  

Cree un índice sobre la tabla nodo en el campo data de tipo Btree  
Utilizando EXPLAIN y haciendo un Select por algun campo json de data,  anote los resultados  
Luego bote el índice y cree un ÍNDICE de tipo GIST   
Utilizando EXPLAIN y haciendo un Select por algun campo json de data,  anote los resultados  
Luego bote el índice y cree un ÍNDICE de tipo GIN   
Utilizando EXPLAIN y haciendo un Select por algun campo json de data,  anote los resultados 

SELECT am.amname AS index_method, opc.opcname AS opclass_name,opc.opcintype::regtype AS indexed_type, opc.opcdefault AS is_defaultFROM pg_am am INNER JOIN pg_opclass opc ON opc.opcmethod = am.oidWHERE am.amname = 'btree'ORDER BY index_method, indexed_type, opclass_name;
CREATE INDEX idx1 ON census.lu_tracts USING btree (tract_name text_pattern_ops);












