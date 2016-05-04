# herramientas-de-ingesta-y-analisis


###Flume

```
tar zxvf apache-flume-1.6.0-bin.tar.gz
sudo mv apache-flume-1.6.0-bin/ /opt/
sudo ln -s /opt/apache-flume-1.6.0-bin /opt/flume

cd /opt/flume/lib

#librerías extra a descargar.
sudo wget http://central.maven.org/maven2/org/apache/hadoop/hadoop-core/1.2.1/hadoop-core-1.2.1.jar
sudo wget http://central.maven.org/maven2/commons-configuration/commons-configuration/1.6/commons-configuration-1.6.jar
sudo wget http://central.maven.org/maven2/net/java/dev/jets3t/jets3t/0.6.1/jets3t-0.6.1.jar
sudo wget http://central.maven.org/maven2/commons-httpclient/commons-httpclient/3.0.1/commons-httpclient-3.0.1.jar
sudo wget http://central.maven.org/maven2/commons-codec/commons-codec/1.4/commons-codec-1.4.jar

cd /opt/flume/conf

cp flume-conf.properties.template flume-conf.properties
cp flume-env.sh.template flume-env.sh
```


Agregar las siguientes variables a su .bashrc
```
###variables de flume
export FLUME_HOME=/opt/flume
export FLUME_CONF_DIR=$FLUME_HOME/conf
export FLUME_CLASSPATH=$FLUME_CONF_DIR
export PATH=$PATH:$FLUME_HOME/bin
export JAVA_HOME=/usr/lib/jvm/java-1.7.0-openjdk-amd64
```
