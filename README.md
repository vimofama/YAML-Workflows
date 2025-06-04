# YAML-Workflows

- Mapas / Diccionarios

```yaml
persona:
  nombre: Juan
  edad: 30
```

- Listas de valores

```yml
usuarios:
  - nombre: Ana
    edad: 30
  - nombre: Luis
    edad: 25
```

- Modificadores Sring multilínea
```yml
mensaje: |
  Hola,
  Esto es un texto multilínea.
```

```yml
texto: >
  Esta es una línea
  que continuará en la siguiente.

# Esta es una línea que continuará en la siguiente
```

- Herencia
```yml
defaults: &defaults
  color: blue
  size: medium

item1:
  <<:: *defaults
  color: red

item2:
  <<: *defaults
  size: small

# item1 hereda de defaults y sobrescribe color.
# item2 hereda de defaults y sobrescribe size.
```


## GitHub actions
### Conceptos

- **Workflow**: Un archivo YAML que define una serie de acciones que se ejecutan automáticamente en respuesta a eventos.

- **Event**: Un disparador que inicia un workflow.

- **Job**: Una unidad de trabajo dentro de un workflow. Un workflow puede tener varios jobs, y cada uno de ellos puede ejecutarse en paralelo o secuencialmente.

- **Step**: Una acción individual dentro de un job.

- **Action**: Un bloque de código reutilizable que realiza una tarea específica en un step.

- **Runner**: Un entorno donde se ejecutan los jobs.