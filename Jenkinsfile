podTemplate(name: 'some-slave2', label: 'some-slave2', cloud: 'openshift', serviceAccount: 'jenkins',
    containers: [
        // This adds the custom slave container to the pod. Must be first with name 'jnlp'
        containerTemplate(name: 'jnlp',
            image: '172.30.1.1:5000/continuous-infra/jenkins-continuous-infra-slave',
            ttyEnabled: false,
            args: '${computer.jnlpmac} ${computer.name}',
            command: '',
            workingDir: '/tmp')
    ], idleMinutes: 1) {

    node('some-slave2') {
      sleep 10
    }

}
