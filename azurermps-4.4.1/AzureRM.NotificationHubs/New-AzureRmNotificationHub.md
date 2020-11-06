---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479018"
---
# <span data-ttu-id="1a5de-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1a5de-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="1a5de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a5de-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5de-103">Erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="1a5de-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a5de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a5de-104">SYNTAX</span></span>

### <span data-ttu-id="1a5de-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a5de-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a5de-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a5de-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a5de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a5de-107">DESCRIPTION</span></span>
<span data-ttu-id="1a5de-108">Das Cmdlet **New-AzureRmNotificationHub** erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="1a5de-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="1a5de-109">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a5de-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="1a5de-110">Benachrichtigungshubs entsprechen in etwa den einzelnen apps: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="1a5de-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="1a5de-111">Das Cmdlet **New-AzureRmNotificationHub** bietet zwei Möglichkeiten zum Erstellen eines neuen benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="1a5de-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="1a5de-112">Sie können eine Instanz des **NotificationHubAttributes** -Objekts erstellen und dieses Objekt dann konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1a5de-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="1a5de-113">Sie können diese Eigenschaftswerte dann mithilfe des *NotificationHubObj* -Parameters in ihren neuen Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="1a5de-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="1a5de-114">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des *Input* File-Parameters anwenden.</span><span class="sxs-lookup"><span data-stu-id="1a5de-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="1a5de-115">Bei Verwendung in Verbindung mit dem Cmdlet **New-AzureRmNotificationHub** wird im vorherigen JSON-Beispiel ein Benachrichtigungs-Hub mit dem Namen ContosoNotificationHub erstellt, der sich im West US-Rechenzentrum befindet.</span><span class="sxs-lookup"><span data-stu-id="1a5de-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="1a5de-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a5de-116">EXAMPLES</span></span>

### <span data-ttu-id="1a5de-117">Beispiel 1: Erstellen eines benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="1a5de-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="1a5de-118">Dieser Befehl erstellt einen Benachrichtigungs-Hub im Namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="1a5de-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="1a5de-119">Der neue Hub wird dem ContosoNotificationsGroup zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1a5de-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="1a5de-120">Sie müssen keinen Namen oder andere Konfigurationsinformationen für den Hub angeben. Diese Informationen werden aus der Eingabedatei C:\Configurations\InternalHub.json übernommen.</span><span class="sxs-lookup"><span data-stu-id="1a5de-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="1a5de-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a5de-121">PARAMETERS</span></span>

### <span data-ttu-id="1a5de-122">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="1a5de-122">-InputFile</span></span>
<span data-ttu-id="1a5de-123">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationswerte für den neuen Benachrichtigungs-Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="1a5de-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="1a5de-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1a5de-124">-Namespace</span></span>
<span data-ttu-id="1a5de-125">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1a5de-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="1a5de-126">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="1a5de-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="1a5de-127">Benachrichtigungshubs müssen einem vorhandenen Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a5de-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="1a5de-128">Das Cmdlet **New-AzureRmNotificationHub** kann keinen neuen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a5de-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="1a5de-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="1a5de-129">-NotificationHubObj</span></span>
<span data-ttu-id="1a5de-130">Gibt das **NotificationHubAttributes** -Objekt an, das Konfigurationsinformationen für den neuen Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="1a5de-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="1a5de-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a5de-131">-ResourceGroup</span></span>
<span data-ttu-id="1a5de-132">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1a5de-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="1a5de-133">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a5de-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="1a5de-134">Sie müssen eine vorhandene Ressourcengruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a5de-134">You must use an existing resource group.</span></span>
<span data-ttu-id="1a5de-135">Das Cmdlet **New-AzureRmNotificationHub** kann keine neue Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a5de-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="1a5de-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a5de-136">-Confirm</span></span>
<span data-ttu-id="1a5de-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a5de-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a5de-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a5de-138">-WhatIf</span></span>
<span data-ttu-id="1a5de-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a5de-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a5de-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a5de-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a5de-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5de-141">-DefaultProfile</span></span>
<span data-ttu-id="1a5de-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a5de-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a5de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5de-143">CommonParameters</span></span>
<span data-ttu-id="1a5de-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5de-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5de-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5de-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a5de-146">INPUTS</span></span>

## <span data-ttu-id="1a5de-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a5de-147">OUTPUTS</span></span>

### <span data-ttu-id="1a5de-148">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1a5de-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="1a5de-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a5de-149">NOTES</span></span>

## <span data-ttu-id="1a5de-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a5de-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a5de-151">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1a5de-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="1a5de-152">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1a5de-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="1a5de-153">Satz-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1a5de-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


