# flux-test

kubectl create ns flux

$GHUSER = "mohit-verma-1688"
fluxctl install `
--git-user=${GHUSER} `
--git-email=${GHUSER}@users.noreply.github.com `
--git-url=git@github.com:${GHUSER}/flux-test.git `
--git-path=kubernetes/configmaps,kubernetes/secrets,kubernetes/deployments `
--git-branch=main `
--namespace=flux | kubectl apply -f -
