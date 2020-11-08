---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176247"
---
# <span data-ttu-id="9399d-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9399d-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="9399d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9399d-102">SYNOPSIS</span></span>
<span data-ttu-id="9399d-103">Entfernt eine Autorisierungsregel aus einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="9399d-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="9399d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9399d-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9399d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9399d-105">DESCRIPTION</span></span>
<span data-ttu-id="9399d-106">Das Cmdlet " **Remove-AzNotificationHubAuthorizationRule** " entfernt eine Autorisierungsregel für eine freigegebene zugriffssignatur (SAS) von einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="9399d-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="9399d-107">Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs durch das Erstellen von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="9399d-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="9399d-108">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="9399d-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="9399d-109">Hören</span><span class="sxs-lookup"><span data-stu-id="9399d-109">Listen</span></span>
- <span data-ttu-id="9399d-110">Senden</span><span class="sxs-lookup"><span data-stu-id="9399d-110">Send</span></span>
- <span data-ttu-id="9399d-111">Clients verwalten werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="9399d-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9399d-112">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="9399d-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="9399d-113">Wenn Sie eine Autorisierungsregel entfernen, wird auch die entsprechende Benutzerberechtigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9399d-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="9399d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9399d-114">EXAMPLES</span></span>

### <span data-ttu-id="9399d-115">Beispiel 1: Entfernen einer Autorisierungsregel von einem Benachrichtigungs-Hub</span><span class="sxs-lookup"><span data-stu-id="9399d-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9399d-116">Dieser Befehl entfernt die Autorisierungsregel namens ListenRule aus dem Benachrichtigungs-Hub mit dem Namen ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="9399d-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="9399d-117">Wenn Sie diesen Befehl ausführen, müssen Sie sowohl den Namespace als auch die Ressourcengruppe angeben, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9399d-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="9399d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9399d-118">PARAMETERS</span></span>

### <span data-ttu-id="9399d-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9399d-119">-AuthorizationRule</span></span>
<span data-ttu-id="9399d-120">Gibt den Namen der SAS-Authentifizierungsregel an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9399d-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9399d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9399d-121">-DefaultProfile</span></span>
<span data-ttu-id="9399d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9399d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9399d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9399d-123">-Force</span></span>
<span data-ttu-id="9399d-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9399d-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9399d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9399d-125">-Namespace</span></span>
<span data-ttu-id="9399d-126">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9399d-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9399d-127">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="9399d-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9399d-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9399d-128">-NotificationHub</span></span>
<span data-ttu-id="9399d-129">Gibt den Benachrichtigungs-Hub an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9399d-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="9399d-130">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden.</span><span class="sxs-lookup"><span data-stu-id="9399d-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="9399d-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9399d-131">-ResourceGroup</span></span>
<span data-ttu-id="9399d-132">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9399d-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9399d-133">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9399d-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9399d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9399d-134">-Confirm</span></span>
<span data-ttu-id="9399d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9399d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9399d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9399d-136">-WhatIf</span></span>
<span data-ttu-id="9399d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9399d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9399d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9399d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9399d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9399d-139">CommonParameters</span></span>
<span data-ttu-id="9399d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9399d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9399d-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9399d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9399d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9399d-142">INPUTS</span></span>

### <span data-ttu-id="9399d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9399d-143">System.String</span></span>

## <span data-ttu-id="9399d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9399d-144">OUTPUTS</span></span>

### <span data-ttu-id="9399d-145">System. void</span><span class="sxs-lookup"><span data-stu-id="9399d-145">System.Void</span></span>

## <span data-ttu-id="9399d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="9399d-146">NOTES</span></span>

## <span data-ttu-id="9399d-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9399d-147">RELATED LINKS</span></span>

[<span data-ttu-id="9399d-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9399d-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9399d-149">Neu – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9399d-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9399d-150">Satz-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9399d-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


