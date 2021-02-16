---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173332"
---
# <span data-ttu-id="e598b-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="e598b-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="e598b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e598b-102">SYNOPSIS</span></span>
<span data-ttu-id="e598b-103">Löschen Sie einen Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="e598b-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="e598b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e598b-104">SYNTAX</span></span>

### <span data-ttu-id="e598b-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e598b-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e598b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e598b-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e598b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e598b-107">DESCRIPTION</span></span>
<span data-ttu-id="e598b-108">Löschen Sie einen Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="e598b-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="e598b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e598b-109">EXAMPLES</span></span>

### <span data-ttu-id="e598b-110">Beispiel 1: Entfernen eines Windows -IoT-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="e598b-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="e598b-111">Mit diesem Befehl werden Windows -IoT-Dienste nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="e598b-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="e598b-112">Beispiel 2: Entfernen eines Windows -IoT-Diensts per Pipeline</span><span class="sxs-lookup"><span data-stu-id="e598b-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="e598b-113">Mit diesem Befehl wird ein Windows -IoT-Dienst per Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="e598b-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="e598b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e598b-114">PARAMETERS</span></span>

### <span data-ttu-id="e598b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e598b-115">-DefaultProfile</span></span>
<span data-ttu-id="e598b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e598b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e598b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e598b-117">-InputObject</span></span>
<span data-ttu-id="e598b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e598b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e598b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e598b-119">-Name</span></span>
<span data-ttu-id="e598b-120">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="e598b-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e598b-121">-ResourceGroupName</span></span>
<span data-ttu-id="e598b-122">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="e598b-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e598b-123">-SubscriptionId</span></span>
<span data-ttu-id="e598b-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e598b-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e598b-125">-Confirm</span></span>
<span data-ttu-id="e598b-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e598b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e598b-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e598b-127">-WhatIf</span></span>
<span data-ttu-id="e598b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e598b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e598b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e598b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e598b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e598b-130">CommonParameters</span></span>
<span data-ttu-id="e598b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e598b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e598b-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e598b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e598b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e598b-133">INPUTS</span></span>

### <span data-ttu-id="e598b-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="e598b-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="e598b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e598b-135">OUTPUTS</span></span>

### <span data-ttu-id="e598b-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="e598b-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="e598b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e598b-137">NOTES</span></span>

<span data-ttu-id="e598b-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e598b-138">ALIASES</span></span>

<span data-ttu-id="e598b-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e598b-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e598b-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e598b-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e598b-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e598b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e598b-142">INPUTOBJECT <IWindowsIotServicesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e598b-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e598b-143">`[DeviceName <String>]`: Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="e598b-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="e598b-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e598b-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e598b-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="e598b-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="e598b-146">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e598b-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e598b-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e598b-147">RELATED LINKS</span></span>

