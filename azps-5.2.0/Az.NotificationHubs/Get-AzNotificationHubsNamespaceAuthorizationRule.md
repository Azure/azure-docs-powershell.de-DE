---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295870"
---
# <span data-ttu-id="71da7-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="71da7-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="71da7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71da7-102">SYNOPSIS</span></span>
<span data-ttu-id="71da7-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="71da7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71da7-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71da7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71da7-105">DESCRIPTION</span></span>
<span data-ttu-id="71da7-106">Das **Cmdlet "Get-AzNotificationHubsNamespaceAuthorizationRule"** gibt Informationen zu den SAS (Shared Access Signature)-Autorisierungsregeln zurück, die einem Benachrichtigungshub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="71da7-107">Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="71da7-108">Alternativ können Sie durch Einbeziehung des *Parameters "AuthorizationRule"* Informationen für eine bestimmte Regel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="71da7-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="71da7-109">Autorisierungsregeln verwalten den Zugriff auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="71da7-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="71da7-110">Dies erfolgt durch die Erstellung von Links als URIs, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="71da7-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="71da7-111">Plattformebenen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="71da7-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="71da7-112">Anhören</span><span class="sxs-lookup"><span data-stu-id="71da7-112">Listen</span></span>
- <span data-ttu-id="71da7-113">Senden</span><span class="sxs-lookup"><span data-stu-id="71da7-113">Send</span></span>
- <span data-ttu-id="71da7-114">"Clients verwalten" wird basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="71da7-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="71da7-115">Beispielsweise wird ein Client, dem die Berechtigung "Listen" erteilt wurde, für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="71da7-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="71da7-116">Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="71da7-117">Verwenden Sie Get-AzNotificationHubsNamespace, um Informationen über den Namespace selbst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="71da7-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="71da7-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71da7-118">EXAMPLES</span></span>

### <span data-ttu-id="71da7-119">Beispiel 1: Informationen zu allen Autorisierungsregeln, die Namespaces zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="71da7-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="71da7-120">Dieser Befehl ruft Informationen über alle Autorisierungsregeln ab, die sowohl dem Namespace "ContosoNamespace" als auch der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="71da7-121">Beispiel 2: Informationen zu einer Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="71da7-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="71da7-122">Dieser Befehl ruft Informationen zu einer einzelnen Namespaceautorisierungsregel namens ListenRule ab.</span><span class="sxs-lookup"><span data-stu-id="71da7-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="71da7-123">Sie müssen den Namespace und die Ressourcengruppe eingeben, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.</span><span class="sxs-lookup"><span data-stu-id="71da7-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="71da7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71da7-124">PARAMETERS</span></span>

### <span data-ttu-id="71da7-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="71da7-125">-AuthorizationRule</span></span>
<span data-ttu-id="71da7-126">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="71da7-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="71da7-127">Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Namespace haben.</span><span class="sxs-lookup"><span data-stu-id="71da7-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="71da7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71da7-128">-DefaultProfile</span></span>
<span data-ttu-id="71da7-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="71da7-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71da7-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="71da7-130">-Namespace</span></span>
<span data-ttu-id="71da7-131">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="71da7-132">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="71da7-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="71da7-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71da7-133">-ResourceGroup</span></span>
<span data-ttu-id="71da7-134">Gibt die Ressourcengruppe an, der die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="71da7-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="71da7-135">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="71da7-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="71da7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71da7-136">CommonParameters</span></span>
<span data-ttu-id="71da7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71da7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71da7-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71da7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71da7-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71da7-139">INPUTS</span></span>

### <span data-ttu-id="71da7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="71da7-140">System.String</span></span>

## <span data-ttu-id="71da7-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71da7-141">OUTPUTS</span></span>

### <span data-ttu-id="71da7-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="71da7-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="71da7-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71da7-143">NOTES</span></span>

## <span data-ttu-id="71da7-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71da7-144">RELATED LINKS</span></span>

[<span data-ttu-id="71da7-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="71da7-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="71da7-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="71da7-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="71da7-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="71da7-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="71da7-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="71da7-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


