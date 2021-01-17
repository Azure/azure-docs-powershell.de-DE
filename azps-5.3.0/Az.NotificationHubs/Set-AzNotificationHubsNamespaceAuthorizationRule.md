---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385005"
---
# <span data-ttu-id="56cd8-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="56cd8-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="56cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="56cd8-103">Legt Autorisierungsregeln für einen Benachrichtigungshub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="56cd8-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="56cd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56cd8-104">SYNTAX</span></span>

### <span data-ttu-id="56cd8-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="56cd8-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56cd8-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="56cd8-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56cd8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56cd8-107">DESCRIPTION</span></span>
<span data-ttu-id="56cd8-108">Das **Cmdlet Set-AzNotificationHubsNamespaceAuthorizationRule** ändert eine SAS (Shared Access Signature)-Autorisierungsregel, die einem Benachrichtigungshub-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="56cd8-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="56cd8-109">Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die in diesem Namespace enthaltenen Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="56cd8-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="56cd8-110">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer einem Namespace zugewiesenen Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="56cd8-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="56cd8-111">Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="56cd8-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="56cd8-112">Zu diesem Zweck können Sie .NET Framework verwenden.</span><span class="sxs-lookup"><span data-stu-id="56cd8-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="56cd8-113">Anschließend können Sie diese Eigenschaftswerte über den Parameter *SASRule* in die Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="56cd8-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="56cd8-114">Alternativ können Sie eine JSON(JavaScript Object Notation)-Datei erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Parameter "InputFile"* anwenden.</span><span class="sxs-lookup"><span data-stu-id="56cd8-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="56cd8-115">Eine #A0 ist eine Textdatei, in der die folgende Syntax verwendet wird: {</span><span class="sxs-lookup"><span data-stu-id="56cd8-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="56cd8-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="56cd8-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="56cd8-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="56cd8-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="56cd8-118">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="56cd8-118">"Rights": \[</span></span>  
        <span data-ttu-id="56cd8-119">"Zuhören",</span><span class="sxs-lookup"><span data-stu-id="56cd8-119">"Listen",</span></span>  
        <span data-ttu-id="56cd8-120">"Senden"</span><span class="sxs-lookup"><span data-stu-id="56cd8-120">"Send"</span></span>  
    \]  
<span data-ttu-id="56cd8-121">} Bei Verwendung in Verbindung mit dem **Cmdlet "Set-AzNotificationHubsNamespaceAuthorizationRule"** ändert das vorangehende Beispiel eine Autorisierungsregel namens "ContosoAuthorizationRule", um Benutzern Listen- und Sendeberechtigungen für den Namespace zu geben.</span><span class="sxs-lookup"><span data-stu-id="56cd8-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="56cd8-122">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56cd8-122">EXAMPLES</span></span>

### <span data-ttu-id="56cd8-123">Beispiel 1: Ändern einer einem Namespace zugewiesenen Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="56cd8-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="56cd8-124">Mit diesem Befehl wird eine dem Namespace "ContosoNamespace" zugewiesene Autorisierungsregel geändert.</span><span class="sxs-lookup"><span data-stu-id="56cd8-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="56cd8-125">Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="56cd8-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="56cd8-126">Informationen zur Autorisierungsregel sind in dem Befehl selbst nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="56cd8-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="56cd8-127">Stattdessen werden diese Informationen aus der Eingabedatei C:\Configuration\AuthorizationRules.jswerden.</span><span class="sxs-lookup"><span data-stu-id="56cd8-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="56cd8-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56cd8-128">PARAMETERS</span></span>

### <span data-ttu-id="56cd8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cd8-129">-DefaultProfile</span></span>
<span data-ttu-id="56cd8-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="56cd8-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56cd8-131">-Force</span><span class="sxs-lookup"><span data-stu-id="56cd8-131">-Force</span></span>
<span data-ttu-id="56cd8-132">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="56cd8-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="56cd8-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="56cd8-133">-InputFile</span></span>
<span data-ttu-id="56cd8-134">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="56cd8-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="56cd8-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="56cd8-135">-Namespace</span></span>
<span data-ttu-id="56cd8-136">Gibt den Namespace an, der die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="56cd8-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="56cd8-137">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="56cd8-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="56cd8-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56cd8-138">-ResourceGroup</span></span>
<span data-ttu-id="56cd8-139">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="56cd8-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="56cd8-140">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="56cd8-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="56cd8-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="56cd8-141">-SASRule</span></span>
<span data-ttu-id="56cd8-142">Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="56cd8-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="56cd8-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56cd8-143">-Confirm</span></span>
<span data-ttu-id="56cd8-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56cd8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56cd8-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56cd8-145">-WhatIf</span></span>
<span data-ttu-id="56cd8-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56cd8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56cd8-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56cd8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56cd8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cd8-148">CommonParameters</span></span>
<span data-ttu-id="56cd8-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56cd8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cd8-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56cd8-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cd8-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56cd8-151">INPUTS</span></span>

### <span data-ttu-id="56cd8-152">System.String</span><span class="sxs-lookup"><span data-stu-id="56cd8-152">System.String</span></span>

## <span data-ttu-id="56cd8-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56cd8-153">OUTPUTS</span></span>

### <span data-ttu-id="56cd8-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="56cd8-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="56cd8-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56cd8-155">NOTES</span></span>

## <span data-ttu-id="56cd8-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56cd8-156">RELATED LINKS</span></span>

[<span data-ttu-id="56cd8-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="56cd8-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="56cd8-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="56cd8-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="56cd8-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="56cd8-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


