# Laboratorio01

Las paginas fueron construidas, desplegadas, verificadas y dadas de baja. Funcionó correctamente.

Los comandos necesarios para la construccion son 

- Para la web01:

        docker build -f src/web01/DOCKERFILE -t web-01 ./src/web01
    
- Para la web02: 

        docker build -f src/web02/DOCKERFILE -t web-02 ./src/web02

    Se especificó que al momento de la construccion se centre en el archivo DOCKERFILE en mayusculas, puesto que, cuando lo probé sin especificar eso, me salia error. La resupuesta que consegui fue que cuando se ejecuta sin especificar, Docker busca el archivo por defecto Dockerfile en minusculas.

Los comandos para el despliegue

- Para la web 01: 
        
        docker run -d --name cont-web01 -p 4000:80 web-01
    
- Para la web 02: 

        docker run -d --name cont-web02 -p 4001:80 web-02

Los comandos para detener los contenedores:

    docker stop cont-web01 cont-web02