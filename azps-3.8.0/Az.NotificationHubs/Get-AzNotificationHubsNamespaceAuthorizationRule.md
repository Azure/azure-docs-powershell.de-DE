---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846332"
---
# <span data-ttu-id="b4f54-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4f54-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b4f54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4f54-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f54-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="b4f54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4f54-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f54-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4f54-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f54-106">Das Cmdlet " **Get-AzNotificationHubsNamespaceAuthorizationRule** " gibt Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) zurück, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="b4f54-107">Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="b4f54-108">Alternativ können Sie auch durch Einschließen des *AuthorizationRule* -Parameters Informationen für eine bestimmte Regel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b4f54-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="b4f54-109">Autorisierungsregeln verwalten den Zugriff auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="b4f54-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="b4f54-110">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="b4f54-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b4f54-111">Plattformebenen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="b4f54-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="b4f54-112">Hören</span><span class="sxs-lookup"><span data-stu-id="b4f54-112">Listen</span></span>
- <span data-ttu-id="b4f54-113">Senden</span><span class="sxs-lookup"><span data-stu-id="b4f54-113">Send</span></span>
- <span data-ttu-id="b4f54-114">Clients verwalten werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4f54-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b4f54-115">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4f54-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="b4f54-116">Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="b4f54-117">Wenn Sie Informationen zum Namespace selbst abrufen möchten, verwenden Sie Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="b4f54-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="b4f54-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4f54-118">EXAMPLES</span></span>

### <span data-ttu-id="b4f54-119">Beispiel 1: Abrufen von Informationen zu allen den Namespaces zugewiesenen Autorisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="b4f54-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b4f54-120">Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace-ContosoNamespace als auch der ContosoNotificationsGroup-Ressourcengruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="b4f54-121">Beispiel 2: Abrufen von Informationen zu einer Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="b4f54-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b4f54-122">Dieser Befehl ruft Informationen zu einer einzelnen Namespace Autorisierungsregel mit dem Namen ListenRule ab.</span><span class="sxs-lookup"><span data-stu-id="b4f54-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="b4f54-123">Sie müssen den Namespace und die Ressourcengruppe einbeziehen, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4f54-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="b4f54-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4f54-124">PARAMETERS</span></span>

### <span data-ttu-id="b4f54-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4f54-125">-AuthorizationRule</span></span>
<span data-ttu-id="b4f54-126">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="b4f54-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="b4f54-127">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Namespace haben.</span><span class="sxs-lookup"><span data-stu-id="b4f54-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f54-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f54-128">-DefaultProfile</span></span>
<span data-ttu-id="b4f54-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b4f54-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4f54-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b4f54-130">-Namespace</span></span>
<span data-ttu-id="b4f54-131">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b4f54-132">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="b4f54-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f54-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4f54-133">-ResourceGroup</span></span>
<span data-ttu-id="b4f54-134">Gibt die Ressourcengruppe an, der die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b4f54-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b4f54-135">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4f54-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f54-136">CommonParameters</span></span>
<span data-ttu-id="b4f54-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f54-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f54-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f54-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4f54-139">INPUTS</span></span>

### <span data-ttu-id="b4f54-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f54-140">System.String</span></span>

## <span data-ttu-id="b4f54-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4f54-141">OUTPUTS</span></span>

### <span data-ttu-id="b4f54-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b4f54-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b4f54-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4f54-143">NOTES</span></span>

## <span data-ttu-id="b4f54-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4f54-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4f54-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b4f54-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b4f54-146">Neu – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b4f54-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b4f54-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b4f54-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b4f54-148">Satz-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b4f54-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


