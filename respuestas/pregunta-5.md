MATCH (e:Empresa)
WITH COUNT(e) AS totalEmpresas
MATCH (p:Persona)-[:TRABAJA_EN]->(e:Empresa)
WITH p, totalEmpresas, COUNT(DISTINCT e) AS empresasDondeTrabaja
WHERE empresasDondeTrabaja = totalEmpresas
RETURN p.nombre