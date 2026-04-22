MATCH (p:Persona)-[:AMIGO_DE]->(a:Persona)
WITH p, COUNT(a) AS totalAmigos
WHERE totalAmigos >= 2
RETURN p.nombre, totalAmigos