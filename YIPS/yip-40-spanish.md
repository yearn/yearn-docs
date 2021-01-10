---
YIP: 40
Título: Reemplazar los firmantes inactivos de la multisig
Estado: Implementada
Autor: cp287 (@illlefr4u), Artem K (@banteg)
Discusiones: https://gov.yearn.finance/t/change-participants-of-the-multisig-wallet/2991

Fecha de creación: 2020-08-24
---

## Explicación corta

Dado el incremento en las responsabilidades de los firmantes de la multisig, cuatro de ellos han decido ceder sus puestos por baja actividad a posibles participantes que sean más activos. Esta propuesta sustituye a cuatro de los firmates por cuatro nuevas personas elegidas en función de su actividad y mérito.

## Resumen

Actualmente, ejecutar una transacción que debe ser firmada por la multisig puede llevar hasta 24 horas. Con el ritmo de trabajo de Andre y un espacio en constante cambio, esto crea problemas y un tiempo muerto innecesario. Los participantes de la multisig deben ser responsables, pero también deben estar al tanto de lo que pasa dentro del projecto y tomar las desiciones necesarias para su rápido desarrollo. 

## Motivación

yEarn necesita una multisig que pueda implementar rápidamente las decisiones tomadas, sin poner en riesgo ni disminuir la seguridad de los fondos bajo el control de la wallet de la multisig. 

## Especificación

### Visión de futuro

Los siguientes firmantes cenden sus puestos:
- Michael (Curve.fi)
- Cooper Turley
- Calvin Liu
- Damir Bandalo

Después de una cuidadosa evaluación y votación, sugerimos los siguientes cuatro candidatos:
- Joe Mahon (Substreight)
- Tarun Chitra (Gauntlet)
- Vasiliy Shapovalov (p2p.org)
- Mariano Conti (ex-MakerDAO)

### Razonamiento

Necesitamos una multisig fuerte y receptiva que pueda resolver las cosas cuando algunos de los miembros no estén disponibles. Consulta los enlaces de discusión para estadísticas de actividad y más justificación.

### Especificación técnica

Para ejecutar una transacción no necesitamos cambiar el mínimo necesario, unicamente ejecutar secuencialmente 8 transacciones firmadas por la multisig:

1. Añadir 0x6E83d6f57012D74e0F131753f8B5Ab557824507D (Vasily)
2. Eliminar 0xFe45baf0F18c207152A807c1b05926583CFE2e4b (Michael)
3. Añadir 0x6F2A8Ee9452ba7d336b3fba03caC27f7818AeAD6 (Mariano)
4. Eliminar 0x59171b87817C5F07157066Bd5284707A711229B3 (Cooper)
5. Añadir 0x07425B7a76a52dE36dFA313E13E9E3a8DBC476CF (Tarun)
6. Eliminar 0xb0325DbE7fA891436E83A094f9F12848c78e449b (Calvin)
7. Añadir 0x50B0C406a5C1fC492F84c3F3D4552391cF4672f2 (Substreight)
8. Eliminar 0xa83838221278f22ee5bAe3E523f34D42b066D67D (Damir)

## Discusión

https://gov.yearn.finance/t/change-participants-of-the-multisig-wallet/2991

https://gov.yearn.finance/t/nominate-yourself-for-the-foundation-model/3166
