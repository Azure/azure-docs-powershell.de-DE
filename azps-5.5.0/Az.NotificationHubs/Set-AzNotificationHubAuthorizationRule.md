---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172379"
---
# <span data-ttu-id="9944b-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9944b-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="9944b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9944b-102">SYNOPSIS</span></span>
<span data-ttu-id="9944b-103">Legt Autorisierungsregeln für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="9944b-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="9944b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9944b-104">SYNTAX</span></span>

### <span data-ttu-id="9944b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9944b-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9944b-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9944b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9944b-107">DESCRIPTION</span></span>
<span data-ttu-id="9944b-108">Das **Cmdlet Set-AzNotificationHubAuthorizationRule** ändert eine SAS (Shared Access Signature)-Autorisierungsregel, die einem Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9944b-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="9944b-109">Autorisierungsregeln verwalten den Zugriff auf Ihre Benachrichtigungshubs durch erstellen von Links als URIs, basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="9944b-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="9944b-110">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="9944b-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="9944b-111">Zuhören</span><span class="sxs-lookup"><span data-stu-id="9944b-111">Listen</span></span>
- <span data-ttu-id="9944b-112">Senden</span><span class="sxs-lookup"><span data-stu-id="9944b-112">Send</span></span>
- <span data-ttu-id="9944b-113">"Clients verwalten" wird basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs geleitet.</span><span class="sxs-lookup"><span data-stu-id="9944b-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9944b-114">Beispielsweise wird ein Client, dem die Berechtigung "Listen" erteilt wurde, für diese Berechtigung an den URI geleitet.</span><span class="sxs-lookup"><span data-stu-id="9944b-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="9944b-115">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Einem Benachrichtigungshub zugewiesenen Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="9944b-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="9944b-116">Sie können beispielsweise eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="9944b-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="9944b-117">Sie können das Objekt über .NET Framework konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9944b-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="9944b-118">Anschließend können Sie diese Eigenschaftswerte mithilfe des Parameters *SASRule* in Ihre Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="9944b-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="9944b-119">Alternativ können Sie eine JSON(JavaScript Object Notation)-Datei erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Parameter "InputFile"* anwenden.</span><span class="sxs-lookup"><span data-stu-id="9944b-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="9944b-120">Eine #A0 ist eine Textdatei, in der die folgende Syntax verwendet wird: { "Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="9944b-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="9944b-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="9944b-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="9944b-122">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="9944b-122">"Rights": \[</span></span>  
        <span data-ttu-id="9944b-123">"Zuhören",</span><span class="sxs-lookup"><span data-stu-id="9944b-123">"Listen",</span></span>  
        <span data-ttu-id="9944b-124">"Senden"</span><span class="sxs-lookup"><span data-stu-id="9944b-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="9944b-125">} Bei Verwendung in Verbindung mit dem Cmdlet New-AzNotificationHubAuthorizationRule ändert das vorangehende Beispiel für JSON eine Autorisierungsregel namens "ContosoAuthorizationRule", um Benutzern Listen- und Sendeberechtigungen für den Hub zu geben.</span><span class="sxs-lookup"><span data-stu-id="9944b-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="9944b-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9944b-126">EXAMPLES</span></span>

### <span data-ttu-id="9944b-127">Beispiel 1: Ändern einer einem Benachrichtigungshub zugewiesenen Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="9944b-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="9944b-128">Mit diesem Befehl wird eine dem Benachrichtigungshub zugewiesene Autorisierungsregel namens "ContosoExternalHub" geändert.</span><span class="sxs-lookup"><span data-stu-id="9944b-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="9944b-129">Sie müssen den Namespace, in dem sich der Hub befindet, sowie die Ressourcengruppe angeben, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9944b-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="9944b-130">Informationen zu der regel, die geändert wird, werden nicht in den Befehl selbst eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9944b-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="9944b-131">Stattdessen finden Sie diese Informationen in der Eingabedatei, C:\Configuration\AuthorizationRules.jssind.</span><span class="sxs-lookup"><span data-stu-id="9944b-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="9944b-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9944b-132">PARAMETERS</span></span>

### <span data-ttu-id="9944b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9944b-133">-DefaultProfile</span></span>
<span data-ttu-id="9944b-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9944b-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9944b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="9944b-135">-Force</span></span>
<span data-ttu-id="9944b-136">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="9944b-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9944b-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9944b-137">-InputFile</span></span>
<span data-ttu-id="9944b-138">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="9944b-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="9944b-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9944b-139">-Namespace</span></span>
<span data-ttu-id="9944b-140">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9944b-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9944b-141">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="9944b-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9944b-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9944b-142">-NotificationHub</span></span>
<span data-ttu-id="9944b-143">Gibt den Benachrichtigungshub an, dem dieses Cmdlet Autorisierungsregeln zugibt.</span><span class="sxs-lookup"><span data-stu-id="9944b-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="9944b-144">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von den von diesen Clients verwendeten Clients an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="9944b-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="9944b-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9944b-145">-ResourceGroup</span></span>
<span data-ttu-id="9944b-146">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9944b-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="9944b-147">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9944b-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9944b-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="9944b-148">-SASRule</span></span>
<span data-ttu-id="9944b-149">Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die geänderten Autorisierungsregeln enthält.</span><span class="sxs-lookup"><span data-stu-id="9944b-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="9944b-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9944b-150">-Confirm</span></span>
<span data-ttu-id="9944b-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9944b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9944b-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9944b-152">-WhatIf</span></span>
<span data-ttu-id="9944b-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9944b-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9944b-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9944b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9944b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9944b-155">CommonParameters</span></span>
<span data-ttu-id="9944b-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9944b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9944b-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9944b-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9944b-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9944b-158">INPUTS</span></span>

### <span data-ttu-id="9944b-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9944b-159">System.String</span></span>

## <span data-ttu-id="9944b-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9944b-160">OUTPUTS</span></span>

### <span data-ttu-id="9944b-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9944b-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9944b-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9944b-162">NOTES</span></span>

## <span data-ttu-id="9944b-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9944b-163">RELATED LINKS</span></span>

[<span data-ttu-id="9944b-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9944b-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9944b-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9944b-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9944b-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9944b-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


