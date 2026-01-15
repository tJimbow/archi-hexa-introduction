#### Le projet Infrastructure

```text
└── [namespace].Infrastructure/
    ├── api/
    │   └── ApiProgramAdapter.cs
    └── ProgramStore.cs 
```

<ul>
    <li class="fragment"><strong>Adaptateurs de port Driven</strong> : Implementation Ports <em>Driven</em>
        <ul>
            <li>Toujours avec un préfixe qui indique la techno utilisée.</li>
            <li class="fragment">Toujours avec le suffixe « Adapter » pour indiquer que c'est un port <em>driven</em>.</li>
            <li class="fragment">Il faut qu'un adaptateur implémente au moins un port <em>driven</em>.</li>
            <li class="fragment">Un adaptateur peut implementer plusieurs ports <em>driven</em>.</li>
        </ul>
    </li>
    <li class="fragment"><strong>Adaptateurs de port Driving</strong> : Implementation Ports <em>Driving</em>
        <ul>
            <li>Nom basé sur le nom de l'interface sans « I ».</li>
            <li class="fragment">Jamais avec le suffixe « Adapter » pour indiquer que c'est un port <em>driving</em>.</li>
            <li class="fragment">Le constructeur doit prendre les interfaces de ports <em>driven</em>.</li>
            <li class="fragment">Il faut qu'un adaptateur implémente un port <em>driving</em> uniquement.</li>
            <li class="fragment">Un adaptateur peut comprendre de la logique business.</li>
        </ul>
    </li>
</ul>
