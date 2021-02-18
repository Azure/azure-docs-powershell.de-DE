---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5c5517faa5dbd65cc6a76a02209cb2b8c429300a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410479"
---
# <span data-ttu-id="81b23-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81b23-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="81b23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b23-102">SYNOPSIS</span></span>
<span data-ttu-id="81b23-103">Ruft Informationen zu einem Benachrichtigungshub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="81b23-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="81b23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81b23-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81b23-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81b23-105">DESCRIPTION</span></span>
<span data-ttu-id="81b23-106">**Das Get-AzNotificationHubsNamespace-Cmdlet** ruft Informationen zu Benachrichtigungshub-Namespaces ab.</span><span class="sxs-lookup"><span data-stu-id="81b23-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="81b23-107">Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen zu allen Ihren Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugewiesen sind, abrufen zu können. oder zum Zurückgeben von Informationen zu einem bestimmten Namespace.</span><span class="sxs-lookup"><span data-stu-id="81b23-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="81b23-108">Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="81b23-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="81b23-109">Sie müssen über mindestens einen Benachrichtigungshub-Namespace verfügen: Alle Benachrichtigungshubs müssen einem Namespace zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="81b23-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="81b23-110">Ein einzelner Namespace kann mehrere Hubs haben, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.</span><span class="sxs-lookup"><span data-stu-id="81b23-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="81b23-111">Sie können jedoch auch über mehrere Namespaces verfügen, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="81b23-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="81b23-112">Das **Cmdlet "Get-AzNotificationHubsNamespace"** gibt grundlegende Informationen über den Namespace selbst zurück.</span><span class="sxs-lookup"><span data-stu-id="81b23-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="81b23-113">Verwenden Sie Get-AzNotificationHubsNamespaceAuthorizationRules, um Informationen zu den Einem Namespace zugeordneten Autorisierungsregeln zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="81b23-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="81b23-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81b23-114">EXAMPLES</span></span>

### <span data-ttu-id="81b23-115">Beispiel 1: Informationen für alle Namespaces des Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="81b23-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="81b23-116">Dieser Befehl gibt Informationen für alle Namespaces des Benachrichtigungshubs zurück.</span><span class="sxs-lookup"><span data-stu-id="81b23-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="81b23-117">Beispiel 2: Informationen für einen einzelnen Benachrichtigungshub-Namespace</span><span class="sxs-lookup"><span data-stu-id="81b23-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="81b23-118">Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungshub-Namespace ab: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="81b23-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="81b23-119">Beispiel 3: Informationen für alle Benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="81b23-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="81b23-120">Dieser Befehl ruft Informationen für alle Benachrichtigungshub-Namespaces ab, die der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="81b23-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="81b23-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81b23-121">PARAMETERS</span></span>

### <span data-ttu-id="81b23-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b23-122">-DefaultProfile</span></span>
<span data-ttu-id="81b23-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="81b23-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b23-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="81b23-124">-Namespace</span></span>
<span data-ttu-id="81b23-125">Gibt einen eindeutigen Namen für den Namespace an.</span><span class="sxs-lookup"><span data-stu-id="81b23-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="81b23-126">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="81b23-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b23-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="81b23-127">-ResourceGroup</span></span>
<span data-ttu-id="81b23-128">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="81b23-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="81b23-129">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="81b23-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b23-130">CommonParameters</span></span>
<span data-ttu-id="81b23-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b23-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b23-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b23-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81b23-133">INPUTS</span></span>

### <span data-ttu-id="81b23-134">System.String</span><span class="sxs-lookup"><span data-stu-id="81b23-134">System.String</span></span>

## <span data-ttu-id="81b23-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81b23-135">OUTPUTS</span></span>

### <span data-ttu-id="81b23-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="81b23-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="81b23-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81b23-137">NOTES</span></span>

## <span data-ttu-id="81b23-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81b23-138">RELATED LINKS</span></span>


[<span data-ttu-id="81b23-139">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81b23-139">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="81b23-140">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81b23-140">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="81b23-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81b23-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


