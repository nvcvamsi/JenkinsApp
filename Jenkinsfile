node{

   def tomcatWeb = 'D:\\apache-tomcat-10.0.5\\webapps'
   def tomcatBin = 'D:\\apache-tomcat-10.0.5\\bin'
   def sourceFilePath= 'D:\\Jenkins'
   def CATALINA_HOME= 'D:\\apache-tomcat-10.0.5'
   def tomcatStatus = ''
   stage('SCM Checkout'){
     git 'https://github.com/nvcvamsi/JenkinsPipelineDemo.git'
   }

   stage('Deploy to Tomcat'){
     bat "copy ${sourceFilePath}\\Jenkins.war \"${tomcatWeb}\\Jenkins.war\""
   }
      stage ('Start Tomcat Server') {
         sleep(time:5,unit:"SECONDS") 
         bat "${tomcatBin}\\startup.bat"
         sleep(time:100,unit:"SECONDS")
   }
}
