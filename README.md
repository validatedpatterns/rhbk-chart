# rhbk

<!-- markdownlint-disable MD013 -->

![Version: 0.0.3](https://img.shields.io/badge/Version-0.0.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

<!-- markdownlint-enable MD013 -->

<!-- markdownlint-disable MD013 -->

Deploys RHBK

<!-- markdownlint-enable MD013 -->

This chart is used to serve as the template for Validated Patterns Charts

## Notable changes

**Homepage:** <https://github.com/validatedpatterns/rhbk-chart>

## Maintainers

| Name                    | Email                                | Url |
| ----------------------- | ------------------------------------ | --- |
| Validated Patterns Team | <validatedpatterns@googlegroups.com> |     |

<!-- markdownlint-disable MD013 MD034 MD060 -->

## Values

| Key                                                                                         | Type   | Default                                        | Description |
| ------------------------------------------------------------------------------------------- | ------ | ---------------------------------------------- | ----------- |
| global.localClusterDomain                                                                   | string | `"apps.example.com"`                           |             |
| global.secretStore.kind                                                                     | string | `"ClusterSecretStore"`                         |             |
| global.secretStore.name                                                                     | string | `"vault-backend"`                              |             |
| keycloak.adminUser.enabled                                                                  | bool   | `true`                                         |             |
| keycloak.adminUser.passwordVaultKey                                                         | string | `"secret/data/hub/infra/keycloak/keycloak"`    |             |
| keycloak.adminUser.secretName                                                               | string | `"keycloak-admin-user"`                        |             |
| keycloak.adminUser.username                                                                 | string | `"admin"`                                      |             |
| keycloak.defaultConfig                                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.clientScopes[0].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[0].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[0].description                                           | string | `"OpenID Connect built-in scope"`              |             |
| keycloak.defaultRealm.clientScopes[0].name                                                  | string | `"openid"`                                     |             |
| keycloak.defaultRealm.clientScopes[0].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].config."id.token.claim"            | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].config."introspection.token.claim" | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].name                               | string | `"sub"`                                        |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[0].protocolMappers[0].protocolMapper                     | string | `"oidc-sub-mapper"`                            |             |
| keycloak.defaultRealm.clientScopes[1].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[1].attributes."include.in.token.scope"                   | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[1].description                                           | string | `"OpenID Connect basic scope"`                 |             |
| keycloak.defaultRealm.clientScopes[1].name                                                  | string | `"basic"`                                      |             |
| keycloak.defaultRealm.clientScopes[1].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].config."introspection.token.claim" | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].name                               | string | `"sub"`                                        |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[1].protocolMappers[0].protocolMapper                     | string | `"oidc-sub-mapper"`                            |             |
| keycloak.defaultRealm.clientScopes[2].attributes."consent.screen.text"                      | string | `"${emailScopeConsentText}"`                   |             |
| keycloak.defaultRealm.clientScopes[2].attributes."display.on.consent.screen"                | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].description                                           | string | `"OpenID Connect email scope"`                 |             |
| keycloak.defaultRealm.clientScopes[2].name                                                  | string | `"email"`                                      |             |
| keycloak.defaultRealm.clientScopes[2].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."claim.name"                | string | `"email"`                                      |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."id.token.claim"            | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."jsonType.label"            | string | `"String"`                                     |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."user.attribute"            | string | `"email"`                                      |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].config."userinfo.token.claim"      | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].name                               | string | `"email"`                                      |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[0].protocolMapper                     | string | `"oidc-usermodel-attribute-mapper"`            |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."claim.name"                | string | `"email_verified"`                             |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."id.token.claim"            | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."jsonType.label"            | string | `"boolean"`                                    |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."user.attribute"            | string | `"emailVerified"`                              |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].config."userinfo.token.claim"      | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].name                               | string | `"email verified"`                             |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[2].protocolMappers[1].protocolMapper                     | string | `"oidc-usermodel-attribute-mapper"`            |             |
| keycloak.defaultRealm.clientScopes[3].attributes."consent.screen.text"                      | string | `"${profileScopeConsentText}"`                 |             |
| keycloak.defaultRealm.clientScopes[3].attributes."display.on.consent.screen"                | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].description                                           | string | `"OpenID Connect profile scope"`               |             |
| keycloak.defaultRealm.clientScopes[3].name                                                  | string | `"profile"`                                    |             |
| keycloak.defaultRealm.clientScopes[3].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."claim.name"                | string | `"preferred_username"`                         |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."id.token.claim"            | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."jsonType.label"            | string | `"String"`                                     |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."user.attribute"            | string | `"username"`                                   |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].config."userinfo.token.claim"      | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].name                               | string | `"username"`                                   |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[0].protocolMapper                     | string | `"oidc-usermodel-attribute-mapper"`            |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].config."id.token.claim"            | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].config."userinfo.token.claim"      | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].name                               | string | `"full name"`                                  |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[3].protocolMappers[1].protocolMapper                     | string | `"oidc-full-name-mapper"`                      |             |
| keycloak.defaultRealm.clientScopes[4].attributes."consent.screen.text"                      | string | `"${rolesScopeConsentText}"`                   |             |
| keycloak.defaultRealm.clientScopes[4].attributes."display.on.consent.screen"                | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[4].attributes."include.in.token.scope"                   | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[4].description                                           | string | `"OpenID Connect roles scope"`                 |             |
| keycloak.defaultRealm.clientScopes[4].name                                                  | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clientScopes[4].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].config."claim.name"                | string | `"realm_access.roles"`                         |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].config."jsonType.label"            | string | `"String"`                                     |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].config."user.attribute"            | string | `"foo"`                                        |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].config.multivalued                 | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].name                               | string | `"realm roles"`                                |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[0].protocolMapper                     | string | `"oidc-usermodel-realm-role-mapper"`           |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[1].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[1].name                               | string | `"audience resolve"`                           |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[1].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[4].protocolMappers[1].protocolMapper                     | string | `"oidc-audience-resolve-mapper"`               |             |
| keycloak.defaultRealm.clientScopes[5].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[5].attributes."include.in.token.scope"                   | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[5].description                                           | string | `"OpenID Connect web origins scope"`           |             |
| keycloak.defaultRealm.clientScopes[5].name                                                  | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.clientScopes[5].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[5].protocolMappers[0].config."access.token.claim"        | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[5].protocolMappers[0].consentRequired                    | bool   | `false`                                        |             |
| keycloak.defaultRealm.clientScopes[5].protocolMappers[0].name                               | string | `"allowed web origins"`                        |             |
| keycloak.defaultRealm.clientScopes[5].protocolMappers[0].protocol                           | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[5].protocolMappers[0].protocolMapper                     | string | `"oidc-allowed-origins-mapper"`                |             |
| keycloak.defaultRealm.clientScopes[6].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[6].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[6].description                                           | string | `"Permission to create documents"`             |             |
| keycloak.defaultRealm.clientScopes[6].name                                                  | string | `"create:document"`                            |             |
| keycloak.defaultRealm.clientScopes[6].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[7].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[7].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[7].description                                           | string | `"Permission to read documents"`               |             |
| keycloak.defaultRealm.clientScopes[7].name                                                  | string | `"read:document"`                              |             |
| keycloak.defaultRealm.clientScopes[7].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[8].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[8].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[8].description                                           | string | `"Permission to update documents"`             |             |
| keycloak.defaultRealm.clientScopes[8].name                                                  | string | `"update:document"`                            |             |
| keycloak.defaultRealm.clientScopes[8].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clientScopes[9].attributes."display.on.consent.screen"                | string | `"false"`                                      |             |
| keycloak.defaultRealm.clientScopes[9].attributes."include.in.token.scope"                   | string | `"true"`                                       |             |
| keycloak.defaultRealm.clientScopes[9].description                                           | string | `"Permission to delete documents"`             |             |
| keycloak.defaultRealm.clientScopes[9].name                                                  | string | `"delete:document"`                            |             |
| keycloak.defaultRealm.clientScopes[9].protocol                                              | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[0].attributes."jwt.credential.issuer"                         | string | `"spiffe"`                                     |             |
| keycloak.defaultRealm.clients[0].attributes."jwt.credential.sub"                            | string | `""`                                           |             |
| keycloak.defaultRealm.clients[0].attributes."post.logout.redirect.uris"                     | string | `"+"`                                          |             |
| keycloak.defaultRealm.clients[0].clientAuthenticatorType                                    | string | `"federated-jwt"`                              |             |
| keycloak.defaultRealm.clients[0].clientId                                                   | string | `"qtodo-app"`                                  |             |
| keycloak.defaultRealm.clients[0].defaultClientScopes[0]                                     | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.clients[0].defaultClientScopes[1]                                     | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[0].defaultClientScopes[2]                                     | string | `"profile"`                                    |             |
| keycloak.defaultRealm.clients[0].defaultClientScopes[3]                                     | string | `"basic"`                                      |             |
| keycloak.defaultRealm.clients[0].defaultClientScopes[4]                                     | string | `"email"`                                      |             |
| keycloak.defaultRealm.clients[0].directAccessGrantsEnabled                                  | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[0].enabled                                                    | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[0].fullScopeAllowed                                           | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[0].name                                                       | string | `"qtodo"`                                      |             |
| keycloak.defaultRealm.clients[0].optionalClientScopes[0]                                    | string | `"offline_access"`                             |             |
| keycloak.defaultRealm.clients[0].protocol                                                   | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[0].publicClient                                               | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[0].redirectUris[0]                                            | string | `"*"`                                          |             |
| keycloak.defaultRealm.clients[0].serviceAccountsEnabled                                     | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[0].standardFlowEnabled                                        | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[0].webOrigins[0]                                              | string | `"+"`                                          |             |
| keycloak.defaultRealm.clients[1].attributes."oauth2.device.authorization.grant.enabled"     | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[1].clientId                                                   | string | `"trusted-artifact-signer"`                    |             |
| keycloak.defaultRealm.clients[1].directAccessGrantsEnabled                                  | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[1].enabled                                                    | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[1].implicitFlowEnabled                                        | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[1].name                                                       | string | `"Red Hat Trusted Artifact Signer Client"`     |             |
| keycloak.defaultRealm.clients[1].protocol                                                   | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].config."access.token.claim"             | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].config."id.token.claim"                 | string | `"false"`                                      |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].config."included.client.audience"       | string | `"trusted-artifact-signer"`                    |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].name                                    | string | `"audience-mapper"`                            |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].protocol                                | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[1].protocolMappers[0].protocolMapper                          | string | `"oidc-audience-mapper"`                       |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."access.token.claim"             | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."claim.name"                     | string | `"email_verified"`                             |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."claim.value"                    | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."id.token.claim"                 | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."jsonType.label"                 | string | `"boolean"`                                    |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].config."userinfo.token.claim"           | string | `"false"`                                      |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].consentRequired                         | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].name                                    | string | `"email-mapper"`                               |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].protocol                                | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[1].protocolMappers[1].protocolMapper                          | string | `"oidc-hardcoded-claim-mapper"`                |             |
| keycloak.defaultRealm.clients[1].publicClient                                               | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[1].redirectUris[0]                                            | string | `"*"`                                          |             |
| keycloak.defaultRealm.clients[1].redirectUris[1]                                            | string | `"urn:ietf:wg:oauth:2.0:oob"`                  |             |
| keycloak.defaultRealm.clients[1].redirectUris[2]                                            | string | `"http://localhost:*/auth/callback"`           |             |
| keycloak.defaultRealm.clients[1].standardFlowEnabled                                        | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[1].webOrigins[0]                                              | string | `"+"`                                          |             |
| keycloak.defaultRealm.clients[2].clientId                                                   | string | `"acs-central"`                                |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[0]                                     | string | `"openid"`                                     |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[1]                                     | string | `"basic"`                                      |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[2]                                     | string | `"email"`                                      |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[3]                                     | string | `"profile"`                                    |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[4]                                     | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[2].defaultClientScopes[5]                                     | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.clients[2].directAccessGrantsEnabled                                  | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[2].enabled                                                    | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[2].fullScopeAllowed                                           | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[2].implicitFlowEnabled                                        | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[2].name                                                       | string | `"Red Hat Advanced Cluster Security Central"`  |             |
| keycloak.defaultRealm.clients[2].optionalClientScopes[0]                                    | string | `"address"`                                    |             |
| keycloak.defaultRealm.clients[2].optionalClientScopes[1]                                    | string | `"phone"`                                      |             |
| keycloak.defaultRealm.clients[2].optionalClientScopes[2]                                    | string | `"offline_access"`                             |             |
| keycloak.defaultRealm.clients[2].protocol                                                   | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].config."access.token.claim"             | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].config."claim.name"                     | string | `"groups"`                                     |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].config."full.path"                      | string | `"false"`                                      |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].config."id.token.claim"                 | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].config."userinfo.token.claim"           | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].consentRequired                         | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].name                                    | string | `"groups"`                                     |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].protocol                                | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[2].protocolMappers[0].protocolMapper                          | string | `"oidc-group-membership-mapper"`               |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config."access.token.claim"             | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config."claim.name"                     | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config."id.token.claim"                 | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config."jsonType.label"                 | string | `"String"`                                     |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config."userinfo.token.claim"           | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].config.multivalued                      | string | `"true"`                                       |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].consentRequired                         | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].name                                    | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].protocol                                | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[2].protocolMappers[1].protocolMapper                          | string | `"oidc-usermodel-realm-role-mapper"`           |             |
| keycloak.defaultRealm.clients[2].publicClient                                               | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[2].redirectUris[0]                                            | string | `"*"`                                          |             |
| keycloak.defaultRealm.clients[2].secret                                                     | string | `"${ACS_CLIENT_SECRET}"`                       |             |
| keycloak.defaultRealm.clients[2].standardFlowEnabled                                        | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[2].webOrigins[0]                                              | string | `"*"`                                          |             |
| keycloak.defaultRealm.clients[3].attributes."access.token.lifespan"                         | string | `"300"`                                        |             |
| keycloak.defaultRealm.clients[3].attributes."post.logout.redirect.uris"                     | string | `"+"`                                          |             |
| keycloak.defaultRealm.clients[3].clientId                                                   | string | `"rhtpa-cli"`                                  |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[0]                                     | string | `"basic"`                                      |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[1]                                     | string | `"email"`                                      |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[2]                                     | string | `"profile"`                                    |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[3]                                     | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[4]                                     | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[5]                                     | string | `"create:document"`                            |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[6]                                     | string | `"read:document"`                              |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[7]                                     | string | `"update:document"`                            |             |
| keycloak.defaultRealm.clients[3].defaultClientScopes[8]                                     | string | `"delete:document"`                            |             |
| keycloak.defaultRealm.clients[3].directAccessGrantsEnabled                                  | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[3].enabled                                                    | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[3].fullScopeAllowed                                           | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[3].implicitFlowEnabled                                        | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[3].name                                                       | string | `"RHTPA CLI Client"`                           |             |
| keycloak.defaultRealm.clients[3].optionalClientScopes[0]                                    | string | `"address"`                                    |             |
| keycloak.defaultRealm.clients[3].optionalClientScopes[1]                                    | string | `"microprofile-jwt"`                           |             |
| keycloak.defaultRealm.clients[3].optionalClientScopes[2]                                    | string | `"offline_access"`                             |             |
| keycloak.defaultRealm.clients[3].optionalClientScopes[3]                                    | string | `"phone"`                                      |             |
| keycloak.defaultRealm.clients[3].protocol                                                   | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[3].publicClient                                               | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[3].secret                                                     | string | `"${RHTPA_CLI_SECRET}"`                        |             |
| keycloak.defaultRealm.clients[3].serviceAccountsEnabled                                     | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[3].standardFlowEnabled                                        | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[4].attributes."access.token.lifespan"                         | string | `"300"`                                        |             |
| keycloak.defaultRealm.clients[4].attributes."post.logout.redirect.uris"                     | string | `"+"`                                          |             |
| keycloak.defaultRealm.clients[4].clientId                                                   | string | `"rhtpa-frontend"`                             |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[0]                                     | string | `"basic"`                                      |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[1]                                     | string | `"email"`                                      |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[2]                                     | string | `"profile"`                                    |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[3]                                     | string | `"roles"`                                      |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[4]                                     | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[5]                                     | string | `"create:document"`                            |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[6]                                     | string | `"read:document"`                              |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[7]                                     | string | `"update:document"`                            |             |
| keycloak.defaultRealm.clients[4].defaultClientScopes[8]                                     | string | `"delete:document"`                            |             |
| keycloak.defaultRealm.clients[4].directAccessGrantsEnabled                                  | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[4].enabled                                                    | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[4].fullScopeAllowed                                           | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[4].implicitFlowEnabled                                        | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[4].name                                                       | string | `"RHTPA Frontend Client"`                      |             |
| keycloak.defaultRealm.clients[4].optionalClientScopes[0]                                    | string | `"address"`                                    |             |
| keycloak.defaultRealm.clients[4].optionalClientScopes[1]                                    | string | `"microprofile-jwt"`                           |             |
| keycloak.defaultRealm.clients[4].optionalClientScopes[2]                                    | string | `"offline_access"`                             |             |
| keycloak.defaultRealm.clients[4].optionalClientScopes[3]                                    | string | `"phone"`                                      |             |
| keycloak.defaultRealm.clients[4].protocol                                                   | string | `"openid-connect"`                             |             |
| keycloak.defaultRealm.clients[4].publicClient                                               | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[4].redirectUris[0]                                            | string | `"*"`                                          |             |
| keycloak.defaultRealm.clients[4].serviceAccountsEnabled                                     | bool   | `false`                                        |             |
| keycloak.defaultRealm.clients[4].standardFlowEnabled                                        | bool   | `true`                                         |             |
| keycloak.defaultRealm.clients[4].webOrigins[0]                                              | string | `"*"`                                          |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[0]                                         | string | `"openid"`                                     |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[1]                                         | string | `"basic"`                                      |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[2]                                         | string | `"email"`                                      |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[3]                                         | string | `"profile"`                                    |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[4]                                         | string | `"roles"`                                      |             |
| keycloak.defaultRealm.defaultDefaultClientScopes[5]                                         | string | `"web-origins"`                                |             |
| keycloak.defaultRealm.displayName                                                           | string | `"ZTVP Realm"`                                 |             |
| keycloak.defaultRealm.enabled                                                               | bool   | `true`                                         |             |
| keycloak.defaultRealm.realm                                                                 | string | `"ztvp"`                                       |             |
| keycloak.defaultRealm.registrationAllowed                                                   | bool   | `false`                                        |             |
| keycloak.defaultRealm.roles.realm[0].description                                            | string | `"QTodo App Administrator"`                    |             |
| keycloak.defaultRealm.roles.realm[0].name                                                   | string | `"qtodo-admin"`                                |             |
| keycloak.defaultRealm.roles.realm[1].description                                            | string | `"Read-only access"`                           |             |
| keycloak.defaultRealm.roles.realm[1].name                                                   | string | `"viewer"`                                     |             |
| keycloak.defaultRealm.roles.realm[2].description                                            | string | `"RHTPA SBOM Creator"`                         |             |
| keycloak.defaultRealm.roles.realm[2].name                                                   | string | `"create:sbom"`                                |             |
| keycloak.defaultRealm.roles.realm[3].description                                            | string | `"RHTPA Document Creator"`                     |             |
| keycloak.defaultRealm.roles.realm[3].name                                                   | string | `"create:document"`                            |             |
| keycloak.defaultRealm.roles.realm[4].description                                            | string | `"ACS Administrator"`                          |             |
| keycloak.defaultRealm.roles.realm[4].name                                                   | string | `"acs-admin"`                                  |             |
| keycloak.defaultRealm.users[0].createdTimestamp                                             | int    | `1`                                            |             |
| keycloak.defaultRealm.users[0].credentials[0].temporary                                     | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[0].credentials[0].type                                          | string | `"password"`                                   |             |
| keycloak.defaultRealm.users[0].credentials[0].value                                         | string | `"${QTODO_ADMIN_PASSWORD}"`                    |             |
| keycloak.defaultRealm.users[0].email                                                        | string | `"qtodo-admin@example.com"`                    |             |
| keycloak.defaultRealm.users[0].emailVerified                                                | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[0].enabled                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[0].firstName                                                    | string | `"QTodo"`                                      |             |
| keycloak.defaultRealm.users[0].lastName                                                     | string | `"Admin"`                                      |             |
| keycloak.defaultRealm.users[0].realmRoles[0]                                                | string | `"qtodo-admin"`                                |             |
| keycloak.defaultRealm.users[0].requiredActions[0]                                           | string | `"UPDATE_PASSWORD"`                            |             |
| keycloak.defaultRealm.users[0].username                                                     | string | `"qtodo-admin"`                                |             |
| keycloak.defaultRealm.users[1].createdTimestamp                                             | int    | `1`                                            |             |
| keycloak.defaultRealm.users[1].credentials[0].temporary                                     | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[1].credentials[0].type                                          | string | `"password"`                                   |             |
| keycloak.defaultRealm.users[1].credentials[0].value                                         | string | `"${QTODO_USER1_PASSWORD}"`                    |             |
| keycloak.defaultRealm.users[1].email                                                        | string | `"qtodo-user1@example.com"`                    |             |
| keycloak.defaultRealm.users[1].emailVerified                                                | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[1].enabled                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[1].firstName                                                    | string | `"QTodo"`                                      |             |
| keycloak.defaultRealm.users[1].lastName                                                     | string | `"User-1"`                                     |             |
| keycloak.defaultRealm.users[1].realmRoles[0]                                                | string | `"viewer"`                                     |             |
| keycloak.defaultRealm.users[1].requiredActions[0]                                           | string | `"UPDATE_PASSWORD"`                            |             |
| keycloak.defaultRealm.users[1].username                                                     | string | `"qtodo-user1"`                                |             |
| keycloak.defaultRealm.users[2].createdTimestamp                                             | int    | `1`                                            |             |
| keycloak.defaultRealm.users[2].credentials[0].temporary                                     | bool   | `false`                                        |             |
| keycloak.defaultRealm.users[2].credentials[0].type                                          | string | `"password"`                                   |             |
| keycloak.defaultRealm.users[2].credentials[0].value                                         | string | `"${RHTAS_USER_PASSWORD}"`                     |             |
| keycloak.defaultRealm.users[2].email                                                        | string | `"rhtas-user@example.com"`                     |             |
| keycloak.defaultRealm.users[2].emailVerified                                                | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[2].enabled                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[2].firstName                                                    | string | `"RHTAS"`                                      |             |
| keycloak.defaultRealm.users[2].lastName                                                     | string | `"Signer"`                                     |             |
| keycloak.defaultRealm.users[2].realmRoles[0]                                                | string | `"viewer"`                                     |             |
| keycloak.defaultRealm.users[2].username                                                     | string | `"rhtas-user"`                                 |             |
| keycloak.defaultRealm.users[3].createdTimestamp                                             | int    | `1`                                            |             |
| keycloak.defaultRealm.users[3].credentials[0].temporary                                     | bool   | `false`                                        |             |
| keycloak.defaultRealm.users[3].credentials[0].type                                          | string | `"password"`                                   |             |
| keycloak.defaultRealm.users[3].credentials[0].value                                         | string | `"${RHTPA_USER_PASSWORD}"`                     |             |
| keycloak.defaultRealm.users[3].email                                                        | string | `"rhtpa-user@example.com"`                     |             |
| keycloak.defaultRealm.users[3].emailVerified                                                | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[3].enabled                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[3].firstName                                                    | string | `"RHTPA"`                                      |             |
| keycloak.defaultRealm.users[3].lastName                                                     | string | `"User"`                                       |             |
| keycloak.defaultRealm.users[3].realmRoles[0]                                                | string | `"viewer"`                                     |             |
| keycloak.defaultRealm.users[3].realmRoles[1]                                                | string | `"create:sbom"`                                |             |
| keycloak.defaultRealm.users[3].realmRoles[2]                                                | string | `"create:document"`                            |             |
| keycloak.defaultRealm.users[3].username                                                     | string | `"rhtpa-user"`                                 |             |
| keycloak.defaultRealm.users[4].createdTimestamp                                             | int    | `1`                                            |             |
| keycloak.defaultRealm.users[4].credentials[0].temporary                                     | bool   | `false`                                        |             |
| keycloak.defaultRealm.users[4].credentials[0].type                                          | string | `"password"`                                   |             |
| keycloak.defaultRealm.users[4].credentials[0].value                                         | string | `"${ACS_ADMIN_PASSWORD}"`                      |             |
| keycloak.defaultRealm.users[4].email                                                        | string | `"admin@example.com"`                          |             |
| keycloak.defaultRealm.users[4].emailVerified                                                | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[4].enabled                                                      | bool   | `true`                                         |             |
| keycloak.defaultRealm.users[4].firstName                                                    | string | `"ACS"`                                        |             |
| keycloak.defaultRealm.users[4].lastName                                                     | string | `"Administrator"`                              |             |
| keycloak.defaultRealm.users[4].realmRoles[0]                                                | string | `"acs-admin"`                                  |             |
| keycloak.defaultRealm.users[4].realmRoles[1]                                                | string | `"offline_access"`                             |             |
| keycloak.defaultRealm.users[4].username                                                     | string | `"admin"`                                      |             |
| keycloak.ingress.enabled                                                                    | bool   | `true`                                         |             |
| keycloak.ingress.hostname                                                                   | string | `""`                                           |             |
| keycloak.ingress.service                                                                    | string | `"keycloak-service-trusted"`                   |             |
| keycloak.ingress.termination                                                                | string | `"reencrypt"`                                  |             |
| keycloak.name                                                                               | string | `"keycloak"`                                   |             |
| keycloak.oidcSecrets.acsClient.vaultPath                                                    | string | `"secret/data/hub/infra/acs/acs-central"`      |             |
| keycloak.oidcSecrets.qtodo.enabled                                                          | bool   | `false`                                        |             |
| keycloak.oidcSecrets.qtodo.vaultPath                                                        | string | `"secret/data/apps/qtodo/qtodo-oidc-client"`   |             |
| keycloak.oidcSecrets.rhtpaCli.vaultPath                                                     | string | `"secret/data/hub/infra/rhtpa/rhtpa-oidc-cli"` |             |
| keycloak.postgresqlDb.database                                                              | string | `"keycloak"`                                   |             |
| keycloak.postgresqlDb.passwordVaultKey                                                      | string | `"secret/data/hub/infra/keycloak/keycloak"`    |             |
| keycloak.postgresqlDb.secretName                                                            | string | `"postgresql-db"`                              |             |
| keycloak.postgresqlDb.username                                                              | string | `"keycloak"`                                   |             |
| keycloak.realms                                                                             | list   | `[]`                                           |             |
| keycloak.spiffeIdentityProvider.config.alias                                                | string | `"spiffe"`                                     |             |
| keycloak.spiffeIdentityProvider.config.config.authorizationUrl                              | string | `""`                                           |             |
| keycloak.spiffeIdentityProvider.config.config.clientId                                      | string | `"keycloak"`                                   |             |
| keycloak.spiffeIdentityProvider.config.config.clientSecret                                  | string | `"unused"`                                     |             |
| keycloak.spiffeIdentityProvider.config.config.issuer                                        | string | `""`                                           |             |
| keycloak.spiffeIdentityProvider.config.config.jwksUrl                                       | string | `""`                                           |             |
| keycloak.spiffeIdentityProvider.config.config.supportsClientAssertionReuse                  | string | `"true"`                                       |             |
| keycloak.spiffeIdentityProvider.config.config.supportsClientAssertions                      | string | `"true"`                                       |             |
| keycloak.spiffeIdentityProvider.config.config.syncMode                                      | string | `"LEGACY"`                                     |             |
| keycloak.spiffeIdentityProvider.config.config.tokenUrl                                      | string | `""`                                           |             |
| keycloak.spiffeIdentityProvider.config.config.useJwksUrl                                    | string | `"true"`                                       |             |
| keycloak.spiffeIdentityProvider.config.config.validateSignature                             | string | `"true"`                                       |             |
| keycloak.spiffeIdentityProvider.config.displayName                                          | string | `"SPIFFE Workload Identity"`                   |             |
| keycloak.spiffeIdentityProvider.config.enabled                                              | bool   | `true`                                         |             |
| keycloak.spiffeIdentityProvider.config.hideOnLogin                                          | bool   | `true`                                         |             |
| keycloak.spiffeIdentityProvider.config.providerId                                           | string | `"oidc"`                                       |             |
| keycloak.spiffeIdentityProvider.enabled                                                     | bool   | `true`                                         |             |
| keycloak.tls.secret                                                                         | string | `"keycloak-tls"`                               |             |
| keycloak.tls.serviceServing                                                                 | bool   | `true`                                         |             |
| keycloak.users.passwordVaultKey                                                             | string | `"secret/data/hub/infra/users/keycloak-users"` |             |
| keycloak.users.secretName                                                                   | string | `"keycloak-users"`                             |             |

<!-- markdownlint-enable MD013 MD034 MD060 -->

---

Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
