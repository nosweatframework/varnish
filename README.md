# varnish

This is a base for Kustomize overlay stacks.

<hr />

[No Sweat Cloud](https://nosweat.cloud) is a group providing managed services for specific open source applications and an easy to use public cloud tailored for small businesses.

This repository is part of many repositories we use our selves. We trust our work so much, that we open source it to inspire others.

<hr />

Your overlay should be the stack to deploy the full system, where you define any specific deployment, like your application.

Some of No Sweat Framework's bases are for open source web applications like Magento, WordPress or Drupal, but make sure to point to your own built application image. Use the Dockerfiles repository for a source of examples.

Use this like:

```bash
mkdir staging
cat <<EOF > staging/kustomization.yaml
bases:
- ../basename1
- ../basename2
namespace: project-stating
EOF

mkdir production
cat <<EOF > prod/kustomization.yaml
bases:
- ../basename1
- ../basename2
namespace: project-production
EOF
```
