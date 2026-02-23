# TASK 1: Ubuntu Container

* Run Ubuntu container
* Pass -e COLLEGE=CSE
* Show echo $COLLEGE
* Stop container  then check what happened

Pull a Ubuntu image:
```bash
docker pull ubuntu
```
Run it (with envirnment 'COLLEGE=CSE'):
```bash
docker run -it -e COLLEGE=CSE ubuntu bash
```
In Terminal, check 'COLLEGE' and stop it:
```bash
/# echo $COLLEGE
/# exit
```
Lastly check it:
```bash
docker ps -a
```
![Container Output](screenshots_and_images/Screenshot%20task-1.png)


