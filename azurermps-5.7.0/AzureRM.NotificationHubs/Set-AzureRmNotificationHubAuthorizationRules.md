---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505426"
---
# <span data-ttu-id="7a5bf-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7a5bf-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="7a5bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5bf-103">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a5bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a5bf-104">SYNTAX</span></span>

### <span data-ttu-id="7a5bf-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a5bf-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a5bf-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a5bf-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a5bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a5bf-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5bf-108">Das Cmdlet " **Satz-AzureRmNotificationHubAuthorizationRules** " ändert eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS), die einem Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="7a5bf-109">Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs durch das Erstellen von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7a5bf-110">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="7a5bf-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="7a5bf-111">Hören</span><span class="sxs-lookup"><span data-stu-id="7a5bf-111">Listen</span></span>
- <span data-ttu-id="7a5bf-112">Senden</span><span class="sxs-lookup"><span data-stu-id="7a5bf-112">Send</span></span>
- <span data-ttu-id="7a5bf-113">Verwalten</span><span class="sxs-lookup"><span data-stu-id="7a5bf-113">Manage</span></span>

<span data-ttu-id="7a5bf-114">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7a5bf-115">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="7a5bf-116">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Autorisierungsregel, die einem Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7a5bf-117">Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="7a5bf-118">Sie können das Objekt über das .NET Framework konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="7a5bf-119">Sie können diese Eigenschaftswerte dann mithilfe des *SASRule* -Parameters in Ihre Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="7a5bf-120">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="7a5bf-121">Eine JSON-Datei ist eine Textdatei, die ähnlich wie diese Syntax verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="7a5bf-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="7a5bf-122">{"Name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="7a5bf-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7a5bf-123">"Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="7a5bf-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7a5bf-124">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="7a5bf-124">"Rights": \[</span></span>  
        <span data-ttu-id="7a5bf-125">"Hören",</span><span class="sxs-lookup"><span data-stu-id="7a5bf-125">"Listen",</span></span>  
        <span data-ttu-id="7a5bf-126">Senden</span><span class="sxs-lookup"><span data-stu-id="7a5bf-126">"Send"</span></span>  
    \]  
<span data-ttu-id="7a5bf-127">}</span><span class="sxs-lookup"><span data-stu-id="7a5bf-127">}</span></span>

<span data-ttu-id="7a5bf-128">Bei Verwendung in Verbindung mit dem New-AzureRmNotificationHubAuthorizationRules-Cmdlet ändert das vorangehende JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule, um Benutzern das Abhören und Senden von Rechten an den Hub zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="7a5bf-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a5bf-129">EXAMPLES</span></span>

### <span data-ttu-id="7a5bf-130">Beispiel 1: Ändern einer Autorisierungsregel, die einem Benachrichtigungs-Hub zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="7a5bf-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="7a5bf-131">Mit diesem Befehl wird eine Autorisierungsregel geändert, die dem Benachrichtigungs-Hub mit dem Namen ContosoExternalHub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="7a5bf-132">Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="7a5bf-133">Informationen zur geänderten Regel sind nicht im Befehl selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="7a5bf-134">Stattdessen finden Sie die Informationen in der Eingabedatei C:\Configuration\AuthorizationRules.jsein.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="7a5bf-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a5bf-135">PARAMETERS</span></span>

### <span data-ttu-id="7a5bf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5bf-136">-DefaultProfile</span></span>
<span data-ttu-id="7a5bf-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7a5bf-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-138">-Force</span><span class="sxs-lookup"><span data-stu-id="7a5bf-138">-Force</span></span>
<span data-ttu-id="7a5bf-139">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-139">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-140">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="7a5bf-140">-InputFile</span></span>
<span data-ttu-id="7a5bf-141">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-141">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-142">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a5bf-142">-Namespace</span></span>
<span data-ttu-id="7a5bf-143">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-143">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7a5bf-144">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-144">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-145">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7a5bf-145">-NotificationHub</span></span>
<span data-ttu-id="7a5bf-146">Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet Autorisierungsregeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-146">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="7a5bf-147">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig davon, welche von diesen Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-147">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-148">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7a5bf-148">-ResourceGroup</span></span>
<span data-ttu-id="7a5bf-149">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-149">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="7a5bf-150">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-150">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-151">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7a5bf-151">-SASRule</span></span>
<span data-ttu-id="7a5bf-152">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die geänderten Autorisierungsregeln enthält.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-152">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a5bf-153">-Confirm</span></span>
<span data-ttu-id="7a5bf-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5bf-155">-WhatIf</span></span>
<span data-ttu-id="7a5bf-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a5bf-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5bf-158">CommonParameters</span></span>
<span data-ttu-id="7a5bf-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5bf-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a5bf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5bf-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a5bf-161">INPUTS</span></span>

### <span data-ttu-id="7a5bf-162">Keine</span><span class="sxs-lookup"><span data-stu-id="7a5bf-162">None</span></span>
<span data-ttu-id="7a5bf-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a5bf-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a5bf-164">OUTPUTS</span></span>

### <span data-ttu-id="7a5bf-165">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7a5bf-165">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7a5bf-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a5bf-166">NOTES</span></span>

## <span data-ttu-id="7a5bf-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a5bf-167">RELATED LINKS</span></span>

[<span data-ttu-id="7a5bf-168">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7a5bf-168">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7a5bf-169">Neu – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7a5bf-169">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7a5bf-170">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7a5bf-170">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


