# flux-test

kubectl create ns flux

$GHUSER = "mohit-verma-1688"
fluxctl install `
--git-user=${GHUSER} `
--git-email=${GHUSER}@users.noreply.github.com `
--git-url=git@github.com:${GHUSER}/flux-test.git `
--git-path=kubernetes/configmaps,kubernetes/secrets`
--git-branch=main `
--namespace=flux | kubectl apply -f -



flux bootstrap git \
  --url=https://github.com/Mohit-Verma-1688/flux-test.git \
  --username=mohit-verma-1688 \
  --password=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 \
  --token-auth=true \
  --path=
