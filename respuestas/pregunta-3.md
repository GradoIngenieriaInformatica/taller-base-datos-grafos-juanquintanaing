MATCH (p:Persona)-[:AMIGO_DE]->(a:Persona)
RETURN p.nombre, COUNT(a) AS totalAmigos