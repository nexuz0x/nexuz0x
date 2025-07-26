nombre: generar pacman juego

en:horario:# Ejecutar automáticamente cada 24 horas-cron:"0 */24 * * *"workflow_dispatch:# Permite la activación manualempujar:# Se ejecuta en cada envío a la rama principalsucursales:-principal
   
      
   
   
    
       

trabajos:generar:permisos:contenidos:escribircontinúa:ubuntu-últimotimeout-minutos:5
  
    
       
     
     

    pasos:-nombre:generarpacman-contribution-graph.svgusos:abozanona/pacman-contribution-graph@maincu:github_nombre_usuario:${{github.propietario_repositorio}}
         
         
        
             

      # Empuje el SVG generado a la rama de salida-nombre:pushgráfico de contribución de Pacman.svgtoelsalidasucursalusos:loco-máximo/ghaction-github-pages@v3.1.0cu:rama_objetivo:salidabuild_dir:distenv:GITHUB_TOKEN:${{secretos.GITHUB_TOKEN}}
             
         
        
           
           
        
             
