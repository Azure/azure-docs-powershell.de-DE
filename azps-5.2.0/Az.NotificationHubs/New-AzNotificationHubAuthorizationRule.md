---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295858"
---
# <span data-ttu-id="85136-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85136-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="85136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85136-102">SYNOPSIS</span></span>
<span data-ttu-id="85136-103">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungshub zu.</span><span class="sxs-lookup"><span data-stu-id="85136-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="85136-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85136-104">SYNTAX</span></span>

### <span data-ttu-id="85136-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="85136-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85136-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="85136-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85136-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85136-107">DESCRIPTION</span></span>
<span data-ttu-id="85136-108">Das **Cmdlet "New-AzNotificationHubAuthorizationRule"** erstellt eine SAS (Notification Hub Shared Access Signature)-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="85136-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="85136-109">Autorisierungsregeln werden verwendet, um den Zugriff auf Ihre Benachrichtigungshubs zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="85136-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="85136-110">Dies erfolgt durch die Erstellung von Links als URIs, die auf unterschiedlichen Berechtigungsstufen basieren.</span><span class="sxs-lookup"><span data-stu-id="85136-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="85136-111">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="85136-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="85136-112">Beispielsweise wird ein Client, dem die Berechtigung "Listen" erteilt wurde, für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="85136-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="85136-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85136-113">EXAMPLES</span></span>

### <span data-ttu-id="85136-114">Beispiel 1: Erstellen einer Benachrichtigungshubautorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="85136-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="85136-115">Mit diesem Befehl wird eine neue Autorisierungsregel erstellt und dem Benachrichtigungshub "ContosoInternalHub" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="85136-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="85136-116">Dieser Hub befindet sich im Namespace "ContosoNamespace" und wird der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="85136-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="85136-117">Beachten Sie, dass alle Konfigurationsinformationen für die Regel, einschließlich des Regelnamens, aus der Eingabedatei C:\Configuration\ExternalAccessRule.jswerden.</span><span class="sxs-lookup"><span data-stu-id="85136-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="85136-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85136-118">PARAMETERS</span></span>

### <span data-ttu-id="85136-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85136-119">-DefaultProfile</span></span>
<span data-ttu-id="85136-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="85136-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85136-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="85136-121">-InputFile</span></span>
<span data-ttu-id="85136-122">Gibt die Eingabedatei für die Autorisierungsregel an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="85136-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85136-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="85136-123">-Namespace</span></span>
<span data-ttu-id="85136-124">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="85136-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="85136-125">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="85136-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="85136-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="85136-126">-NotificationHub</span></span>
<span data-ttu-id="85136-127">Gibt den Benachrichtigungshub an, dem die Autorisierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="85136-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="85136-128">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="85136-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="85136-129">Beachten Sie, dass Sie den Namen eines vorhandenen Benachrichtigungshubs angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="85136-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="85136-130">Das **Cmdlet "New-AzNotificationHubAuthorizationRule"** kann keine neuen Benachrichtigungshubs erstellen.</span><span class="sxs-lookup"><span data-stu-id="85136-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="85136-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85136-131">-ResourceGroup</span></span>
<span data-ttu-id="85136-132">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="85136-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="85136-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="85136-133">-SASRule</span></span>
<span data-ttu-id="85136-134">Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die neuen Regeln enthält.</span><span class="sxs-lookup"><span data-stu-id="85136-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85136-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85136-135">-Confirm</span></span>
<span data-ttu-id="85136-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85136-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85136-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85136-137">-WhatIf</span></span>
<span data-ttu-id="85136-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85136-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85136-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85136-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85136-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85136-140">CommonParameters</span></span>
<span data-ttu-id="85136-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85136-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85136-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85136-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85136-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85136-143">INPUTS</span></span>

### <span data-ttu-id="85136-144">System.String</span><span class="sxs-lookup"><span data-stu-id="85136-144">System.String</span></span>

## <span data-ttu-id="85136-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85136-145">OUTPUTS</span></span>

### <span data-ttu-id="85136-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="85136-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="85136-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85136-147">NOTES</span></span>

## <span data-ttu-id="85136-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85136-148">RELATED LINKS</span></span>

[<span data-ttu-id="85136-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85136-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="85136-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85136-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="85136-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85136-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


