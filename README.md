## JFrog Gradle Artifactoryプラグイン利用手順

* ### 前提条件は以下の通り
&emsp;1. リリース用リポジトリ名はgradle-snapshot-local  
&emsp;2. スナップショット用リポジトリ名はgradle-release-local  
&emsp;3. gradle.propertiesの各種パラメータを環境に合わせて設定

* ### 以下のアーティファクトを作成し、Artifactoryにアップロードする
&emsp;1. Javaアプリケーションをビルドしたjarファイル  
&emsp;2. ビルドしたjarファイルは実行可能  
&emsp;3. Javaアプリケーションソースのjarファイル  
&emsp;4. Javaアプリケーションのjavadocのjarファイル  

* ### 利用方法
&emsp;1. GitHubに保存しているソースのクローン  
&emsp;&emsp;`git clone https://github.com/iwahi01/jfrog-gradle.git`
    
&emsp;2. ソースのビルド、デプロイ及びArtifactoryへのアップロード(以下はUNIX環境の場合)  
&emsp;&emsp;`./gradlew artifactoryPublish`　 

&emsp;&emsp;*Jenkinsで実行する場合のGoals and optionsの指定内容は以下の通り*  
&emsp;&emsp;`artifactoryPublish`  

&emsp;3. ビルドした実行可能jarファイルを実行する場合は引数には標準出力に出力する文字列を指定して実行  
&emsp;&emsp;`java -jar 実行可能jarファイル.jar 標準出力文字列`  
### ※以下はMavenプラグインとの違い
&emsp;1. Adminのリポジトリ設定でRepository LayoutをGradle-defaultを使用した場合はSNAPSHOTがバージョン管理できない為、maven-2-defaultを使用することで対応可能  
&emsp;2. ArtifactoryのBuildsページのURLはMavenプラグインでは表示されるがGradleプラグインでは表示されない  

## 各製品の設定内容

* ### Jenkins
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle01.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle02.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle03.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle04.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle05.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle06.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle07.png)
![Jenkins](https://github.com/iwahi01/jfrog-gradle/wiki/images/jenkins-gradle08.png)

* ### GitLab
![GitLab](https://github.com/iwahi01/jfrog-gradle/wiki/images/gitlab-gradle01.png)
![GitLab](https://github.com/iwahi01/jfrog-gradle/wiki/images/gitlab-gradle02.png)
![GitLab](https://github.com/iwahi01/jfrog-gradle/wiki/images/gitlab-gradle03.png)

* ### Artifactory
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle01.png)
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle02.png)
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle03.png)
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle04.png)
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle05.png)
![Artifactory](https://github.com/iwahi01/jfrog-gradle/wiki/images/artifactory-gradle06.png)

* ### Eclipse
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle01.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle02.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle03.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle04.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle05.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle06.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle07.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle08.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle09.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle10.png)
![Eclipse](https://github.com/iwahi01/jfrog-gradle/wiki/images/eclipse-gradle11.png)
