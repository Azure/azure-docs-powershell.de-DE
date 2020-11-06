---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504314"
---
# <span data-ttu-id="73688-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="73688-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="73688-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73688-102">SYNOPSIS</span></span>
<span data-ttu-id="73688-103">Ruft Informationen zu einem Notification Hub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="73688-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73688-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73688-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73688-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73688-105">DESCRIPTION</span></span>
<span data-ttu-id="73688-106">**Das Cmdlet "Get-AzureRmNotificationHubsNamespace"** Ruft Informationen zu Notification Hub-Namespaces ab.</span><span class="sxs-lookup"><span data-stu-id="73688-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="73688-107">Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen für alle Ihre Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugeordnet sind, zu erhalten. oder um Informationen zu einem bestimmten Namespace zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="73688-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="73688-108">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="73688-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="73688-109">Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen: alle benachrichtigungshubs müssen einem Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="73688-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="73688-110">Ein einzelner Namespace kann mehrere Hubs beherbergen, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.</span><span class="sxs-lookup"><span data-stu-id="73688-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="73688-111">Sie können jedoch auch mehrere Namespaces haben, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="73688-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="73688-112">Das Cmdlet " **Get-AzureRmNotificationHubsNamespace** " gibt grundlegende Informationen zum Namespace selbst zurück.</span><span class="sxs-lookup"><span data-stu-id="73688-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="73688-113">Verwenden Sie Get-AzureRmNotificationHubsNamespaceAuthorizationRules, um Informationen zu den Autorisierungsregeln abzurufen, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="73688-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="73688-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73688-114">EXAMPLES</span></span>

### <span data-ttu-id="73688-115">Beispiel 1: Abrufen von Informationen für alle Notification Hub-Namespaces</span><span class="sxs-lookup"><span data-stu-id="73688-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="73688-116">Dieser Befehl gibt Informationen für alle Ihre Benachrichtigungs-Hub-Namespaces zurück.</span><span class="sxs-lookup"><span data-stu-id="73688-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="73688-117">Beispiel 2: Abrufen von Informationen für einen einzelnen Notification Hub-Namespace</span><span class="sxs-lookup"><span data-stu-id="73688-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="73688-118">Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungs-Hub-Namespace ab: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="73688-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="73688-119">Beispiel 3: Abrufen von Informationen für alle benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="73688-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="73688-120">Dieser Befehl ruft Informationen für alle Notification Hub-Namespaces ab, die der Ressourcengruppe ContosoNotificationsGroup zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="73688-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="73688-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="73688-121">PARAMETERS</span></span>

### <span data-ttu-id="73688-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73688-122">-DefaultProfile</span></span>
<span data-ttu-id="73688-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="73688-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73688-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73688-124">-Namespace</span></span>
<span data-ttu-id="73688-125">Gibt einen eindeutigen Namen für den Namespace an.</span><span class="sxs-lookup"><span data-stu-id="73688-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="73688-126">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="73688-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="73688-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73688-127">-ResourceGroup</span></span>
<span data-ttu-id="73688-128">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="73688-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="73688-129">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73688-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="73688-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73688-130">CommonParameters</span></span>
<span data-ttu-id="73688-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73688-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73688-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73688-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73688-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73688-133">INPUTS</span></span>

### <span data-ttu-id="73688-134">System. String</span><span class="sxs-lookup"><span data-stu-id="73688-134">System.String</span></span>

## <span data-ttu-id="73688-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73688-135">OUTPUTS</span></span>

### <span data-ttu-id="73688-136">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="73688-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="73688-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="73688-137">NOTES</span></span>

## <span data-ttu-id="73688-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73688-138">RELATED LINKS</span></span>

[<span data-ttu-id="73688-139">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="73688-139">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="73688-140">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="73688-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="73688-141">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="73688-141">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="73688-142">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="73688-142">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


