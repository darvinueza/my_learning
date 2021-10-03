# Despliegue desde una imagen. Parte 2

## COMANDOS

    # oc get all -o name -l app=blog
    # oc get svc blog
    # oc expose svc blog
    # oc get route blog
    # oc get all -o name -l app=blog
    # oc describe route blog
    # oc scale --replicas=3 deployment blog
