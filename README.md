# Cliente ficticio: Aguas del Plata S.A.

## Sector
Utility de agua potable y saneamiento. Opera plantas de tratamiento,
estaciones de bombeo y red de distribución para una ciudad intermedia
(~400.000 habitantes) en Argentina.

## Descripción
Aguas del Plata es una empresa mixta (capital estatal/privado) de tamaño
medio. Gestiona 3 plantas potabilizadoras, 12 estaciones de bombeo y una
planta de tratamiento de líquidos cloacales. Tiene ~450 empleados, de los
cuales una fracción pequeña (equipo de IT, ~8 personas) es responsable
tanto de sistemas administrativos como de soporte a los sistemas de
control industrial (OT), sin un equipo de seguridad dedicado.

## Superficie de exposición estimada
- **OT/SCADA:** PLCs y HMIs de al menos dos generaciones distintas,
  algunos con protocolos sin autenticación (Modbus TCP expuesto en
  segmentos internos mal aislados de la red corporativa).
- **Acceso remoto:** VPN para mantenimiento de vendors externos de
  automatización, con credenciales compartidas y sin MFA.
- **IT corporativo:** ERP, facturación online para usuarios, correo,
  sitio web público con portal de pagos.
- **IoT/sensores:** sensores de nivel y calidad de agua con conectividad
  celular/NB-IoT, gestionados por un proveedor tercero.
- **Cadena de suministro:** dependencia de 2-3 integradores externos
  para mantenimiento de PLCs (superficie de exposición vía terceros).
- **Factor humano:** personal operativo de planta con bajo nivel de
  concientización en phishing/ingeniería social.

## Por qué me importa
Los ataques a infraestructura de agua dejaron de ser hipotéticos: el
intento de manipular niveles de hidróxido de sodio en Oldsmar (EE.UU.,
2021) y los ataques de 2023-2024 contra PLCs Unitronics en utilities de
agua estadounidenses (atribuidos a grupos vinculados a Irán) muestran
que este sector es un blanco activo, no teórico. A diferencia de un
banco, acá el impacto de un incidente no es solo financiero: es salud
pública directa. Y a diferencia de una gran multinacional, una utility
mediana como Aguas del Plata tiene el mismo nivel de exposición pero
una fracción del presupuesto y la madurez de seguridad para defenderse.
Ese desbalance —blanco de alto impacto, defensa de bajo presupuesto—
es exactamente el tipo de escenario que quiero aprender a analizar.
