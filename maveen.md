### Maveen

## Intro

To install maveen in linux

***method 1.***

1. Install Java Development Kit (JDK):
 
       'sudo apt update'
        'sudo apt install default-jdk -y'

Verify the installation of Java:

         'java -version'

2. Install Maven Using APT:

          'sudo apt install maven -y'

After installation, you can verify the Maven installation:

          'mvn -version'

3. Manual Installation:

  If you want to install the latest version of Maven manually, follow these steps:

      1. Download Maven: Visit the Maven download page and copy the link for the binary tar.gz archive. Then use wget to download it:

           'wget https://downloads.apache.org/maven/maven-3/3.9.7/binaries/apache-maven-3.9.7-bin.tar.gz -P /tmp'

   2.Extract the Archive:

            'sudo tar xf /tmp/apache-maven-3.9.7-bin.tar.gz -C /opt'

   
 3.Create a Symbolic Link:

            'sudo ln -s /opt/apache-maven-3.9.7 /opt/maven'

 4.Set Up Environment Variables: Create a script to set the environment variables:

             'sudo nano /etc/profile.d/maven.sh'

 Add the following lines:

             ' export JAVA_HOME=/usr/lib/jvm/default-java'
              'export M2_HOME=/opt/maven'
              'export PATH=${M2_HOME}/bin:${PATH}'
                  
5.Apply the Changes:

          'source /etc/profile.d/maven.sh'

6.Verify the Installation:

         'mvn -version'


## Conclusion
Following these steps will successfully install Maven on your Linux system.