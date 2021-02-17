---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158764"
---
# <span data-ttu-id="6d39e-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="6d39e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d39e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d39e-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d39e-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="6d39e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d39e-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d39e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d39e-105">DESCRIPTION</span></span>
<span data-ttu-id="6d39e-106">Das **Cmdlet "Get-AzNotificationHubAuthorizationRule"** ruft Informationen zu den Sas(Shared Access Signature)-Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d39e-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="6d39e-107">Das Cmdlet gibt Informationen zu allen Regeln zurück, die einem Hub zugeordnet sind, oder ruft durch Einbeziehung des Parameters *"AuthorizationRule"* Informationen zu einer bestimmten Regel ab.</span><span class="sxs-lookup"><span data-stu-id="6d39e-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="6d39e-108">Autorisierungsregeln verwalten den Zugriff auf Ihre Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="6d39e-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="6d39e-109">Eine Autorisierungsregel erstellt Links als URI, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="6d39e-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="6d39e-110">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="6d39e-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="6d39e-111">Beispielsweise wird ein Client mit der Berechtigung "Listen" für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="6d39e-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="6d39e-112">Das **Cmdlet "Get-AzNotificationHubAuthorizationRule"** ruft nur Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d39e-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="6d39e-113">Verwenden Sie Get-AzNotificationHub, um Informationen über den Hub selbst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d39e-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="6d39e-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d39e-114">EXAMPLES</span></span>

### <span data-ttu-id="6d39e-115">Beispiel 1: Informationen zu allen Autorisierungsregeln, die einem Benachrichtigungshub zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="6d39e-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="6d39e-116">Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungshub "ContosoInternalHub" im Namespace "ContosoNamespace" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6d39e-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="6d39e-117">Sie müssen den Namespace, in dem sich der Hub befindet, sowie die Ressourcengruppe angeben, der der Hub zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="6d39e-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="6d39e-118">Beispiel 2: Informationen zu Autorisierungsregeln, die einem Benachrichtigungshub zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="6d39e-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6d39e-119">Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungshub "ContosoInternalHub" im Namespace "ContosoNamespace" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6d39e-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="6d39e-120">Der Befehl verwendet den *Parameter "AuthorizationRule",* um die zurückgegebenen Daten auf eine einzelne Autorisierungsregel namens "ListenRule" zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="6d39e-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="6d39e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d39e-121">PARAMETERS</span></span>

### <span data-ttu-id="6d39e-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-122">-AuthorizationRule</span></span>
<span data-ttu-id="6d39e-123">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="6d39e-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="6d39e-124">Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Benachrichtigungshub haben.</span><span class="sxs-lookup"><span data-stu-id="6d39e-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d39e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d39e-125">-DefaultProfile</span></span>
<span data-ttu-id="6d39e-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6d39e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d39e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d39e-127">-Namespace</span></span>
<span data-ttu-id="6d39e-128">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6d39e-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6d39e-129">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="6d39e-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6d39e-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6d39e-130">-NotificationHub</span></span>
<span data-ttu-id="6d39e-131">Gibt den Benachrichtigungshub an, dem dieses Cmdlet Autorisierungsregeln zugibt.</span><span class="sxs-lookup"><span data-stu-id="6d39e-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="6d39e-132">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="6d39e-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d39e-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d39e-133">-ResourceGroup</span></span>
<span data-ttu-id="6d39e-134">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6d39e-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6d39e-135">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass die Bestandsverwaltung und die Verwaltung von Azure vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="6d39e-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6d39e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d39e-136">CommonParameters</span></span>
<span data-ttu-id="6d39e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d39e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d39e-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d39e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d39e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d39e-139">INPUTS</span></span>

### <span data-ttu-id="6d39e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6d39e-140">System.String</span></span>

## <span data-ttu-id="6d39e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d39e-141">OUTPUTS</span></span>

### <span data-ttu-id="6d39e-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6d39e-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6d39e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6d39e-143">NOTES</span></span>

## <span data-ttu-id="6d39e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6d39e-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d39e-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="6d39e-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="6d39e-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="6d39e-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d39e-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


