---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505430"
---
# <span data-ttu-id="37c10-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="37c10-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="37c10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37c10-102">SYNOPSIS</span></span>
<span data-ttu-id="37c10-103">Legt Eigenschaftswerte für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="37c10-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37c10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37c10-104">SYNTAX</span></span>

### <span data-ttu-id="37c10-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="37c10-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37c10-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="37c10-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c10-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37c10-107">DESCRIPTION</span></span>
<span data-ttu-id="37c10-108">Mit dem Cmdlet " **festlegen-AzureRmNotificationHub** " werden die Eigenschaftenwerte eines benachrichtigungshubs geändert.</span><span class="sxs-lookup"><span data-stu-id="37c10-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="37c10-109">Sie können einen Benachrichtigungs-Hub-Eigenschaftswert auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="37c10-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="37c10-110">Zum einen können Sie eine Instanz des **NotificationHubAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die der neue Hub besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="37c10-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="37c10-111">Dies kann über das .NET Framework erfolgen.</span><span class="sxs-lookup"><span data-stu-id="37c10-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="37c10-112">Sie können diese Eigenschaftswerte dann mithilfe des *NotificationHubObj* -Parameters in ihren Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="37c10-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="37c10-113">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.</span><span class="sxs-lookup"><span data-stu-id="37c10-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="37c10-114">Eine JSON-Datei ist eine Textdatei, die Syntax ähnlich der folgenden verwendet:</span><span class="sxs-lookup"><span data-stu-id="37c10-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="37c10-115">{</span><span class="sxs-lookup"><span data-stu-id="37c10-115">{</span></span>  
    <span data-ttu-id="37c10-116">"Name": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="37c10-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="37c10-117">"Standort": "West US",</span><span class="sxs-lookup"><span data-stu-id="37c10-117">"Location": "West US",</span></span>  
<span data-ttu-id="37c10-118">}</span><span class="sxs-lookup"><span data-stu-id="37c10-118">}</span></span>

<span data-ttu-id="37c10-119">Bei Verwendung in Verbindung mit dem Cmdlet **Set-AzureRmNotificationHub** legt das obige JSON-Beispiel den Positionswert eines benachrichtigungshubs mit dem Namen ContosoNotificationHub auf West US fest.</span><span class="sxs-lookup"><span data-stu-id="37c10-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="37c10-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37c10-120">EXAMPLES</span></span>

### <span data-ttu-id="37c10-121">Beispiel 1: Ändern der Eigenschaftswerte für einen Benachrichtigungs-Hub</span><span class="sxs-lookup"><span data-stu-id="37c10-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="37c10-122">Mit diesem Befehl werden die Eigenschaftenwerte für einen Benachrichtigungs-Hub geändert, der im ContosoNamespace-Namespace gefunden und der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="37c10-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="37c10-123">Die Eigenschaftenwerte sowie der Name des zu ändernden Hubs werden nicht im Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="37c10-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="37c10-124">Stattdessen sind diese Informationen in der Eingabedatei C:\Configuration\Hubs.json enthalten.</span><span class="sxs-lookup"><span data-stu-id="37c10-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="37c10-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="37c10-125">PARAMETERS</span></span>

### <span data-ttu-id="37c10-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c10-126">-DefaultProfile</span></span>
<span data-ttu-id="37c10-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="37c10-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37c10-128">-Force</span><span class="sxs-lookup"><span data-stu-id="37c10-128">-Force</span></span>
<span data-ttu-id="37c10-129">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="37c10-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="37c10-130">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="37c10-130">-InputFile</span></span>
<span data-ttu-id="37c10-131">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für den Benachrichtigungs-Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="37c10-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="37c10-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="37c10-132">-Namespace</span></span>
<span data-ttu-id="37c10-133">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="37c10-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="37c10-134">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="37c10-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="37c10-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="37c10-135">-NotificationHubObj</span></span>
<span data-ttu-id="37c10-136">Gibt das **NotificationHubAttributes** -Objekt an, das Konfigurationsinformationen für den Hub enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37c10-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c10-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37c10-137">-ResourceGroup</span></span>
<span data-ttu-id="37c10-138">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="37c10-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="37c10-139">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37c10-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="37c10-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37c10-140">-Confirm</span></span>
<span data-ttu-id="37c10-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37c10-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c10-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c10-142">-WhatIf</span></span>
<span data-ttu-id="37c10-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37c10-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37c10-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37c10-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c10-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c10-145">CommonParameters</span></span>
<span data-ttu-id="37c10-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c10-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c10-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c10-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c10-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37c10-148">INPUTS</span></span>

### <span data-ttu-id="37c10-149">Keine</span><span class="sxs-lookup"><span data-stu-id="37c10-149">None</span></span>
<span data-ttu-id="37c10-150">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="37c10-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37c10-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37c10-151">OUTPUTS</span></span>

### <span data-ttu-id="37c10-152">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="37c10-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="37c10-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="37c10-153">NOTES</span></span>

## <span data-ttu-id="37c10-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37c10-154">RELATED LINKS</span></span>

[<span data-ttu-id="37c10-155">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="37c10-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="37c10-156">Neu – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="37c10-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="37c10-157">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="37c10-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)


