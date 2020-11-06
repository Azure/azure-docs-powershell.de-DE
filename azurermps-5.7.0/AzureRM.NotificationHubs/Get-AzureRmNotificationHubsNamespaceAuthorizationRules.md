---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505437"
---
# <span data-ttu-id="b1aa6-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b1aa6-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="b1aa6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1aa6-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1aa6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1aa6-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1aa6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="b1aa6-106">Das Cmdlet " **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** " gibt Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) zurück, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="b1aa6-107">Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="b1aa6-108">Alternativ können Sie auch durch Einschließen des *AuthorizationRule* -Parameters Informationen für eine bestimmte Regel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="b1aa6-109">Autorisierungsregeln verwalten den Zugriff auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="b1aa6-110">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b1aa6-111">Plattformebenen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="b1aa6-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="b1aa6-112">Hören</span><span class="sxs-lookup"><span data-stu-id="b1aa6-112">Listen</span></span>
- <span data-ttu-id="b1aa6-113">Senden</span><span class="sxs-lookup"><span data-stu-id="b1aa6-113">Send</span></span>
- <span data-ttu-id="b1aa6-114">Verwalten</span><span class="sxs-lookup"><span data-stu-id="b1aa6-114">Manage</span></span>

<span data-ttu-id="b1aa6-115">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b1aa6-116">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="b1aa6-117">Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="b1aa6-118">Wenn Sie Informationen zum Namespace selbst abrufen möchten, verwenden Sie Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="b1aa6-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1aa6-119">EXAMPLES</span></span>

### <span data-ttu-id="b1aa6-120">Beispiel 1: Abrufen von Informationen zu allen den Namespaces zugewiesenen Autorisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="b1aa6-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b1aa6-121">Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace-ContosoNamespace als auch der ContosoNotificationsGroup-Ressourcengruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="b1aa6-122">Beispiel 2: Abrufen von Informationen zu einer Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="b1aa6-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b1aa6-123">Dieser Befehl ruft Informationen zu einer einzelnen Namespace Autorisierungsregel mit dem Namen ListenRule ab.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="b1aa6-124">Sie müssen den Namespace und die Ressourcengruppe einbeziehen, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="b1aa6-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1aa6-125">PARAMETERS</span></span>

### <span data-ttu-id="b1aa6-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b1aa6-126">-AuthorizationRule</span></span>
<span data-ttu-id="b1aa6-127">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="b1aa6-128">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Namespace haben.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-128">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1aa6-129">-DefaultProfile</span></span>
<span data-ttu-id="b1aa6-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1aa6-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa6-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1aa6-131">-Namespace</span></span>
<span data-ttu-id="b1aa6-132">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b1aa6-133">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa6-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1aa6-134">-ResourceGroup</span></span>
<span data-ttu-id="b1aa6-135">Gibt die Ressourcengruppe an, der die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="b1aa6-136">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1aa6-137">CommonParameters</span></span>
<span data-ttu-id="b1aa6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1aa6-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1aa6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1aa6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1aa6-140">INPUTS</span></span>

### <span data-ttu-id="b1aa6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="b1aa6-141">None</span></span>
<span data-ttu-id="b1aa6-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b1aa6-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1aa6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1aa6-143">OUTPUTS</span></span>

### <span data-ttu-id="b1aa6-144">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="b1aa6-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="b1aa6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1aa6-145">NOTES</span></span>

## <span data-ttu-id="b1aa6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1aa6-146">RELATED LINKS</span></span>

[<span data-ttu-id="b1aa6-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b1aa6-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="b1aa6-148">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b1aa6-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="b1aa6-149">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b1aa6-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="b1aa6-150">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b1aa6-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


