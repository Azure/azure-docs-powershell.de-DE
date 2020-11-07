---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 9c65ec6f4cf1a8b9c6a8e85b196d4b61b62df09a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823655"
---
# <span data-ttu-id="a9f1a-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9f1a-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="a9f1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f1a-103">Erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-103">Creates a notification hub.</span></span>

## <span data-ttu-id="a9f1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9f1a-104">SYNTAX</span></span>

### <span data-ttu-id="a9f1a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9f1a-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f1a-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9f1a-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9f1a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9f1a-107">DESCRIPTION</span></span>
<span data-ttu-id="a9f1a-108">Das Cmdlet **New-AzNotificationHub** erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="a9f1a-109">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="a9f1a-110">Benachrichtigungshubs entsprechen in etwa den einzelnen apps: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="a9f1a-111">Das Cmdlet **New-AzNotificationHub** bietet zwei Möglichkeiten zum Erstellen eines neuen benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="a9f1a-112">Sie können eine Instanz des **NotificationHubAttributes** -Objekts erstellen und dieses Objekt dann konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="a9f1a-113">Sie können diese Eigenschaftswerte dann mithilfe des *NotificationHubObj* -Parameters in ihren neuen Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="a9f1a-114">Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des *Input* File-Parameters anwenden.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="a9f1a-115">Bei Verwendung in Verbindung mit dem Cmdlet **New-AzNotificationHub** wird im vorherigen JSON-Beispiel ein Benachrichtigungs-Hub mit dem Namen ContosoNotificationHub erstellt, der sich im West US-Rechenzentrum befindet.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="a9f1a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9f1a-116">EXAMPLES</span></span>

### <span data-ttu-id="a9f1a-117">Beispiel 1: Erstellen eines benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="a9f1a-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="a9f1a-118">Dieser Befehl erstellt einen Benachrichtigungs-Hub im Namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="a9f1a-119">Der neue Hub wird dem ContosoNotificationsGroup zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="a9f1a-120">Sie müssen keinen Namen oder andere Konfigurationsinformationen für den Hub angeben. Diese Informationen werden aus der Eingabedatei C:\Configurations\InternalHub.json übernommen.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="a9f1a-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9f1a-121">PARAMETERS</span></span>

### <span data-ttu-id="a9f1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f1a-122">-DefaultProfile</span></span>
<span data-ttu-id="a9f1a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9f1a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9f1a-124">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="a9f1a-124">-InputFile</span></span>
<span data-ttu-id="a9f1a-125">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationswerte für den neuen Benachrichtigungs-Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="a9f1a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9f1a-126">-Namespace</span></span>
<span data-ttu-id="a9f1a-127">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="a9f1a-128">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="a9f1a-129">Benachrichtigungshubs müssen einem vorhandenen Namespace zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="a9f1a-130">Das Cmdlet **New-AzNotificationHub** kann keinen neuen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="a9f1a-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="a9f1a-131">-NotificationHubObj</span></span>
<span data-ttu-id="a9f1a-132">Gibt das **NotificationHubAttributes** -Objekt an, das Konfigurationsinformationen für den neuen Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="a9f1a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9f1a-133">-ResourceGroup</span></span>
<span data-ttu-id="a9f1a-134">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="a9f1a-135">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="a9f1a-136">Sie müssen eine vorhandene Ressourcengruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-136">You must use an existing resource group.</span></span>
<span data-ttu-id="a9f1a-137">Das Cmdlet **New-AzNotificationHub** kann keine neue Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="a9f1a-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9f1a-138">-Confirm</span></span>
<span data-ttu-id="a9f1a-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9f1a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9f1a-140">-WhatIf</span></span>
<span data-ttu-id="a9f1a-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9f1a-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9f1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f1a-143">CommonParameters</span></span>
<span data-ttu-id="a9f1a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f1a-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f1a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f1a-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9f1a-146">INPUTS</span></span>

### <span data-ttu-id="a9f1a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f1a-147">System.String</span></span>

## <span data-ttu-id="a9f1a-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9f1a-148">OUTPUTS</span></span>

### <span data-ttu-id="a9f1a-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a9f1a-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="a9f1a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9f1a-150">NOTES</span></span>

## <span data-ttu-id="a9f1a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9f1a-151">RELATED LINKS</span></span>

[<span data-ttu-id="a9f1a-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9f1a-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="a9f1a-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9f1a-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="a9f1a-154">Satz-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9f1a-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


