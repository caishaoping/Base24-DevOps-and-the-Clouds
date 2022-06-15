

## after_script: 
the result won't impact the status of the job

## needs:[]: 
specify that the job can start as soon as the pipeline starts, regardless of the stage defined.

## rules: 
           rules:
             - if: $CI_COMMIT_BRANCH == $CI_DEFAULT_BRANCH
               allow_failure: false
             - if: $CI_COMMIT_BRANCH
               allow_failure: true

## extend a template's job with new stage overriden:

         In template: 
                      sast:
                      stage: test
         In consumer:
                      include:
			  - template: Security/SAST.gitlab-ci.yml 

                      # overwrite SAST job stage, use NodeJsScan scanner, and start job as soon as pipeline begins
                      sast:
                        stage: security
                        needs: []
                        variables: 
                          SAST_EXCLUDED_ANALYZERS: "eslint, bandit, brakeman, flawfinder, gosec, kubesec, mobsf, phpcs-security-audit, pmd-apex, security-code-scan, semgrep, sobelow, spotbugs"

## cache:
Different pipelines and branches in a project can share cache, but cache can't be shared across projects. https://docs.gitlab.com/ee/ci/caching/


