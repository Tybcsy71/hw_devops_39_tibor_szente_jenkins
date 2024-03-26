# Elvárás

GutHubról lehessen letölteni egy Jenkins file-t, amit bekonfigurálva egy Jenkinsre, majd lefuttatva, letölt egy szkriptet, ami létrehoz egy fájlt, azt elmenti artifact-ként, illetve telepít egy távoli gépre egy Apache szolgáltatást.


## A repoban található fájlok
1. **Jenkins**: Ez a Jenkins fájl, amit ne kell konfigurálni a Jenkinsen egy új jobhoz. A job Pipeline job, ami GIT-ből kerül letöltésre az alábbi beállításokkal:
    - Pipeline script from SCM
    - SCM: GIT
    - Repo URL: https://github.com/Tybcsy71/hw_devops_39_tibor_szente_jenkins.git
    - Branch: */main
    - Script Path: Jenkinsfile

2. **install_apache.sh**: Ez a fájl kerül letöltésre a job által. Létrehoz egy apache_install_date.txt fájlt a futás időpontjával, és ez elmentésre kerül artifact-ként.
    Emellett még telepítenie kellene a jenkins-slave-eb egy apache szolgáltatást, de erre már nem volt időm. Ahhoz, hogy ez működjön, SSH-val be kell tudni lépni a távoli számítógépre a szkriptből, majd feltelepíteni yum-mal az apache-t, engedélyezni a szolgáltatást. 