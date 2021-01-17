---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470957"
---
# <span data-ttu-id="50ebd-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50ebd-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="50ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="50ebd-103">Verknüpft einen Azure-Benachrichtigungshub mit diesem Kommunikationsdienst.</span><span class="sxs-lookup"><span data-stu-id="50ebd-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="50ebd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50ebd-104">SYNTAX</span></span>

### <span data-ttu-id="50ebd-105">LinkExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="50ebd-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50ebd-106">Link</span><span class="sxs-lookup"><span data-stu-id="50ebd-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50ebd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="50ebd-108">Verknüpft einen Azure-Benachrichtigungshub mit diesem Kommunikationsdienst.</span><span class="sxs-lookup"><span data-stu-id="50ebd-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="50ebd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50ebd-109">EXAMPLES</span></span>

### <span data-ttu-id="50ebd-110">Beispiel 1: Interaktives Bereitstellen von Details des Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="50ebd-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="50ebd-111">Ein verknüpfter Benachrichtigungshub ermöglicht einer ACS-Ressource das Senden von Benachrichtigungen für bestimmte Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="50ebd-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="50ebd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50ebd-112">PARAMETERS</span></span>

### <span data-ttu-id="50ebd-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="50ebd-113">-CommunicationServiceName</span></span>
<span data-ttu-id="50ebd-114">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="50ebd-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="50ebd-115">-ConnectionString</span></span>
<span data-ttu-id="50ebd-116">Verbindungszeichenfolge für den Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="50ebd-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ebd-117">-DefaultProfile</span></span>
<span data-ttu-id="50ebd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50ebd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="50ebd-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="50ebd-120">Beschreibung eines #A0 zur Verknüpfung mit dem Kommunikationsdienst "Zu erstellen" finden Sie im Abschnitt NOTES zu den LINKNOTIFICATIONHUBPARAMETER-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="50ebd-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="50ebd-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="50ebd-122">Die Ressourcen-ID des Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="50ebd-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ebd-123">-ResourceGroupName</span></span>
<span data-ttu-id="50ebd-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="50ebd-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="50ebd-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="50ebd-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50ebd-126">-SubscriptionId</span></span>
<span data-ttu-id="50ebd-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="50ebd-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="50ebd-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="50ebd-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ebd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50ebd-129">-Confirm</span></span>
<span data-ttu-id="50ebd-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50ebd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ebd-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50ebd-131">-WhatIf</span></span>
<span data-ttu-id="50ebd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50ebd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50ebd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50ebd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50ebd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ebd-134">CommonParameters</span></span>
<span data-ttu-id="50ebd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ebd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ebd-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50ebd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ebd-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50ebd-137">INPUTS</span></span>

### <span data-ttu-id="50ebd-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="50ebd-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="50ebd-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50ebd-139">OUTPUTS</span></span>

### <span data-ttu-id="50ebd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="50ebd-140">System.String</span></span>

## <span data-ttu-id="50ebd-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50ebd-141">NOTES</span></span>

<span data-ttu-id="50ebd-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="50ebd-142">ALIASES</span></span>

<span data-ttu-id="50ebd-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="50ebd-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50ebd-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50ebd-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50ebd-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50ebd-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50ebd-146">LINKNOTIFICATIONHUBPARAMETER: <ILinkNotificationHubParameters> Beschreibung eines Azure-Benachrichtigungshubs, der mit dem Kommunikationsdienst verbunden werden soll</span><span class="sxs-lookup"><span data-stu-id="50ebd-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="50ebd-147">`ConnectionString <String>`: Verbindungszeichenfolge für den Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="50ebd-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="50ebd-148">`ResourceId <String>`: Die Ressourcen-ID des Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="50ebd-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="50ebd-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50ebd-149">RELATED LINKS</span></span>

