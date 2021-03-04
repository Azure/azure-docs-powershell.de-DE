---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: e0012bab0679a49e0ad5a117845ca9e0e5d5a6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928411"
---
# <span data-ttu-id="72a7e-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="72a7e-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="72a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="72a7e-103">Löschen Sie einen Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="72a7e-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="72a7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72a7e-104">SYNTAX</span></span>

### <span data-ttu-id="72a7e-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="72a7e-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72a7e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72a7e-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72a7e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72a7e-107">DESCRIPTION</span></span>
<span data-ttu-id="72a7e-108">Löschen Sie einen Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="72a7e-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="72a7e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72a7e-109">EXAMPLES</span></span>

### <span data-ttu-id="72a7e-110">Beispiel 1: Entfernen eines Windows IoT-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="72a7e-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="72a7e-111">Mit diesem Befehl wird ein Windows IoT-Dienst nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="72a7e-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="72a7e-112">Beispiel 2: Entfernen eines Windows IoT-Diensts per Pipeline</span><span class="sxs-lookup"><span data-stu-id="72a7e-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="72a7e-113">Mit diesem Befehl werden Windows IoT-Dienste per Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="72a7e-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="72a7e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72a7e-114">PARAMETERS</span></span>

### <span data-ttu-id="72a7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a7e-115">-DefaultProfile</span></span>
<span data-ttu-id="72a7e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72a7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72a7e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72a7e-117">-InputObject</span></span>
<span data-ttu-id="72a7e-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="72a7e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72a7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="72a7e-119">-Name</span></span>
<span data-ttu-id="72a7e-120">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="72a7e-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="72a7e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a7e-121">-ResourceGroupName</span></span>
<span data-ttu-id="72a7e-122">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="72a7e-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="72a7e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72a7e-123">-SubscriptionId</span></span>
<span data-ttu-id="72a7e-124">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="72a7e-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="72a7e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72a7e-125">-Confirm</span></span>
<span data-ttu-id="72a7e-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72a7e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72a7e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a7e-127">-WhatIf</span></span>
<span data-ttu-id="72a7e-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72a7e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a7e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72a7e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72a7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a7e-130">CommonParameters</span></span>
<span data-ttu-id="72a7e-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a7e-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72a7e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a7e-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72a7e-133">INPUTS</span></span>

### <span data-ttu-id="72a7e-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="72a7e-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="72a7e-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72a7e-135">OUTPUTS</span></span>

### <span data-ttu-id="72a7e-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="72a7e-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="72a7e-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72a7e-137">NOTES</span></span>

<span data-ttu-id="72a7e-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="72a7e-138">ALIASES</span></span>

<span data-ttu-id="72a7e-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="72a7e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72a7e-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="72a7e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72a7e-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72a7e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72a7e-142">INPUTOBJECT <IWindowsIotServicesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="72a7e-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72a7e-143">`[DeviceName <String>]`: Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="72a7e-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="72a7e-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="72a7e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72a7e-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="72a7e-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="72a7e-146">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="72a7e-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="72a7e-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72a7e-147">RELATED LINKS</span></span>

