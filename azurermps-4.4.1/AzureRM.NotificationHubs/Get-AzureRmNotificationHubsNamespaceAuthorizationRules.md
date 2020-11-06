---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: aa9b4dba29c766923966571c736c7f96a608df29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481786"
---
# <span data-ttu-id="35c37-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="35c37-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="35c37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35c37-102">SYNOPSIS</span></span>
<span data-ttu-id="35c37-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c37-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35c37-105">DESCRIPTION</span></span>
<span data-ttu-id="35c37-106">Das Cmdlet " **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** " gibt Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) zurück, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="35c37-107">Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="35c37-108">Alternativ können Sie auch durch Einschließen des *AuthorizationRule* -Parameters Informationen für eine bestimmte Regel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="35c37-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="35c37-109">Autorisierungsregeln verwalten den Zugriff auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="35c37-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="35c37-110">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="35c37-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="35c37-111">Plattformebenen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="35c37-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="35c37-112">Hören</span><span class="sxs-lookup"><span data-stu-id="35c37-112">Listen</span></span>
- <span data-ttu-id="35c37-113">Senden</span><span class="sxs-lookup"><span data-stu-id="35c37-113">Send</span></span>
- <span data-ttu-id="35c37-114">Verwalten</span><span class="sxs-lookup"><span data-stu-id="35c37-114">Manage</span></span>

<span data-ttu-id="35c37-115">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="35c37-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="35c37-116">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="35c37-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="35c37-117">Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="35c37-118">Wenn Sie Informationen zum Namespace selbst abrufen möchten, verwenden Sie Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="35c37-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="35c37-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c37-119">EXAMPLES</span></span>

### <span data-ttu-id="35c37-120">Beispiel 1: Abrufen von Informationen zu allen den Namespaces zugewiesenen Autorisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="35c37-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="35c37-121">Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace-ContosoNamespace als auch der ContosoNotificationsGroup-Ressourcengruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="35c37-122">Beispiel 2: Abrufen von Informationen zu einer Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="35c37-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="35c37-123">Dieser Befehl ruft Informationen zu einer einzelnen Namespace Autorisierungsregel mit dem Namen ListenRule ab.</span><span class="sxs-lookup"><span data-stu-id="35c37-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="35c37-124">Sie müssen den Namespace und die Ressourcengruppe einbeziehen, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.</span><span class="sxs-lookup"><span data-stu-id="35c37-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="35c37-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c37-125">PARAMETERS</span></span>

### <span data-ttu-id="35c37-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="35c37-126">-AuthorizationRule</span></span>
<span data-ttu-id="35c37-127">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="35c37-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="35c37-128">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Namespace haben.</span><span class="sxs-lookup"><span data-stu-id="35c37-128">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="35c37-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35c37-129">-Namespace</span></span>
<span data-ttu-id="35c37-130">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-130">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="35c37-131">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="35c37-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="35c37-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35c37-132">-ResourceGroup</span></span>
<span data-ttu-id="35c37-133">Gibt die Ressourcengruppe an, der die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="35c37-133">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="35c37-134">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35c37-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="35c37-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c37-135">-DefaultProfile</span></span>
<span data-ttu-id="35c37-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35c37-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c37-137">CommonParameters</span></span>
<span data-ttu-id="35c37-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c37-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c37-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c37-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35c37-140">INPUTS</span></span>

## <span data-ttu-id="35c37-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35c37-141">OUTPUTS</span></span>

### <span data-ttu-id="35c37-142">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="35c37-142">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="35c37-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="35c37-143">NOTES</span></span>

## <span data-ttu-id="35c37-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35c37-144">RELATED LINKS</span></span>

[<span data-ttu-id="35c37-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="35c37-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="35c37-146">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="35c37-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="35c37-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="35c37-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="35c37-148">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="35c37-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


