---
title: Authorizing a personal access token for use with single sign-on
intro: 'To use a {% data variables.product.pat_v1 %} with an organization that uses single sign-on (SSO), you must first authorize the token.'
redirect_from:
  - /articles/authorizing-a-personal-access-token-for-use-with-a-saml-single-sign-on-organization
  - /articles/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on
  - /github/authenticating-to-github/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on
  - /github/authenticating-to-github/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on
  - /authentication/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on
versions:
  ghec: '*'
topics:
  - SSO
shortTitle: '{% data variables.product.pat_generic_caps %} with SSO'
---
You must authorize your {% data variables.product.pat_v1 %} after creation before the token can access an organization that uses SAML single sign-on (SSO). Access to `internal` resources (repositories, projects, and packages) in an enterprise requires an SSO authorization for an organization within an enterprise. For more information about creating a new {% data variables.product.pat_v1 %}, see [AUTOTITLE](/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token). {% data variables.product.pat_v2_caps %}s are authorized during token creation, before access to the organization is granted.

{% data reusables.saml.must-authorize-linked-identity %}

{% data reusables.saml.authorized-creds-info %}

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.developer_settings %}
{% data reusables.user-settings.personal_access_tokens %}

1. Next to the token you'd like to authorize, click **Configure SSO**. {% data reusables.saml.authenticate-with-saml-at-least-once %}

   ![Screenshot of a list entry for a {% data variables.product.pat_v1 %}. A dropdown menu, labeled "Configure SSO", is outlined in orange.](/assets/images/help/settings/sso-allowlist-button.png)

1. In the dropdown menu, to the right of the organization you'd like to authorize the token for, click **Authorize**.

> [!NOTE]
> When authorizing a {% data variables.product.pat_v1 %} for use within an organization that belongs to an enterprise which has both an IP allow list and single sign-on enabled at the enterprise level, your IP must also be allowed at the enterprise level. See [AUTOTITLE](/admin/configuring-settings/hardening-security-for-your-enterprise/restricting-network-traffic-to-your-enterprise-with-an-ip-allow-list).

## Further reading

* [AUTOTITLE](/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
* [AUTOTITLE](/authentication/authenticating-with-single-sign-on/about-authentication-with-single-sign-on)
