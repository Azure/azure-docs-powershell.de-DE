---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385075"
---
# <span data-ttu-id="94028-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94028-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="94028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94028-102">SYNOPSIS</span></span>
<span data-ttu-id="94028-103">Entfernt eine Autorisierungsregel aus einem Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="94028-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="94028-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94028-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94028-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94028-105">DESCRIPTION</span></span>
<span data-ttu-id="94028-106">Das **Cmdlet "Remove-AzNotificationHubsNamespaceAuthorizationRule"** entfernt eine SAS (Shared Access Signature)-Autorisierungsregel aus einem Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="94028-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="94028-107">Autorisierungsregeln verwalten den Zugriff auf einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="94028-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="94028-108">Dies erfolgt durch die Erstellung von Links als URIs, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="94028-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="94028-109">Berechtigungsstufen können die folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="94028-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="94028-110">Anhören</span><span class="sxs-lookup"><span data-stu-id="94028-110">Listen</span></span>
- <span data-ttu-id="94028-111">Senden</span><span class="sxs-lookup"><span data-stu-id="94028-111">Send</span></span>
- <span data-ttu-id="94028-112">"Clients verwalten" wird basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="94028-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="94028-113">Beispielsweise wird ein Client, dem die Berechtigung "Listen" erteilt wurde, für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="94028-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="94028-114">Durch das Entfernen einer Autorisierungsregel wird auch die entsprechende Benutzerberechtigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="94028-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="94028-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94028-115">EXAMPLES</span></span>

### <span data-ttu-id="94028-116">Beispiel 1: Entfernen einer Autorisierungsregel aus einem Namespace</span><span class="sxs-lookup"><span data-stu-id="94028-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="94028-117">Mit diesem Befehl wird die Autorisierungsregel "ListenRule" aus dem Namespace "ContosoNamespace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="94028-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="94028-118">Wenn Sie diesen Befehl ausführen, müssen Sie die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="94028-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="94028-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94028-119">PARAMETERS</span></span>

### <span data-ttu-id="94028-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94028-120">-AuthorizationRule</span></span>
<span data-ttu-id="94028-121">Gibt den Namen der SAS-Authentifizierungsregel an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94028-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="94028-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94028-122">-DefaultProfile</span></span>
<span data-ttu-id="94028-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="94028-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94028-124">-Force</span><span class="sxs-lookup"><span data-stu-id="94028-124">-Force</span></span>
<span data-ttu-id="94028-125">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="94028-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94028-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94028-126">-Namespace</span></span>
<span data-ttu-id="94028-127">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="94028-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="94028-128">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="94028-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="94028-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94028-129">-ResourceGroup</span></span>
<span data-ttu-id="94028-130">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="94028-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="94028-131">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="94028-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="94028-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94028-132">-Confirm</span></span>
<span data-ttu-id="94028-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94028-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94028-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="94028-134">-WhatIf</span></span>
<span data-ttu-id="94028-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94028-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94028-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94028-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94028-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94028-137">CommonParameters</span></span>
<span data-ttu-id="94028-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94028-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94028-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94028-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94028-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94028-140">INPUTS</span></span>

### <span data-ttu-id="94028-141">System.String</span><span class="sxs-lookup"><span data-stu-id="94028-141">System.String</span></span>

## <span data-ttu-id="94028-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94028-142">OUTPUTS</span></span>

### <span data-ttu-id="94028-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94028-143">System.Boolean</span></span>

## <span data-ttu-id="94028-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="94028-144">NOTES</span></span>

## <span data-ttu-id="94028-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="94028-145">RELATED LINKS</span></span>

[<span data-ttu-id="94028-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94028-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="94028-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94028-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="94028-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94028-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


