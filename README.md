# bashscripthomework
A home work to implement some Jfrog Artifactory REST APIs using bash script in a CLI
########################################################################################################################################

#!/bin/bash


getStorageInfo(){
        clear
        echo "Geting storage info"
        curl -X GET -H "Authorization: Bearer {TOKEN}" "https://zubi.jfrog.io/artifactory/api/storageinfo"


}

systemPing(){

        clear
        echo "System ping requested"
         curl -X GET -H "Authorization: Bearer {TOKEN}" "https://zubi.jfrog.io/artifactory/api/system/ping"


}

createUser(){

        clear
        echo "Create a user:"
        curl -X POST -H "Authorization: Bearer {TOKEN}" "https://zubi.jfrog.io/artifactory/api/v1/scim/v2/Users"


}



deleteUser(){

        clear
        echo "Delete a user:"
        curl -X DELETE -H "Authorization: Bearer {TOKEN}" "https://zubi.jfrog.io/artifactory/api/v1/scim/v2/Users/"

}


clear
echo "MENU"
echo ""
echo "1) Get Storage info"
echo "2) Ping system"
echo "3) Create a user"
echo "4) Delete a user"
echo "5) Exit"

read answer

case "$answer" in
        1) getStorageInfo;;
        2) systemPing;;
        3) createUser;;
        4) deleteUser;;
        5) exit;;


esac

###########################################################################################################################
                                                                                                                             57,0-1        Bot
