---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660110"
---
# <span data-ttu-id="1dd28-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="1dd28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dd28-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd28-103">Ruft Informationen zu einem Notification Hub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="1dd28-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="1dd28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dd28-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dd28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dd28-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd28-106">**Das Cmdlet "Get-AzNotificationHubsNamespace"** Ruft Informationen zu Notification Hub-Namespaces ab.</span><span class="sxs-lookup"><span data-stu-id="1dd28-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="1dd28-107">Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen für alle Ihre Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugeordnet sind, zu erhalten. oder um Informationen zu einem bestimmten Namespace zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1dd28-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="1dd28-108">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="1dd28-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="1dd28-109">Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen: alle benachrichtigungshubs müssen einem Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1dd28-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="1dd28-110">Ein einzelner Namespace kann mehrere Hubs beherbergen, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.</span><span class="sxs-lookup"><span data-stu-id="1dd28-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="1dd28-111">Sie können jedoch auch mehrere Namespaces haben, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="1dd28-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="1dd28-112">Das Cmdlet " **Get-AzNotificationHubsNamespace** " gibt grundlegende Informationen zum Namespace selbst zurück.</span><span class="sxs-lookup"><span data-stu-id="1dd28-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="1dd28-113">Verwenden Sie Get-AzNotificationHubsNamespaceAuthorizationRules, um Informationen zu den Autorisierungsregeln abzurufen, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1dd28-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="1dd28-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dd28-114">EXAMPLES</span></span>

### <span data-ttu-id="1dd28-115">Beispiel 1: Abrufen von Informationen für alle Notification Hub-Namespaces</span><span class="sxs-lookup"><span data-stu-id="1dd28-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="1dd28-116">Dieser Befehl gibt Informationen für alle Ihre Benachrichtigungs-Hub-Namespaces zurück.</span><span class="sxs-lookup"><span data-stu-id="1dd28-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="1dd28-117">Beispiel 2: Abrufen von Informationen für einen einzelnen Notification Hub-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="1dd28-118">Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungs-Hub-Namespace ab: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="1dd28-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="1dd28-119">Beispiel 3: Abrufen von Informationen für alle benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="1dd28-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1dd28-120">Dieser Befehl ruft Informationen für alle Notification Hub-Namespaces ab, die der Ressourcengruppe ContosoNotificationsGroup zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1dd28-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="1dd28-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dd28-121">PARAMETERS</span></span>

### <span data-ttu-id="1dd28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd28-122">-DefaultProfile</span></span>
<span data-ttu-id="1dd28-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1dd28-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd28-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-124">-Namespace</span></span>
<span data-ttu-id="1dd28-125">Gibt einen eindeutigen Namen für den Namespace an.</span><span class="sxs-lookup"><span data-stu-id="1dd28-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="1dd28-126">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="1dd28-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1dd28-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1dd28-127">-ResourceGroup</span></span>
<span data-ttu-id="1dd28-128">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1dd28-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1dd28-129">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1dd28-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1dd28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd28-130">CommonParameters</span></span>
<span data-ttu-id="1dd28-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd28-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd28-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd28-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dd28-133">INPUTS</span></span>

### <span data-ttu-id="1dd28-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd28-134">System.String</span></span>

## <span data-ttu-id="1dd28-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dd28-135">OUTPUTS</span></span>

### <span data-ttu-id="1dd28-136">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1dd28-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1dd28-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dd28-137">NOTES</span></span>

## <span data-ttu-id="1dd28-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dd28-138">RELATED LINKS</span></span>

[<span data-ttu-id="1dd28-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1dd28-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="1dd28-140">Neu – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1dd28-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1dd28-142">Satz-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1dd28-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


