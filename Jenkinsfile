properties([
    parameters([
        gitParameter(branch: '',
                     branchFilter: 'origin/(.*)',
                     defaultValue: 'master',
                     description: '',
                     name: 'BRANCH',
                     quickFilterEnabled: false,
                     selectedValue: 'NONE',
                     sortMode: 'NONE',
                     tagFilter: '*',
                     type: 'PT_BRANCH')
    ])
])
node {
    stage("Clean"){
        sh "uptime"
        deleteDir()
        //sh "docker ps -q |xargs docker rm"
        //sh "docker images -q |xargs docker rmi"
    }
    //git branch: "${params.BRANCH}", url: 'https://github.com/StribPav/simple-springboot-app.git'
    stage("Git Clone"){
        sshagent(['c228f7ab-9912-4763-a485-841103a1f5f6']) {
         sh "git clone -b ${params.BRANCH} https://github.com/StribPav/simple-springboot-app.git . --depth 1"
        }
    }
    stage("Build"){
        println("Test Test Test Test")
    }
    stage("Upload to Nexus"){
        println("Test Test Test Test")
    }
    stage("Black Box test"){
        try {
            sh "return 1"
        } catch (Exception ex) {
            currentBuild.result = 'UNSTABLE'
        }
    }
    stage("Deploy"){
        println("Test Test Test Test")
    }
    stage("UiTest"){
        println("Test Test Test Test")
    }
}
