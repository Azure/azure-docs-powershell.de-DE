---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497029"
---
# <span data-ttu-id="e4817-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e4817-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="e4817-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4817-102">SYNOPSIS</span></span>
<span data-ttu-id="e4817-103">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungs-Hub zu.</span><span class="sxs-lookup"><span data-stu-id="e4817-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4817-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4817-104">SYNTAX</span></span>

### <span data-ttu-id="e4817-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4817-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4817-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4817-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4817-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4817-107">DESCRIPTION</span></span>
<span data-ttu-id="e4817-108">Mit dem Cmdlet " **New-AzureRmNotificationHubAuthorizationRules** " wird eine Benachrichtigungs-Hub-Autorisierungsregel (Shared Access Signature, SAS) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4817-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="e4817-109">Autorisierungsregeln werden verwendet, um den Zugriff auf Ihre benachrichtigungshubs zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e4817-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="e4817-110">Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="e4817-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="e4817-111">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4817-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e4817-112">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4817-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="e4817-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4817-113">EXAMPLES</span></span>

### <span data-ttu-id="e4817-114">Beispiel 1: Erstellen einer Benachrichtigungs-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="e4817-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="e4817-115">Mit diesem Befehl wird eine neue Autorisierungsregel erstellt und dem Benachrichtigungs-Hub mit dem Namen "ContosoInternalHub" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e4817-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="e4817-116">Dieser Hub befindet sich im ContosoNamespace-Namespace und wird der ContosoNotificationsGroup-Ressourcengruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e4817-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="e4817-117">Beachten Sie, dass alle Konfigurationsinformationen für die Regel, einschließlich des Regel namens, aus der Eingabedatei C:\Configuration\ExternalAccessRule.jsauf übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="e4817-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="e4817-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4817-118">PARAMETERS</span></span>

### <span data-ttu-id="e4817-119">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="e4817-119">-InputFile</span></span>
<span data-ttu-id="e4817-120">Gibt die Eingabedatei für die Autorisierungsregel an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4817-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e4817-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4817-121">-Namespace</span></span>
<span data-ttu-id="e4817-122">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="e4817-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="e4817-123">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="e4817-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e4817-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e4817-124">-NotificationHub</span></span>
<span data-ttu-id="e4817-125">Gibt den Benachrichtigungs-Hub an, dem die Autorisierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="e4817-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="e4817-126">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4817-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="e4817-127">Beachten Sie, dass Sie den Namen eines vorhandenen benachrichtigungshubs angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="e4817-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="e4817-128">Mit dem Cmdlet **New-AzureRmNotificationHubAuthorizationRules** können keine neuen benachrichtigungshubs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e4817-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="e4817-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4817-129">-ResourceGroup</span></span>
<span data-ttu-id="e4817-130">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e4817-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="e4817-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="e4817-131">-SASRule</span></span>
<span data-ttu-id="e4817-132">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die neuen Regeln enthält.</span><span class="sxs-lookup"><span data-stu-id="e4817-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="e4817-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4817-133">-Confirm</span></span>
<span data-ttu-id="e4817-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4817-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4817-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4817-135">-WhatIf</span></span>
<span data-ttu-id="e4817-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4817-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4817-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4817-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4817-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4817-138">-DefaultProfile</span></span>
<span data-ttu-id="e4817-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4817-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4817-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4817-140">CommonParameters</span></span>
<span data-ttu-id="e4817-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4817-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4817-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4817-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4817-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4817-143">INPUTS</span></span>

## <span data-ttu-id="e4817-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4817-144">OUTPUTS</span></span>

### <span data-ttu-id="e4817-145">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e4817-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e4817-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4817-146">NOTES</span></span>

## <span data-ttu-id="e4817-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4817-147">RELATED LINKS</span></span>

[<span data-ttu-id="e4817-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e4817-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="e4817-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e4817-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="e4817-150">Satz-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e4817-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


