#### Le projet Domain

```text
└── [namespace].Domain/
    ├── port/
    │   ├── driven/
    │   │   └── IInboundProgramPort.cs (Secondary Port)
    │   └── driving/
    │       └── IProgramStore.cs (Primary Port)
    └── Program.cs (Domain Object)
```

<ul>
    <li class="fragment"><strong>Ports Driven</strong> :
        <ul>
            <li>Souvent avec le préfixe « Inbound » ou « Outbound » pour indiquer le sens du port.</li>
            <li class="fragment">Toujours avec le suffixe « Port » pour indiquer comme un port <em>driven</em>.</li>
        </ul>
    </li>
    <li class="fragment"><strong>Ports Driving</strong> :
        <ul>
            <li>Sans préfixe/suffixe.</li>
            <li class="fragment">Les contrat pour les objets qui communique en utilisant nos ports <em>driven</em>.</li>
        </ul>
    </li>
    <li class="fragment"><strong>Objets de domaine</strong> :
        <ul>
            <li class="fragment">Le langage interne de notre component.</li>
            <li class="fragment">On transforme tout objet qui rentre en objet de domaine.</li>
            <li class="fragment">Par extension de ce principle, on transforme tout objet de domaine qui sort au niveau des ports <em>driven</em>.</li>
            <li class="fragment">Pas forcement un objet qu'on stocke dans une base.</li>
        </ul>
    </li>
</ul>
