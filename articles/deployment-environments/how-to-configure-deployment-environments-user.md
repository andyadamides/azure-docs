---
title: Provide user access to Azure Deployment Environments projects
titleSuffix: Azure Deployment Environments
description: Learn how to configure access to projects for developers by using the Deployment Environments User built-in role.
ms.service: deployment-environments
ms.custom: ignite-2022
ms.author: rosemalcolm
author: RoseHJM
ms.date: 12/05/2023
ms.topic: how-to
---

# Provide access to projects for developers

This guide explains how to provide user access for Azure Deployment Environments projects.

In Azure Deployment Environments, development team members must have access to a project before they can create deployment environments. By using the built-in roles, Deployment Environments User and Deployment Environments Reader, you can assign permissions to users or groups at either the project level or the environment type level.

When assigned at the project level, a developer who has the Deployment Environments User role can perform the following actions on all enabled project environment types:

* View the project environment types.
* Create an environment.
* Read, write, delete, or perform actions (like deploy or reset) on their own environment.

A developer who has the Deployment Environments Reader role can:

* Read environments that other users created.

When you assign a role to specific environment types, the user can perform the actions only on the respective environment types.

## Assign permissions to developers for a project

1. Sign in to the [Azure portal](https://portal.azure.com) and go to Azure Deployment Environments.

1. Select **Projects** from the left pane, then choose the project that you want your developers to be able to access.

1. Select **Access control (IAM)** from the left pane.

1. Select **Add** > **Add role assignment**.

1. Assign the following role. For detailed steps, see [Assign Azure roles using the Azure portal](../role-based-access-control/role-assignments-portal.md).

    | Setting | Value |
    | --- | --- |
    | **Role** | Select **[Deployment Environments User](how-to-configure-deployment-environments-user.md)**. |
    | **Assign access to** | Select **User, group, or service principal**. |
    | **Members** | Select the users or groups you want to have access to the project. |

    :::image type="content" source="media/quickstart-create-configure-projects/add-role-assignment.png" alt-text="Screenshot that shows the Add role assignment pane." lightbox="media/quickstart-create-configure-projects/add-role-assignment.png":::

The users can now view the project and all the environment types enabled within it. Users who have the Deployment Environments User role can [create environments in the developer portal](./quickstart-create-access-environments.md).

## Assign permissions to developers for an environment type

1. Sign in to the [Azure portal](https://portal.azure.com) and go to Azure Deployment Environments.

1. Select **Projects** from the left pane, then choose the project that you want your developers to be able to access.

1. Select **Environment types** from the left pane, and then select the ellipsis (**...**) beside the specific environment type.

   :::image type="content" source="media\configure-deployment-environments-user\project-environment-types.png" alt-text="Screenshot that shows the environment types associated with a project." lightbox="media\configure-deployment-environments-user\project-environment-types.png":::

1. Select **Access control**.

1. Select **Add** > **Add role assignment**.

1. Assign the following role. For detailed steps, see [Assign Azure roles using the Azure portal](../role-based-access-control/role-assignments-portal.md).

    | Setting | Value |
    | --- | --- |
    | **Role** | Select **[Deployment Environments User](how-to-configure-deployment-environments-user.md)**. |
    | **Assign access to** | Select **User, group, or service principal**. |
    | **Members** | Select the users or groups you want to have access to the project. |

    :::image type="content" source="media/quickstart-create-configure-projects/add-role-assignment.png" alt-text="Screenshot that shows the Add role assignment pane for environment type." lightbox="media/quickstart-create-configure-projects/add-role-assignment.png":::

The users can now view the project and the specific environment type that you granted them access to. Users who have the Deployment Environments User role can also [create environments in the developer portal](./quickstart-create-access-environments.md).

[!INCLUDE [note-deployment-environments-user](includes/note-deployment-environments-user.md)]

## Related content

* [Create and configure an Azure Deployment Environments project](./quickstart-create-and-configure-projects.md)
* [Provide access for dev team leads to Deployment Environments projects](./how-to-configure-project-admin.md)
