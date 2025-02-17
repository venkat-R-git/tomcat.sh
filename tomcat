####take amazomlinux2 while creating ec2
sudo amazon-linux-extras install java-openjdk11 -y
wget https://archive.apache.org/dist/tomcat/tomcat-10/v10.1.34/bin/apache-tomcat-10.1.34.tar.gz
tar -zxvf apache-tomcat-10.1.34.tar.gz
sudo mv apache-tomcat-10.1.34 /opt/tomcat
sudo nano /opt/tomcat/conf/tomcat-users.xml
#ADD BELOW CONTENT   
<role rolename="manager-gui"/>
  <role rolename="manager-script"/>
  <role rolename="manager-jmx"/>
  <role rolename="manager-status"/>
  <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
  <user username="deployer" password="deployer" roles="manager-script"/>
  <user username="tomcat" password="s3cret" roles="manager-gui"/>


open this 
sudo nano /opt/tomcat/webapps/manager/META-INF/context.xml
just comment the valve path, to access the manager
again go to this path
vi /opt/tomcat/webapps/host-manager/META-INF/context.xml
cmt this 
<!--<Valve className="org.apache.catalina.valves.RemoteAddrValve"
  allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" /> -->
cd /bin/
sh shutdown.sh
sh start.sh
publicip:8080
