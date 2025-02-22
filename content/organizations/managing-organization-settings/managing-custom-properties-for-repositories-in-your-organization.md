---
title: Managing custom properties for repositories in your organization
intro: 'With custom properties, you can add metadata to repositories in your organization. You can use those properties to target repositories with rulesets.'
permissions: 'Organization owners can add and set a custom property schema at the organization level. People with read permissions to a repository can view the values of custom properties for that repository.'
versions:
  feature: repository-properties
topics:
  - Repositories
shortTitle: Custom properties
---

{% note %}

**Note:** Repository properties are in public beta and subject to change.

{% endnote %}

## About custom properties

Custom properties allow you to decorate your repositories with information such as compliance frameworks, data sensitivity, or project details. Custom properties are private and can only be viewed by people with read permissions to the repository.

You can use repository properties to determine which repositories to target with a ruleset. For more information, see "[AUTOTITLE](/organizations/managing-organization-settings/creating-rulesets-for-repositories-in-your-organization#targeting-repositories-by-properties-in-your-organization)."

## Allowed characters

Custom property names and values may only contain certain characters:

- Names: `a-z`, `A-Z`, `0-9`, `_`, `-`, `$`, `#`.
- Values: All printable ASCII characters except `"`.

## Adding custom properties

You can add custom properties to your organization and set values for those properties for repositories in your organization.

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.access-custom-properties %}
1. To add a new custom property, click **New property** in the upper right corner.
1. In the "Name" field, type the name you'd like to use for your custom property. The name can't contain spaces.
1. Optionally, in the "Description" field, fill in a description of your custom property.
1. Under "Type", select the type of property you'd like to add. This can either be a string or a single select field.
1. Optionally, you can select **Require this property for all repositories** and add a default value. This means that you require that all repositories in your organization have a value for this property. Repositories that don’t have an explicit value for this property will inherit the default value.
1. Click **Save property**.

## Setting values for repositories in your organization

You can set values for custom properties for repositories in your organization.

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.access-custom-properties %}
1. Click the "Set values" tab.
1. Select one or more repositories from the list and click {% octicon "pencil" aria-hidden="true" %} **Edit properties**.

    ![Screenshot the page to set values for repositories. A button, labeled with a pencil icon and "Edit properties", is highlighted with an orange outline.](/assets/images/help/repository/edit-properties.png)

1. In the modal dialog that appears, select a value for each property you'd like to set for the selected repositories.
1. Click **Save changes**.

## Viewing values for repositories in your organization

People with read permissions to a repository can view the values of custom properties for that repository, but they can't edit those values.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
1. In the "Code and automation" section of the sidebar, click **{% octicon "tools" aria-hidden="true"%} Custom properties**.

## Searching and filtering repositories by custom properties values

You can search for repositories in your organization by custom properties values.

{% data reusables.profile.access_org %}
{% data reusables.user-settings.access_org %}
1. Under your organization name, click {% octicon "repo" aria-hidden="true" %} **Repositories**.
1. In the search bar, type `prop` to see a list of all custom properties in your organization, and select the property you'd like to search by.
