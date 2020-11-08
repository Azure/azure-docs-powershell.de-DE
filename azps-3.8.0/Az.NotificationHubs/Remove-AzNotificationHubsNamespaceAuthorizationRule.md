---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002976"
---
# <span data-ttu-id="943af-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="943af-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="943af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="943af-102">SYNOPSIS</span></span>
<span data-ttu-id="943af-103">Entfernt eine Autorisierungsregel aus einem Notification Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="943af-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="943af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="943af-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="943af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="943af-105">DESCRIPTION</span></span>
<span data-ttu-id="943af-106">Das Cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** entfernt eine Autorisierungsregel für eine freigegebene zugriffssignatur (SAS) aus einem Notification Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="943af-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="943af-107">Autorisierungsregeln verwalten den Zugriff auf einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="943af-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="943af-108">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="943af-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="943af-109">Berechtigungsstufen können wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="943af-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="943af-110">Hören</span><span class="sxs-lookup"><span data-stu-id="943af-110">Listen</span></span>
- <span data-ttu-id="943af-111">Senden</span><span class="sxs-lookup"><span data-stu-id="943af-111">Send</span></span>
- <span data-ttu-id="943af-112">Clients verwalten werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="943af-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="943af-113">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="943af-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="943af-114">Wenn Sie eine Autorisierungsregel entfernen, wird auch die entsprechende Benutzerberechtigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="943af-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="943af-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="943af-115">EXAMPLES</span></span>

### <span data-ttu-id="943af-116">Beispiel 1: Entfernen einer Autorisierungsregel aus einem Namespace</span><span class="sxs-lookup"><span data-stu-id="943af-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="943af-117">Dieser Befehl entfernt die Autorisierungsregel mit dem Namen ListenRule aus dem Namespace mit dem Namen ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="943af-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="943af-118">Wenn Sie diesen Befehl ausführen, müssen Sie die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="943af-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="943af-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="943af-119">PARAMETERS</span></span>

### <span data-ttu-id="943af-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="943af-120">-AuthorizationRule</span></span>
<span data-ttu-id="943af-121">Gibt den Namen der zu entfernenden SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="943af-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="943af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943af-122">-DefaultProfile</span></span>
<span data-ttu-id="943af-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="943af-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="943af-124">-Force</span><span class="sxs-lookup"><span data-stu-id="943af-124">-Force</span></span>
<span data-ttu-id="943af-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="943af-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="943af-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="943af-126">-Namespace</span></span>
<span data-ttu-id="943af-127">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="943af-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="943af-128">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="943af-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="943af-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="943af-129">-ResourceGroup</span></span>
<span data-ttu-id="943af-130">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="943af-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="943af-131">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="943af-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="943af-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="943af-132">-Confirm</span></span>
<span data-ttu-id="943af-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="943af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943af-134">-WhatIf</span></span>
<span data-ttu-id="943af-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="943af-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="943af-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="943af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943af-137">CommonParameters</span></span>
<span data-ttu-id="943af-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="943af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943af-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="943af-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943af-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="943af-140">INPUTS</span></span>

### <span data-ttu-id="943af-141">System. String</span><span class="sxs-lookup"><span data-stu-id="943af-141">System.String</span></span>

## <span data-ttu-id="943af-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="943af-142">OUTPUTS</span></span>

### <span data-ttu-id="943af-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="943af-143">System.Boolean</span></span>

## <span data-ttu-id="943af-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="943af-144">NOTES</span></span>

## <span data-ttu-id="943af-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="943af-145">RELATED LINKS</span></span>

[<span data-ttu-id="943af-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="943af-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="943af-147">Neu – AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="943af-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="943af-148">Satz-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="943af-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


