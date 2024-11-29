# Meeting notes

- Meeting times: as per https://crab.fit/ekumen-152483

## [[2024-11-XX]]
- Attending: [[Matt Noyes]] [[Nathan Schneider]] [[Eduardo Mercovich]] [[Eduardo Ivanec]] ...
- Check ins
- Why we're here
- What we've thought of, done so far
    - Documentation and other shared artifacts
- Other projects in this space
- Other people who might be interested in this project or any adjacent
- Where to go from here


## [[2024-11-29]]
- Attending: [[edumerco]] [[flancian]]
- Check ins
    - Flan: Lighter work week due to thanksgiving meaning the US is out :)
    - Edu: Interesting research regarding community infrastructure, rights advocacy
        - [[Appreciative interviews]]
        - [[comunicación]] y [[co-cuidado digital]]
        - Found common patterns across three different organizations
        - Gradientes de: confianza y control; herramientas y estrategias
        - Documentación de best practices para reducir vulnerabilidad
- Gradientes y el Ekumen
    - [[autopoiesis]]
    - métricas de conectividad entre instancias
    - feeds de moderación
        - spam.rss
        - abuse.rss
        - etc.
- Sutty
    - [[massive wiki]] link


## [[2024-11-22]]
- Attending: [[edumerco]] [[flancian]]
- Check ins
    - Dinámica de comunidad
        - Axiomas, compartidos o no
    - Post-enfermedad
- Social.coop
    - procesos de gobernancia
- Ekumen
    - charla compartida
    - riesgos cuando hay una pretensión de imponer las propias preferencias
    - concepción:
        - publicamos recomendaciones de bloqueo/federación/defederación de acuerdo a ciertos criterios establecidos y públicos
        - la gente puede adoptarlas o no
        - establecer reglas y procesos de forking/merging para 'incorporar' procesos de resolución de conflicto, modularidad
        - cómo construir espacios seguros de diferente nivel?
            - -> deberíamos proveer las herramientas y dejar que las comunidades las usen para construirse
            - -> sistema por niveles? e.g. L5 es una amenaza directa de violencia/sugerencia de genocidio. L3 es discurso violento. etc.
        - empezar con el caso base: social.coop publicando nuestras normas de forma estructurada. después: cómo co-federar estas con una instancia amiga.
        - largo plazo: actividades de moderación en activitypub?
    - compartiendo actividad de moderación con criterios comunes para construir espacios más seguros y humanos
        - cuenta designada para consumo programático?
- Formas de optimizar procesos de moderación
    - toda la información necesaria para evaluar un reporte en un lugar (incluido el post!)
        - -> FR para Mastodon?
    - automod + confirmación a posteriori
        - puede ser script

## [[2024-11-01]]
- Attending: [[edumerco]] [[flancian]]
- Agora recap and tips :)
- Eduardo found [[UFOI]]: https://ufoi.org
    - It is very much Ekumen-like. Should we join it instead?
    - We don't necessarily agree with some of their principles, like the nudity policy.
    - But we could use it as a base, and still try to federate with them and co-moderate.
    - Alternatively we could target tool building and start something smaller, like the neighborhood of social.coop.
    - Tools can build on the subset of established shared norms between instances. The contracts could be modular.
- [[Sutty]] is experimenting with site federation using [[ActivityPub]]
    - Publishes articles from static sites to the Fediverse
    - Supports moderation of comments


## [[2024-10-11]]
- Attending: [[edumerco]] [[flancian]]
- Task list
    - Codeberg
    - List
    - Agora

## [[2024-10-18]]
- Attending: [[edumerco]] [[flancian]]
- Ontologías organizacionales (?)
    - Mecanismos de defensa
- Otros proyectos
    - [[Sutty]]: dando servicio y cuidado a las comunidades de militantes
- [[Sociocracia]]:
    - https://bbb.de.meet.coop/playback/presentation/2.3/b0a4306a4f14665b2b4d3977372cb4736440d8ff-1729112065531 
    - https://bbb.de.meet.coop/presentation/b0a4306a4f14665b2b4d3977372cb4736440d8ff-1729112065531/meeting.mp4
- [[Ekumen]]:
    - Repos
    - Bootstrap
        - Agregar llave a Codeberg:
            - copiar/pegar de ~/.ssh/id_ed25519.pub (o id_rsa.pub, etc.)
            - a https://codeberg.org/user/settings/keys
        - `git clone git@codeberg.org:Ekumen/ekumen.git`
            - Acá podemos poner documentación inicial
            - Después e.g.: git add example.md; git commit -a -m 'test'; git push
    - https://writer.oliphant.social/oliphant/islands-an-opt-in-federated-network
    - Next steps:
        - Iterate on the initial promoter group
        - Determine a slot to meet
        - Iterate on the basic tenets
        - Start modeling the system that the Ekumen would try to instantiate
            - (Actors, processes)
        - Document potential for optimizing processes in the Fediverse
            - e.g. trusted person reports spam -> limit immediately, review later
            - e.g. N people report spam -> suspend first, review later
            - "[[automod]]" 
    
## [[2024-10-04]]
- Attending: [[edumerco]] [[flancian]]
- Check ins
    - [[Milei]]
        - Qué viene después de Milei?
            - [[Kicillof]]?
            - [[Juan Grabois]]?
    - Gripe
- Facetas del Ekumen :)
    - Documentación
    - Repos
        - [x] flancian: crear repositorio en e.g. codeberg
            - https://codeberg.org/Ekumen/ekumen.git
        - [ ] edumerco: crear usuario en codeberg: https://codeberg.org/
- Next steps
    - Determine possible invitees
    - Once we have this, we can create a time poll
    - Draft invitation, initial meeting
    - The some co-design meetings
    - Then seeking funding for concrete implementation
- Comments
    - Discoverability phase
- Meta-governance (for this group)
    - How to handle self-moderation, group membership, associated protocols
- Initial definition
- https://cryptpad.fr/pad/#/2/pad/edit/5xxQZvxvjfAP2eQTYenLuWOZ/embed/
 

## Invitades posibles
- Flancian y EduMerco
- Darius y Erin
- Wouter Tebbens
- IFTAS
- Ivan y Mayel (Bonfire)
- Evan Podromou
- Christine Lemmer-Webber
- mhoye @mhoye@mastodon.social
- Nathan Schneider
- Matt Noyes (social coop)
- Mike Hales
- other near/aligned instances? 

## Definición inicial
The Ekumen - The Hainish ¿Coalition, confederation? 

Our objective is to create a more welcoming, safe, and humane Fediverse. In order to do that, we
+ imagine, explore, design, prototype and test socio-technical systems (agreements, processes and tools) and
+ share information and knowledge for everyone to make this systems better. 

We start with a small groups of people from various instances who share values of equity, respect, diversity, self governance and non-discrimination.

The key to shared and increased power is the correlation of sharing and receiving information between instances in a clear, trusted, and guarded space.

We can understand and act as a group in ways that no one could do alone.

## Plan
1. Meet and get to know each other. Check if there are other that need to be here now. 
2. Research previous related projects. Learn from them.
3. Design the agreements and processes. 