---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505422"
---
# <span data-ttu-id="d2aa0-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2aa0-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="d2aa0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2aa0-103">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2aa0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2aa0-104">SYNTAX</span></span>

### <span data-ttu-id="d2aa0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2aa0-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2aa0-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2aa0-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2aa0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2aa0-107">DESCRIPTION</span></span>
<span data-ttu-id="d2aa0-108">Das Cmdlet " **Satz-AzureRmNotificationHubsNamespaceAuthorizationRules** " ändert eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS), die einem Benachrichtigungs-Hub-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="d2aa0-109">Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die benachrichtigungshubs, die in diesem Namespace enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="d2aa0-110">Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Autorisierungsregel, die einem Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="d2aa0-111">Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="d2aa0-112">Sie können das .NET Framework verwenden, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="d2aa0-113">Sie können diese Eigenschaftswerte dann über den *SASRule* -Parameter in die Regel kopieren.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="d2aa0-114">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="d2aa0-115">Eine JSON-Datei ist eine Textdatei, die ähnlich wie diese Syntax verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="d2aa0-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="d2aa0-116">{</span><span class="sxs-lookup"><span data-stu-id="d2aa0-116">{</span></span>  
    <span data-ttu-id="d2aa0-117">"Name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="d2aa0-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="d2aa0-118">"Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="d2aa0-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="d2aa0-119">"Rechte": \[</span><span class="sxs-lookup"><span data-stu-id="d2aa0-119">"Rights": \[</span></span>  
        <span data-ttu-id="d2aa0-120">"Hören",</span><span class="sxs-lookup"><span data-stu-id="d2aa0-120">"Listen",</span></span>  
        <span data-ttu-id="d2aa0-121">Senden</span><span class="sxs-lookup"><span data-stu-id="d2aa0-121">"Send"</span></span>  
    \]  
<span data-ttu-id="d2aa0-122">}</span><span class="sxs-lookup"><span data-stu-id="d2aa0-122">}</span></span>

<span data-ttu-id="d2aa0-123">Bei Verwendung in Verbindung mit dem Cmdlet " **setAzureRmNotificationHubsNamespaceAuthorizationRules** " ändert das vorangehende JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule, um Benutzern das Abhören und Senden von Rechten an den Namespace zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="d2aa0-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2aa0-124">EXAMPLES</span></span>

### <span data-ttu-id="d2aa0-125">Beispiel 1: Ändern einer Autorisierungsregel, die einem Namespace zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="d2aa0-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="d2aa0-126">Mit diesem Befehl wird eine Autorisierungsregel geändert, die dem Namespace mit dem Namen ContosoNamespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="d2aa0-127">Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="d2aa0-128">Informationen zur Autorisierungsregel sind nicht im Befehl selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="d2aa0-129">Stattdessen werden die Informationen aus der Eingabedatei C:\Configuration\AuthorizationRules.jsauf abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="d2aa0-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2aa0-130">PARAMETERS</span></span>

### <span data-ttu-id="d2aa0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2aa0-131">-DefaultProfile</span></span>
<span data-ttu-id="d2aa0-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d2aa0-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2aa0-133">-Force</span><span class="sxs-lookup"><span data-stu-id="d2aa0-133">-Force</span></span>
<span data-ttu-id="d2aa0-134">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-134">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d2aa0-135">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="d2aa0-135">-InputFile</span></span>
<span data-ttu-id="d2aa0-136">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2aa0-137">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d2aa0-137">-Namespace</span></span>
<span data-ttu-id="d2aa0-138">Gibt den Namespace an, der die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="d2aa0-139">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d2aa0-140">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d2aa0-140">-ResourceGroup</span></span>
<span data-ttu-id="d2aa0-141">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="d2aa0-142">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d2aa0-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="d2aa0-143">-SASRule</span></span>
<span data-ttu-id="d2aa0-144">Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2aa0-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2aa0-145">-Confirm</span></span>
<span data-ttu-id="d2aa0-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2aa0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2aa0-147">-WhatIf</span></span>
<span data-ttu-id="d2aa0-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2aa0-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2aa0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2aa0-150">CommonParameters</span></span>
<span data-ttu-id="d2aa0-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2aa0-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2aa0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2aa0-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2aa0-153">INPUTS</span></span>

### <span data-ttu-id="d2aa0-154">Keine</span><span class="sxs-lookup"><span data-stu-id="d2aa0-154">None</span></span>
<span data-ttu-id="d2aa0-155">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d2aa0-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2aa0-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2aa0-156">OUTPUTS</span></span>

### <span data-ttu-id="d2aa0-157">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d2aa0-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d2aa0-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2aa0-158">NOTES</span></span>

## <span data-ttu-id="d2aa0-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2aa0-159">RELATED LINKS</span></span>

[<span data-ttu-id="d2aa0-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2aa0-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="d2aa0-161">Neu – AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2aa0-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="d2aa0-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2aa0-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


