---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: f59ac6a2e1431c3ba04ff0ac9cf9cafbfdfe367e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824160"
---
# <span data-ttu-id="54b77-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="54b77-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="54b77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54b77-102">SYNOPSIS</span></span>
<span data-ttu-id="54b77-103">Legt Eigenschaftswerte für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="54b77-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="54b77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54b77-104">SYNTAX</span></span>

### <span data-ttu-id="54b77-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b77-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54b77-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b77-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54b77-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54b77-107">DESCRIPTION</span></span>
<span data-ttu-id="54b77-108">Mit dem Cmdlet " **festlegen-AzNotificationHub** " werden die Eigenschaftenwerte eines benachrichtigungshubs geändert.</span><span class="sxs-lookup"><span data-stu-id="54b77-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="54b77-109">Sie können einen Benachrichtigungs-Hub-Eigenschaftswert auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="54b77-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="54b77-110">Zum einen können Sie eine Instanz des **NotificationHubAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die der neue Hub besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="54b77-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="54b77-111">Dies kann über das .NET Framework erfolgen.</span><span class="sxs-lookup"><span data-stu-id="54b77-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="54b77-112">Sie können diese Eigenschaftswerte dann mithilfe des *NotificationHubObj* -Parameters in ihren Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="54b77-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="54b77-113">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.</span><span class="sxs-lookup"><span data-stu-id="54b77-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="54b77-114">Eine JSON-Datei ist eine Textdatei, die Syntax ähnlich der folgenden verwendet: {</span><span class="sxs-lookup"><span data-stu-id="54b77-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="54b77-115">"Name": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="54b77-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="54b77-116">"Standort": "West US",</span><span class="sxs-lookup"><span data-stu-id="54b77-116">"Location": "West US",</span></span>  
<span data-ttu-id="54b77-117">} Bei Verwendung in Verbindung mit dem Cmdlet " **Set-AzNotificationHub** " legt das obige JSON-Beispiel den Positionswert eines benachrichtigungshubs mit dem Namen ContosoNotificationHub auf West US fest.</span><span class="sxs-lookup"><span data-stu-id="54b77-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="54b77-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54b77-118">EXAMPLES</span></span>

### <span data-ttu-id="54b77-119">Beispiel 1: Ändern der Eigenschaftswerte für einen Benachrichtigungs-Hub</span><span class="sxs-lookup"><span data-stu-id="54b77-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="54b77-120">Mit diesem Befehl werden die Eigenschaftenwerte für einen Benachrichtigungs-Hub geändert, der im ContosoNamespace-Namespace gefunden und der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="54b77-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="54b77-121">Die Eigenschaftenwerte sowie der Name des zu ändernden Hubs werden nicht im Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="54b77-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="54b77-122">Stattdessen sind diese Informationen in der Eingabedatei C:\Configuration\Hubs.json enthalten.</span><span class="sxs-lookup"><span data-stu-id="54b77-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="54b77-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="54b77-123">PARAMETERS</span></span>

### <span data-ttu-id="54b77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b77-124">-DefaultProfile</span></span>
<span data-ttu-id="54b77-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="54b77-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b77-126">-Force</span><span class="sxs-lookup"><span data-stu-id="54b77-126">-Force</span></span>
<span data-ttu-id="54b77-127">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="54b77-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="54b77-128">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="54b77-128">-InputFile</span></span>
<span data-ttu-id="54b77-129">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für den Benachrichtigungs-Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="54b77-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="54b77-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="54b77-130">-Namespace</span></span>
<span data-ttu-id="54b77-131">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="54b77-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="54b77-132">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="54b77-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="54b77-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="54b77-133">-NotificationHubObj</span></span>
<span data-ttu-id="54b77-134">Gibt das **NotificationHubAttributes** -Objekt an, das Konfigurationsinformationen für den Hub enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="54b77-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b77-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54b77-135">-ResourceGroup</span></span>
<span data-ttu-id="54b77-136">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="54b77-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="54b77-137">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54b77-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="54b77-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54b77-138">-Confirm</span></span>
<span data-ttu-id="54b77-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54b77-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54b77-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b77-140">-WhatIf</span></span>
<span data-ttu-id="54b77-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54b77-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54b77-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54b77-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54b77-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b77-143">CommonParameters</span></span>
<span data-ttu-id="54b77-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b77-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b77-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b77-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b77-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54b77-146">INPUTS</span></span>

### <span data-ttu-id="54b77-147">System. String</span><span class="sxs-lookup"><span data-stu-id="54b77-147">System.String</span></span>

## <span data-ttu-id="54b77-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54b77-148">OUTPUTS</span></span>

### <span data-ttu-id="54b77-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="54b77-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="54b77-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="54b77-150">NOTES</span></span>

## <span data-ttu-id="54b77-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54b77-151">RELATED LINKS</span></span>

[<span data-ttu-id="54b77-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="54b77-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="54b77-153">Neu – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="54b77-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="54b77-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="54b77-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


