---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918259"
---
# <span data-ttu-id="c6273-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c6273-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="c6273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6273-102">SYNOPSIS</span></span>
<span data-ttu-id="c6273-103">Erstellt einen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="c6273-103">Creates a notification hub.</span></span>

## <span data-ttu-id="c6273-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6273-104">SYNTAX</span></span>

### <span data-ttu-id="c6273-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6273-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6273-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6273-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6273-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6273-107">DESCRIPTION</span></span>
<span data-ttu-id="c6273-108">Das **Cmdlet New-AzNotificationHub** erstellt einen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="c6273-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="c6273-109">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6273-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="c6273-110">Benachrichtigungshubs entsprechen in etwa einzelnen Apps: Jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="c6273-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="c6273-111">Das **Cmdlet New-AzNotificationHub** bietet zwei Möglichkeiten zum Erstellen eines neuen Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="c6273-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="c6273-112">Sie können eine Instanz des **NotificationHubAttributes-Objekts** erstellen und dann dieses Objekt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c6273-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="c6273-113">Sie können diese Eigenschaftswerte dann über den Parameter *NotificationHubObj* in Ihren neuen Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="c6273-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="c6273-114">Alternativ können Sie eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des Parameters *InputFile* anwenden.</span><span class="sxs-lookup"><span data-stu-id="c6273-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="c6273-115">In Verbindung mit dem **New-AzNotificationHub-Cmdlet** wird im vorherigen JSON-Beispiel ein Benachrichtigungshub namens ContosoNotificationHub erstellt, der sich im West US-Rechenzentrum befindet.</span><span class="sxs-lookup"><span data-stu-id="c6273-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="c6273-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6273-116">EXAMPLES</span></span>

### <span data-ttu-id="c6273-117">Beispiel 1: Erstellen eines Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="c6273-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="c6273-118">Mit diesem Befehl wird ein Benachrichtigungshub im Namespace ContosoNamespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6273-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="c6273-119">Der neue Hub wird der ContosoNotificationsGroup zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6273-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="c6273-120">Sie müssen keinen Namen oder andere Konfigurationsinformationen für den Hub angeben. diese Informationen werden aus der Eingabedatei C:\Configurations\InternalHub.jsübernommen.</span><span class="sxs-lookup"><span data-stu-id="c6273-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="c6273-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6273-121">PARAMETERS</span></span>

### <span data-ttu-id="c6273-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6273-122">-DefaultProfile</span></span>
<span data-ttu-id="c6273-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c6273-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6273-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c6273-124">-InputFile</span></span>
<span data-ttu-id="c6273-125">Gibt den Pfad zu einer JSON-Datei mit Konfigurationswerten für den neuen Benachrichtigungshub an.</span><span class="sxs-lookup"><span data-stu-id="c6273-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="c6273-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6273-126">-Namespace</span></span>
<span data-ttu-id="c6273-127">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c6273-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="c6273-128">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="c6273-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="c6273-129">Einem vorhandenen Namespace müssen Benachrichtigungshubs zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c6273-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="c6273-130">Das **Cmdlet New-AzNotificationHub** kann keinen neuen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6273-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="c6273-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="c6273-131">-NotificationHubObj</span></span>
<span data-ttu-id="c6273-132">Gibt das **NotificationHubAttributes-Objekt** an, das Konfigurationsinformationen für den neuen Hub enthält.</span><span class="sxs-lookup"><span data-stu-id="c6273-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="c6273-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6273-133">-ResourceGroup</span></span>
<span data-ttu-id="c6273-134">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c6273-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="c6273-135">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6273-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="c6273-136">Sie müssen eine vorhandene Ressourcengruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6273-136">You must use an existing resource group.</span></span>
<span data-ttu-id="c6273-137">Das **Cmdlet New-AzNotificationHub** kann keine neue Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6273-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="c6273-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6273-138">-Confirm</span></span>
<span data-ttu-id="c6273-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6273-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6273-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6273-140">-WhatIf</span></span>
<span data-ttu-id="c6273-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6273-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6273-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6273-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6273-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6273-143">CommonParameters</span></span>
<span data-ttu-id="c6273-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6273-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6273-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6273-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6273-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6273-146">INPUTS</span></span>

### <span data-ttu-id="c6273-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c6273-147">System.String</span></span>

## <span data-ttu-id="c6273-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6273-148">OUTPUTS</span></span>

### <span data-ttu-id="c6273-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c6273-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="c6273-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6273-150">NOTES</span></span>

## <span data-ttu-id="c6273-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6273-151">RELATED LINKS</span></span>

[<span data-ttu-id="c6273-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c6273-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="c6273-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c6273-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="c6273-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c6273-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


