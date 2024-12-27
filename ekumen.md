# Meeting notes

- Meeting times: as per https://crab.fit/ekumen-152483

## [[2024-12-27]]
- Attending: [[Eduardo Mercovich]] [[Flancian]]
- Japan trip
    - [[Hiroshima]]
- [[Puntos de palanca]]
    - Mejor herramienta para moderación
        - "Moderaverse"
        - Podríamos mejorar lo que tiene mastodon a través de las APIs
        - Idealmente sería universal
        - Los mods podrían formar parte de la comunidad que hace esta herramienta
        - Unos temas
            - Instalación / overhead técnico
            - Hosting / servicio reusable por varias instancias (oauth etc.)
        - Próximos pasos
            - Edu podría ser invitado por el CWG para conocer los reportes que recibimos
            - Prototipar una interfaz?
                - Mostrar cola de moderación
                - Traer información de los actores involucrados (denunciante, denunciade, contexto)
- [[January reboot]]

## [[2024-12-06]]
- Attending: [[Ivan]] [[Eduardo Mercovich]] [[Flancian]] ...
- Check ins
    - Political background
    - Ivan: doing well, happy to go through this together and looking forward to discussing the Ekumen and progress in Bonfire
    - Eduardo: tired but happy :) Many things going on, good and not so good, but have decided that the not so good can't take away from the overall wellbeing infinitely.
    - Flan: happy to be here, taking a break from corporate environment. Looking forward also to discussing Ekumen and Bonfire.
- Why we're here
    - Eduardo: in the [[mydata]] board. Would like to think going forward on how we can build synergy between several projects in this space; organizations like mydata.org are interested in shifting more towards the Fediverse.
- What we've thought of, done so far here under the Ekumen banner
    - Focus on [[governance]] and [[tooling]]
    - [[Eduardo]] on how we got here
        - Anti-meta [[Fedipact]] took place in the Fediverse last year
        - Led us to think: instead of taking this 'anti' stance, why don't we try a positive approach: let's define a basic set of values that instances can endorse.
        - [[Fediversalist papers]]
            - [[Ivan]]: this is great work and is indeed a great guide.
        - [[UFOI]] and [[archipielago]] movements
        - [[IFTAS]]
    - Sharing moderation burden between instances
        - And in general develop tools for enabling better and cheaper moderation
- Bonfire roadmap
    - Updates from [[bonfire]]
    - [[Ivan]]: Bonfire is approaching this space as a set of extensions. We want to ensure Bonfire is safe and moderated bottom-up.
        - 1.0 had a lot of effort towards bottom-up fine-grained moderation. We're using the concepts of circles and boundaries; implemented also in [[gotosocial]].
            - Need to test interop with [[gotosocial]], which has reply control.
            - Access roles (sp?) linked to actions: what a user can and cannot do.
                - This lets you specify who can do what in your activities (reply, boost, edit!).
            - Question: can we create rules like "with 2 people of this circle and no objection in 7 days, the proposal passes?"
                - Yes, this is exactly the kind of scope.
        - We believe in co-designing with the community of users.
        - **Have had conversations with [[Erin Kissane]], collaborating with us to release a version of boundaries/circles but also to explore how to implement governance features. She would probably be interested.**
        - 2 points: Ekumen tries to be tool agnostic + once designed, search funds to develop. 
        - Also a conversation with [[X]] from [[PolicyKit]].
            - Q: Who? Amy Zhang
            - Thanks!
        - And the new CTO of [[OpenCollective]], since they are now more decentralized they were considering tools for distributed governance.
        - Intrigued by e.g. [[archipielago]], [[opt-in]] moderation models
        - Q: let's assume we're using Bonfire to discuss these topics, could we express rules and moderation actions in both computer-readable and human-readable ways?
            - A (Ivan): wouldn't rush to answer this, as I have to still read e.g. how the internals of [[PolicyKit]] work. They have their own UI, so reviewing their UI could give us guidance here. Bonfire is intending on publishing PolicyKit actions as activities.
            - **The architecture of Bonfire makes possible that everything and any activity can be threaded.**
            - Q: community annotations?
                - A: https://bonfirenetworks.org/posts/content_labelling_in_bonfire/
  - Edu: the Ekumen wants to be implementation-agnostic as much as possible, we'd like to be able to add value for communities using all of Bonfire/Mastodon/Pleroma/etc.
    - Would like to focus on design work first, then seek funding to support work.
    - Ivan: makes sense. We can leverage e.g. shared diffusion opportunities like blog posts.
    - Ivan: on bounties for Bonfire and attracting contributors.
        - Main goal is to release 1.0 and prove that Bonfire is a NG framework. Next April!
        - We can now develop iOS and Android applications with Elixir; [[LiveViewNative]].
    - Ivan: [[Digital Common Goods]] is what we're trying to create.
- Tooling and technical ideas
  - Starting ideas
    - Publishing moderation events as activities
        - (Already discussed previously w.r.t. PolicyKit)
    - Affinity/levels of trust between instances
        - Bonfire doesn't support this directly, but through circles you could keep a list of moderators you trust from other instances. So this could be adapted into affinity level.
        - Edu: on the relationship to [[IFTAS]]
            - (who want to move to Bonfire)
            - on getting feedback from other instances; knowing if suggested moderation actions were taking remotely and potentially "rewarding" the instance with a higher affinity/trust level.
            - The Ekumen as an opt-in [[neighborhood]]
    - Documentation and other shared artifacts
        - https://miro.com/app/board/uXjVL-azEBw=/
- Information sharing about related projects and goings on
    - Other projects in this space
    - Other people who might be interested in this project or any adjacent
        - From the above: [[Erin Kissane]], [[Amy Zhang]], the CEO of OC
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
        - basadas en la conectividad real del grafo social
        - y los eventos de moderación
    - feeds de moderación
        - spam.rss
        - abuse.rss
        - etc.
    - feeds de coordinación
        - covenant.rss
        - rules.rss?
    - budas y bouncers
    - streams estrictos y laxos
- Sutty
    - [[massive wiki]] link
        - [[massive wiki builder]] ~ [[massive builder]]
- Para [[laburar]] en conjunto: https://miro.com/app/board/uXjVL-azEBw=/


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