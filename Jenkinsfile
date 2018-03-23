@Library('jenkins-library')

def podName = 'vpt-node-deployment'
def buildType = 'node'
def testFolder = ''

def pipeline = new devops.vptPipelinev1()
def additionalRepos = [ : ]

node('docker') {
  withEnv(["TEST_OPTS=pipeline"]) {
    pipeline.runStandardPipeline(podName, buildType, testFolder, additionalRepos)
  }
}
