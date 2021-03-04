---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: afbe8f904a8a1dad2d39a38817959e4ed4b5bad4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918187"
---
# <span data-ttu-id="e5798-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5798-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="e5798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5798-102">SYNOPSIS</span></span>
<span data-ttu-id="e5798-103">Entfernt eine Autorisierungsregel von einem Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="e5798-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="e5798-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5798-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5798-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5798-105">DESCRIPTION</span></span>
<span data-ttu-id="e5798-106">Das **Cmdlet Remove-AzNotificationHubAuthorizationRule** entfernt eine Sas-Autorisierungsregel (Shared Access Signature) aus einem Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="e5798-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="e5798-107">Autorisierungsregeln verwalten den Zugriff auf Ihre Benachrichtigungshubs durch erstellen von Links als URIs, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="e5798-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="e5798-108">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e5798-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="e5798-109">Anhören</span><span class="sxs-lookup"><span data-stu-id="e5798-109">Listen</span></span>
- <span data-ttu-id="e5798-110">Senden</span><span class="sxs-lookup"><span data-stu-id="e5798-110">Send</span></span>
- <span data-ttu-id="e5798-111">Manage Clients werden basierend auf der entsprechenden Berechtigungsstufe an eine dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="e5798-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e5798-112">Beispielsweise wird ein Client mit der Berechtigung "Anhören" an den URI geleitet, um diese Berechtigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e5798-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="e5798-113">Durch das Entfernen einer Autorisierungsregel wird auch die entsprechende Benutzerberechtigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5798-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="e5798-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5798-114">EXAMPLES</span></span>

### <span data-ttu-id="e5798-115">Beispiel 1: Entfernen einer Autorisierungsregel von einem Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="e5798-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="e5798-116">Mit diesem Befehl wird die Autorisierungsregel "ListenRule" aus dem Benachrichtigungshub namens ContosoExternalHub entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5798-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="e5798-117">Wenn Sie diesen Befehl ausführen, müssen Sie sowohl den Namespace als auch die Ressourcengruppe angeben, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e5798-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="e5798-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5798-118">PARAMETERS</span></span>

### <span data-ttu-id="e5798-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5798-119">-AuthorizationRule</span></span>
<span data-ttu-id="e5798-120">Gibt den Namen der SAS-Authentifizierungsregel an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e5798-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5798-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5798-121">-DefaultProfile</span></span>
<span data-ttu-id="e5798-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e5798-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5798-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e5798-123">-Force</span></span>
<span data-ttu-id="e5798-124">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="e5798-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5798-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5798-125">-Namespace</span></span>
<span data-ttu-id="e5798-126">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e5798-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="e5798-127">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="e5798-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e5798-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e5798-128">-NotificationHub</span></span>
<span data-ttu-id="e5798-129">Gibt den Benachrichtigungshub an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="e5798-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="e5798-130">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="e5798-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="e5798-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5798-131">-ResourceGroup</span></span>
<span data-ttu-id="e5798-132">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e5798-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e5798-133">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5798-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e5798-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5798-134">-Confirm</span></span>
<span data-ttu-id="e5798-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5798-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5798-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5798-136">-WhatIf</span></span>
<span data-ttu-id="e5798-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5798-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5798-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5798-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5798-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5798-139">CommonParameters</span></span>
<span data-ttu-id="e5798-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5798-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5798-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5798-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5798-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5798-142">INPUTS</span></span>

### <span data-ttu-id="e5798-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e5798-143">System.String</span></span>

## <span data-ttu-id="e5798-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5798-144">OUTPUTS</span></span>

### <span data-ttu-id="e5798-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5798-145">System.Void</span></span>

## <span data-ttu-id="e5798-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5798-146">NOTES</span></span>

## <span data-ttu-id="e5798-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5798-147">RELATED LINKS</span></span>

[<span data-ttu-id="e5798-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5798-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e5798-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5798-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e5798-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5798-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


