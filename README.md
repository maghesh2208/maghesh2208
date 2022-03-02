mvn -Dmigration=true -Dapp=rdpv-core -Ddb=core_1 -o;
//mvn install -Dmaven.test.skip=true -Dapp=rdpv-core -Ddb=core_1 -Denvi=development -o;
mvn -Passembly -Dmaven.test.skip=true -Ddb=core_1 -Dignoreproperties=true -Dapp=rdpv-core -Dclient=demo-newui -o

mvn install:install-file -DgroupId=org.radaptive.core -DartifactId=rdpv-core-cls-guid -Dversion=23-02-2022_65fc260 -Dpackaging=jar -Dfile=/home/ubuntu/Radaptive_New_Repo/appbuilder/target/rdpv-core-cls-guid-23-02-2022_65fc260.jar -o;


mvn install:install-file -DgroupId=org.radaptive.core -DartifactId=rdpv-core-webapp-guid -Dversion=23-02-2022_65fc260 -Dpackaging=war -Dfile=/home/ubuntu/Radaptive_New_Repo/appbuilder/target/rdpv-core-webapp-guid-23-02-2022_65fc260.war -o;


mvn -Dcore-migration=true -Dapp=rdpv-core -Ddb=RDPV_DB -o;
mvn -Dmigration=true -Dapp=rdpv-core -Ddb=RDPV_DB -o;
mvn -Dmigration=true -Dapp=rdpv-demo -Ddb=RDPV_DB -o;
mvn install -Dmaven.test.skip=true -Dapp=rdpv-demo -Ddb=RDPV_DB -Denvi=development -o;
