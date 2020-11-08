---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174955"
---
# <span data-ttu-id="3183e-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3183e-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="3183e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3183e-102">SYNOPSIS</span></span>
<span data-ttu-id="3183e-103">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungs-Hub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="3183e-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="3183e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3183e-104">SYNTAX</span></span>

### <span data-ttu-id="3183e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3183e-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3183e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3183e-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3183e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3183e-107">DESCRIPTION</span></span>
<span data-ttu-id="3183e-108">Das Cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** erstellt eine Autorisierungsregel für die Shared Access-Signatur (SAS) und weist Sie einem Notification Hub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="3183e-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="3183e-109">Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die benachrichtigungshubs, die in diesem Namespace enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3183e-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="3183e-110">Dieses Cmdlet bietet zwei Möglichkeiten, um eine neue Autorisierungsregel zu erstellen und Sie einem Namespace zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3183e-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="3183e-111">Sie können eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die neue Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="3183e-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="3183e-112">Dies kann mit .NET Framework erfolgen.</span><span class="sxs-lookup"><span data-stu-id="3183e-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="3183e-113">Sie können diese Eigenschaftswerte dann mithilfe des *SASRule* -Parameters in Ihre neue Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="3183e-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="3183e-114">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des *Input* File-Parameters anwenden.</span><span class="sxs-lookup"><span data-stu-id="3183e-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="3183e-115">Eine JSON-Datei ist eine Textdatei, die Syntax ähnlich der folgenden verwendet: {</span><span class="sxs-lookup"><span data-stu-id="3183e-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="3183e-116">"Name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="3183e-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="3183e-117">"Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="3183e-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="3183e-118">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="3183e-118">"Rights": \[</span></span>  
        <span data-ttu-id="3183e-119">"Hören",</span><span class="sxs-lookup"><span data-stu-id="3183e-119">"Listen",</span></span>  
        <span data-ttu-id="3183e-120">Senden</span><span class="sxs-lookup"><span data-stu-id="3183e-120">"Send"</span></span>  
    \]  
<span data-ttu-id="3183e-121">} Bei Verwendung in Verbindung mit dem Cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** wird im vorherigen JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule erstellt, die Benutzern das Abhören und Senden von Rechten an den Namespace ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3183e-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="3183e-122">Der für die Authentifizierung verwendete *primär* Wert kann mithilfe des folgenden Windows PowerShell-Befehls nach dem Zufallsprinzip generiert werden: \[ Convert \] :: Base64-Wert ((1.. 32 |% { \[ Byte/] (Get-Random-mindestens 0-Maximum 255))))</span><span class="sxs-lookup"><span data-stu-id="3183e-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="3183e-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3183e-123">EXAMPLES</span></span>

### <span data-ttu-id="3183e-124">Beispiel 1: Erstellen einer Autorisierungsregel und Zuweisen der Autorisierung zu einem Namespace</span><span class="sxs-lookup"><span data-stu-id="3183e-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="3183e-125">Dieser Befehl erstellt eine Autorisierungsregel und weist diese Regel dem Namespace ContosoNamespace zu.</span><span class="sxs-lookup"><span data-stu-id="3183e-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="3183e-126">Beim Erstellen dieser Regel müssen Sie den entsprechenden Namespace und die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3183e-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="3183e-127">Sie müssen jedoch keine Informationen über die Regel selbst angeben: Regel Informationen werden aus der Eingabedatei C:\Configuration\NamespaceAuthorizationRules.json übernommen.</span><span class="sxs-lookup"><span data-stu-id="3183e-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="3183e-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="3183e-128">PARAMETERS</span></span>

### <span data-ttu-id="3183e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3183e-129">-DefaultProfile</span></span>
<span data-ttu-id="3183e-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3183e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3183e-131">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="3183e-131">-InputFile</span></span>
<span data-ttu-id="3183e-132">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Autorisierungsregel enthält.</span><span class="sxs-lookup"><span data-stu-id="3183e-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3183e-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3183e-133">-Namespace</span></span>
<span data-ttu-id="3183e-134">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3183e-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="3183e-135">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="3183e-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="3183e-136">Die neuen Regeln müssen einem vorhandenen Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3183e-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="3183e-137">Das Cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** kann keinen neuen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="3183e-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="3183e-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3183e-138">-ResourceGroup</span></span>
<span data-ttu-id="3183e-139">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3183e-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="3183e-140">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3183e-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="3183e-141">Sie müssen eine vorhandene Ressourcengruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3183e-141">You must use an existing resource group.</span></span>
<span data-ttu-id="3183e-142">Dieses Cmdlet kann keine neue Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="3183e-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="3183e-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3183e-143">-SASRule</span></span>
<span data-ttu-id="3183e-144">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die neuen Regeln enthält.</span><span class="sxs-lookup"><span data-stu-id="3183e-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3183e-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3183e-145">-Confirm</span></span>
<span data-ttu-id="3183e-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3183e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3183e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3183e-147">-WhatIf</span></span>
<span data-ttu-id="3183e-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3183e-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3183e-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3183e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3183e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3183e-150">CommonParameters</span></span>
<span data-ttu-id="3183e-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3183e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3183e-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3183e-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3183e-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3183e-153">INPUTS</span></span>

### <span data-ttu-id="3183e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3183e-154">System.String</span></span>

## <span data-ttu-id="3183e-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3183e-155">OUTPUTS</span></span>

### <span data-ttu-id="3183e-156">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3183e-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3183e-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="3183e-157">NOTES</span></span>

## <span data-ttu-id="3183e-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3183e-158">RELATED LINKS</span></span>

[<span data-ttu-id="3183e-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3183e-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3183e-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3183e-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3183e-161">Satz-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3183e-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


