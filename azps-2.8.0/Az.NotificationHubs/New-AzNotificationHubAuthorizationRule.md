---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 436ed6aaa720074be2014d9c736ab0636a09869f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823652"
---
# <span data-ttu-id="98323-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="98323-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="98323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98323-102">SYNOPSIS</span></span>
<span data-ttu-id="98323-103">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungs-Hub zu.</span><span class="sxs-lookup"><span data-stu-id="98323-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="98323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98323-104">SYNTAX</span></span>

### <span data-ttu-id="98323-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="98323-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98323-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="98323-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98323-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98323-107">DESCRIPTION</span></span>
<span data-ttu-id="98323-108">Mit dem Cmdlet " **New-AzNotificationHubAuthorizationRule** " wird eine Benachrichtigungs-Hub-Autorisierungsregel (Shared Access Signature, SAS) erstellt.</span><span class="sxs-lookup"><span data-stu-id="98323-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="98323-109">Autorisierungsregeln werden verwendet, um den Zugriff auf Ihre benachrichtigungshubs zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="98323-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="98323-110">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="98323-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="98323-111">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="98323-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="98323-112">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="98323-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="98323-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98323-113">EXAMPLES</span></span>

### <span data-ttu-id="98323-114">Beispiel 1: Erstellen einer Benachrichtigungs-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="98323-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="98323-115">Mit diesem Befehl wird eine neue Autorisierungsregel erstellt und dem Benachrichtigungs-Hub mit dem Namen "ContosoInternalHub" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="98323-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="98323-116">Dieser Hub befindet sich im ContosoNamespace-Namespace und wird der ContosoNotificationsGroup-Ressourcengruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="98323-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="98323-117">Beachten Sie, dass alle Konfigurationsinformationen für die Regel, einschließlich des Regel namens, aus der Eingabedatei C:\Configuration\ExternalAccessRule.jsauf übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="98323-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="98323-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="98323-118">PARAMETERS</span></span>

### <span data-ttu-id="98323-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98323-119">-DefaultProfile</span></span>
<span data-ttu-id="98323-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="98323-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98323-121">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="98323-121">-InputFile</span></span>
<span data-ttu-id="98323-122">Gibt die Eingabedatei für die Autorisierungsregel an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="98323-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="98323-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98323-123">-Namespace</span></span>
<span data-ttu-id="98323-124">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="98323-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="98323-125">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="98323-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="98323-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="98323-126">-NotificationHub</span></span>
<span data-ttu-id="98323-127">Gibt den Benachrichtigungs-Hub an, dem die Autorisierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="98323-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="98323-128">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98323-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="98323-129">Beachten Sie, dass Sie den Namen eines vorhandenen benachrichtigungshubs angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="98323-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="98323-130">Mit dem Cmdlet **New-AzNotificationHubAuthorizationRule** können keine neuen benachrichtigungshubs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="98323-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="98323-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="98323-131">-ResourceGroup</span></span>
<span data-ttu-id="98323-132">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="98323-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="98323-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="98323-133">-SASRule</span></span>
<span data-ttu-id="98323-134">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die neuen Regeln enthält.</span><span class="sxs-lookup"><span data-stu-id="98323-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="98323-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98323-135">-Confirm</span></span>
<span data-ttu-id="98323-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98323-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98323-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98323-137">-WhatIf</span></span>
<span data-ttu-id="98323-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98323-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98323-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98323-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98323-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98323-140">CommonParameters</span></span>
<span data-ttu-id="98323-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98323-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98323-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98323-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98323-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98323-143">INPUTS</span></span>

### <span data-ttu-id="98323-144">System. String</span><span class="sxs-lookup"><span data-stu-id="98323-144">System.String</span></span>

## <span data-ttu-id="98323-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98323-145">OUTPUTS</span></span>

### <span data-ttu-id="98323-146">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="98323-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="98323-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="98323-147">NOTES</span></span>

## <span data-ttu-id="98323-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98323-148">RELATED LINKS</span></span>

[<span data-ttu-id="98323-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="98323-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="98323-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="98323-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="98323-151">Satz-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="98323-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


