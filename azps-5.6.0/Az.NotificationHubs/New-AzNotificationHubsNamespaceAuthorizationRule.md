---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918240"
---
# <span data-ttu-id="bd037-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd037-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="bd037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd037-102">SYNOPSIS</span></span>
<span data-ttu-id="bd037-103">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungshubnamespace zu.</span><span class="sxs-lookup"><span data-stu-id="bd037-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="bd037-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd037-104">SYNTAX</span></span>

### <span data-ttu-id="bd037-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd037-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd037-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd037-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd037-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd037-107">DESCRIPTION</span></span>
<span data-ttu-id="bd037-108">Das **Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** erstellt eine Sas-Autorisierungsregel (Shared Access Signature) und weist sie einem Benachrichtigungshub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="bd037-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="bd037-109">Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die Benachrichtigungshubs, die in diesem Namespace enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bd037-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="bd037-110">Dieses Cmdlet bietet zwei Möglichkeiten zum Erstellen einer neuen Autorisierungsregel und zum Zuweisen zu einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="bd037-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="bd037-111">Sie können eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die neue Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="bd037-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="bd037-112">Dies kann mithilfe von .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bd037-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="bd037-113">Anschließend können Sie diese Eigenschaftswerte mithilfe des *SASRule-Parameters* in ihre neue Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="bd037-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="bd037-114">Alternativ können Sie eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des Parameters *InputFile* anwenden.</span><span class="sxs-lookup"><span data-stu-id="bd037-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="bd037-115">Eine #A0 ist eine Textdatei, die eine syntax ähnliche Syntax wie die folgende verwendet: {</span><span class="sxs-lookup"><span data-stu-id="bd037-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="bd037-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="bd037-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="bd037-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="bd037-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="bd037-118">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="bd037-118">"Rights": \[</span></span>  
        <span data-ttu-id="bd037-119">"Hören",</span><span class="sxs-lookup"><span data-stu-id="bd037-119">"Listen",</span></span>  
        <span data-ttu-id="bd037-120">"Senden"</span><span class="sxs-lookup"><span data-stu-id="bd037-120">"Send"</span></span>  
    \]  
<span data-ttu-id="bd037-121">} Bei Verwendung in Verbindung mit **dem Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** wird im vorherigen JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule erstellt, die Benutzern Listen- und Sendeberechtigungen für den Namespace gewährt.</span><span class="sxs-lookup"><span data-stu-id="bd037-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="bd037-122">Der *für* die Authentifizierung verwendete Primärschlüssel kann mithilfe des folgenden Windows PowerShell-Befehls zufällig generiert werden: \[ Konvertieren \] ::ToBase64String(((1,32 |% { \[ Byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="bd037-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="bd037-123">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd037-123">EXAMPLES</span></span>

### <span data-ttu-id="bd037-124">Beispiel 1: Erstellen einer Autorisierungsregel und Zuweisen zu einem Namespace</span><span class="sxs-lookup"><span data-stu-id="bd037-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="bd037-125">Dieser Befehl erstellt eine Autorisierungsregel und weist diese Regel dem Namespace ContosoNamespace zu.</span><span class="sxs-lookup"><span data-stu-id="bd037-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="bd037-126">Beim Erstellen dieser Regel müssen Sie den entsprechenden Namespace und die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bd037-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="bd037-127">Sie müssen jedoch keine Informationen zur Regel selbst angeben: Regelinformationen werden aus der Eingabedatei C:\Configuration\NamespaceAuthorizationRules.jsübernommen.</span><span class="sxs-lookup"><span data-stu-id="bd037-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="bd037-128">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd037-128">PARAMETERS</span></span>

### <span data-ttu-id="bd037-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd037-129">-DefaultProfile</span></span>
<span data-ttu-id="bd037-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bd037-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd037-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bd037-131">-InputFile</span></span>
<span data-ttu-id="bd037-132">Gibt den Pfad zu einer JSON-Datei an, der Konfigurationsinformationen für die neue Autorisierungsregel enthält.</span><span class="sxs-lookup"><span data-stu-id="bd037-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="bd037-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd037-133">-Namespace</span></span>
<span data-ttu-id="bd037-134">Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bd037-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="bd037-135">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="bd037-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="bd037-136">Die neuen Regeln müssen einem vorhandenen Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bd037-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="bd037-137">Das **Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** kann keinen neuen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd037-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="bd037-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd037-138">-ResourceGroup</span></span>
<span data-ttu-id="bd037-139">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bd037-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="bd037-140">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd037-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="bd037-141">Sie müssen eine vorhandene Ressourcengruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd037-141">You must use an existing resource group.</span></span>
<span data-ttu-id="bd037-142">Dieses Cmdlet kann keine neue Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd037-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="bd037-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="bd037-143">-SASRule</span></span>
<span data-ttu-id="bd037-144">Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die neuen Regeln enthält.</span><span class="sxs-lookup"><span data-stu-id="bd037-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="bd037-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd037-145">-Confirm</span></span>
<span data-ttu-id="bd037-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd037-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd037-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd037-147">-WhatIf</span></span>
<span data-ttu-id="bd037-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd037-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd037-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd037-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd037-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd037-150">CommonParameters</span></span>
<span data-ttu-id="bd037-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd037-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd037-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd037-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd037-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd037-153">INPUTS</span></span>

### <span data-ttu-id="bd037-154">System.String</span><span class="sxs-lookup"><span data-stu-id="bd037-154">System.String</span></span>

## <span data-ttu-id="bd037-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd037-155">OUTPUTS</span></span>

### <span data-ttu-id="bd037-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bd037-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bd037-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd037-157">NOTES</span></span>

## <span data-ttu-id="bd037-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd037-158">RELATED LINKS</span></span>

[<span data-ttu-id="bd037-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd037-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bd037-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd037-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bd037-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd037-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


