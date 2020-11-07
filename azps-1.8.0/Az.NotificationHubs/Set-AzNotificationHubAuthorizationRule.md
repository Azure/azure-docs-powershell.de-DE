---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74aa4d00d387e832c1abf02a5c65ca5e34e42123
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660087"
---
# <span data-ttu-id="59499-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59499-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="59499-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59499-102">SYNOPSIS</span></span>
<span data-ttu-id="59499-103">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="59499-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="59499-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59499-104">SYNTAX</span></span>

### <span data-ttu-id="59499-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="59499-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59499-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="59499-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59499-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59499-107">DESCRIPTION</span></span>
<span data-ttu-id="59499-108">Das Cmdlet " **Satz-AzNotificationHubAuthorizationRule** " ändert eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS), die einem Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="59499-109">Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs durch das Erstellen von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="59499-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="59499-110">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="59499-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="59499-111">Hören</span><span class="sxs-lookup"><span data-stu-id="59499-111">Listen</span></span>
- <span data-ttu-id="59499-112">Senden</span><span class="sxs-lookup"><span data-stu-id="59499-112">Send</span></span>
- <span data-ttu-id="59499-113">Clients verwalten werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="59499-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="59499-114">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="59499-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="59499-115">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Autorisierungsregel, die einem Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="59499-116">Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="59499-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="59499-117">Sie können das Objekt über das .NET Framework konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="59499-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="59499-118">Sie können diese Eigenschaftswerte dann mithilfe des *SASRule* -Parameters in Ihre Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="59499-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="59499-119">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.</span><span class="sxs-lookup"><span data-stu-id="59499-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="59499-120">Eine JSON-Datei ist eine Textdatei, die ähnlich wie diese Syntax verwendet wird: {"Name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="59499-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="59499-121">"Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="59499-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="59499-122">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="59499-122">"Rights": \[</span></span>  
        <span data-ttu-id="59499-123">"Hören",</span><span class="sxs-lookup"><span data-stu-id="59499-123">"Listen",</span></span>  
        <span data-ttu-id="59499-124">Senden</span><span class="sxs-lookup"><span data-stu-id="59499-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="59499-125">} Wenn in Verbindung mit dem New-AzNotificationHubAuthorizationRule-Cmdlet verwendet wird, ändert das vorangehende JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule, um Benutzern das Abhören und Senden von Rechten an den Hub zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="59499-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="59499-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59499-126">EXAMPLES</span></span>

### <span data-ttu-id="59499-127">Beispiel 1: Ändern einer Autorisierungsregel, die einem Benachrichtigungs-Hub zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="59499-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="59499-128">Mit diesem Befehl wird eine Autorisierungsregel geändert, die dem Benachrichtigungs-Hub mit dem Namen ContosoExternalHub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="59499-129">Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="59499-130">Informationen zur geänderten Regel sind nicht im Befehl selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="59499-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="59499-131">Stattdessen finden Sie die Informationen in der Eingabedatei C:\Configuration\AuthorizationRules.jsein.</span><span class="sxs-lookup"><span data-stu-id="59499-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="59499-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="59499-132">PARAMETERS</span></span>

### <span data-ttu-id="59499-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59499-133">-DefaultProfile</span></span>
<span data-ttu-id="59499-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="59499-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59499-135">-Force</span><span class="sxs-lookup"><span data-stu-id="59499-135">-Force</span></span>
<span data-ttu-id="59499-136">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="59499-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59499-137">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="59499-137">-InputFile</span></span>
<span data-ttu-id="59499-138">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="59499-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="59499-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59499-139">-Namespace</span></span>
<span data-ttu-id="59499-140">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="59499-141">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="59499-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="59499-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="59499-142">-NotificationHub</span></span>
<span data-ttu-id="59499-143">Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet Autorisierungsregeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="59499-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="59499-144">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig davon, welche von diesen Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59499-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="59499-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59499-145">-ResourceGroup</span></span>
<span data-ttu-id="59499-146">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59499-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="59499-147">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59499-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="59499-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="59499-148">-SASRule</span></span>
<span data-ttu-id="59499-149">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die geänderten Autorisierungsregeln enthält.</span><span class="sxs-lookup"><span data-stu-id="59499-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="59499-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59499-150">-Confirm</span></span>
<span data-ttu-id="59499-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59499-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59499-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59499-152">-WhatIf</span></span>
<span data-ttu-id="59499-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59499-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59499-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59499-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59499-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59499-155">CommonParameters</span></span>
<span data-ttu-id="59499-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59499-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59499-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59499-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59499-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59499-158">INPUTS</span></span>

### <span data-ttu-id="59499-159">System. String</span><span class="sxs-lookup"><span data-stu-id="59499-159">System.String</span></span>

## <span data-ttu-id="59499-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59499-160">OUTPUTS</span></span>

### <span data-ttu-id="59499-161">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="59499-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="59499-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="59499-162">NOTES</span></span>

## <span data-ttu-id="59499-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59499-163">RELATED LINKS</span></span>

[<span data-ttu-id="59499-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59499-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="59499-165">Neu – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59499-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="59499-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59499-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


