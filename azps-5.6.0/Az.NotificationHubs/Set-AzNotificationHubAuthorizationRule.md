---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 30c6a16d7b9cfb94f1fb2032940aa4587d27e550
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918168"
---
# <span data-ttu-id="7507d-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7507d-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="7507d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7507d-102">SYNOPSIS</span></span>
<span data-ttu-id="7507d-103">Legt Autorisierungsregeln für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="7507d-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="7507d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7507d-104">SYNTAX</span></span>

### <span data-ttu-id="7507d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7507d-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7507d-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7507d-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7507d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7507d-107">DESCRIPTION</span></span>
<span data-ttu-id="7507d-108">Das **Cmdlet Set-AzNotificationHubAuthorizationRule** ändert eine Sas-Autorisierungsregel (Shared Access Signature), die einem Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7507d-109">Autorisierungsregeln verwalten den Zugriff auf Ihre Benachrichtigungshubs durch erstellen von Links als URIs, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="7507d-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7507d-110">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="7507d-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="7507d-111">Anhören</span><span class="sxs-lookup"><span data-stu-id="7507d-111">Listen</span></span>
- <span data-ttu-id="7507d-112">Senden</span><span class="sxs-lookup"><span data-stu-id="7507d-112">Send</span></span>
- <span data-ttu-id="7507d-113">Manage Clients werden basierend auf der entsprechenden Berechtigungsstufe an eine dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="7507d-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7507d-114">Beispielsweise wird ein Client mit der Berechtigung "Listen" für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="7507d-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="7507d-115">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Autorisierungsregel, die einem Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7507d-116">Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="7507d-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="7507d-117">Sie können das Objekt über die -.NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7507d-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="7507d-118">Anschließend können Sie diese Eigenschaftswerte mithilfe des *SASRule-Parameters* in Ihre Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="7507d-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="7507d-119">Alternativ können Sie eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Parameter InputFile* anwenden.</span><span class="sxs-lookup"><span data-stu-id="7507d-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="7507d-120">Eine #A0 ist eine Textdatei, die eine ähnliche Syntax verwendet: { "Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="7507d-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="7507d-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="7507d-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="7507d-122">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="7507d-122">"Rights": \[</span></span>  
        <span data-ttu-id="7507d-123">"Hören",</span><span class="sxs-lookup"><span data-stu-id="7507d-123">"Listen",</span></span>  
        <span data-ttu-id="7507d-124">"Senden"</span><span class="sxs-lookup"><span data-stu-id="7507d-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="7507d-125">} Bei Verwendung in Verbindung mit dem New-AzNotificationHubAuthorizationRule-Cmdlet ändert das vorangehende JSON-Beispiel eine Autorisierungsregel namens ContosoAuthorizationRule, um Benutzern Die Rechte zum Anhören und Senden an den Hub zu geben.</span><span class="sxs-lookup"><span data-stu-id="7507d-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="7507d-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7507d-126">EXAMPLES</span></span>

### <span data-ttu-id="7507d-127">Beispiel 1: Ändern einer Autorisierungsregel, die einem Benachrichtigungshub zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="7507d-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="7507d-128">Mit diesem Befehl wird eine Autorisierungsregel geändert, die dem Benachrichtigungshub "ContosoExternalHub" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="7507d-129">Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="7507d-130">Informationen zu der geänderten Regel sind im Befehl selbst nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="7507d-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="7507d-131">Stattdessen finden Sie diese Informationen in der Eingabedatei, C:\Configuration\AuthorizationRules.jsein.</span><span class="sxs-lookup"><span data-stu-id="7507d-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="7507d-132">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7507d-132">PARAMETERS</span></span>

### <span data-ttu-id="7507d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7507d-133">-DefaultProfile</span></span>
<span data-ttu-id="7507d-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7507d-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7507d-135">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7507d-135">-Force</span></span>
<span data-ttu-id="7507d-136">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="7507d-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7507d-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7507d-137">-InputFile</span></span>
<span data-ttu-id="7507d-138">Gibt den Pfad zu einer JSON-Datei an, der Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="7507d-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="7507d-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7507d-139">-Namespace</span></span>
<span data-ttu-id="7507d-140">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7507d-141">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="7507d-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7507d-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7507d-142">-NotificationHub</span></span>
<span data-ttu-id="7507d-143">Gibt den Benachrichtigungshub an, dem dieses Cmdlet Autorisierungsregeln zugibt.</span><span class="sxs-lookup"><span data-stu-id="7507d-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="7507d-144">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von dem, der von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7507d-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="7507d-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7507d-145">-ResourceGroup</span></span>
<span data-ttu-id="7507d-146">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7507d-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="7507d-147">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7507d-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7507d-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7507d-148">-SASRule</span></span>
<span data-ttu-id="7507d-149">Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die geänderten Autorisierungsregeln enthält.</span><span class="sxs-lookup"><span data-stu-id="7507d-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="7507d-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7507d-150">-Confirm</span></span>
<span data-ttu-id="7507d-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7507d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7507d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7507d-152">-WhatIf</span></span>
<span data-ttu-id="7507d-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7507d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7507d-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7507d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7507d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7507d-155">CommonParameters</span></span>
<span data-ttu-id="7507d-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7507d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7507d-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7507d-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7507d-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7507d-158">INPUTS</span></span>

### <span data-ttu-id="7507d-159">System.String</span><span class="sxs-lookup"><span data-stu-id="7507d-159">System.String</span></span>

## <span data-ttu-id="7507d-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7507d-160">OUTPUTS</span></span>

### <span data-ttu-id="7507d-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7507d-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7507d-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7507d-162">NOTES</span></span>

## <span data-ttu-id="7507d-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7507d-163">RELATED LINKS</span></span>

[<span data-ttu-id="7507d-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7507d-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7507d-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7507d-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7507d-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7507d-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


