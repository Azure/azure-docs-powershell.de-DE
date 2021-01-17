---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467748"
---
# <span data-ttu-id="da404-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="da404-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="da404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da404-102">SYNOPSIS</span></span>
<span data-ttu-id="da404-103">Aktualisieren Sie die Metadaten von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="da404-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="da404-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da404-104">SYNTAX</span></span>

### <span data-ttu-id="da404-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="da404-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da404-106">Update</span><span class="sxs-lookup"><span data-stu-id="da404-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da404-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da404-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da404-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="da404-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da404-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da404-109">DESCRIPTION</span></span>
<span data-ttu-id="da404-110">Aktualisieren Sie die Metadaten von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="da404-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="da404-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da404-111">EXAMPLES</span></span>

### <span data-ttu-id="da404-112">Beispiel 1: UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="da404-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="da404-113">Aktualisieren der angegebenen DigitalTwinsInstance nach ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da404-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="da404-114">Beispiel 2: Aktualisieren von AzDigitalTwinsInstance durch ein anderes AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="da404-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="da404-115">Aktualisieren von AzDigitalTwinsInstance durch ein anderes AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="da404-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="da404-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da404-116">PARAMETERS</span></span>

### <span data-ttu-id="da404-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da404-117">-DefaultProfile</span></span>
<span data-ttu-id="da404-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da404-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da404-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="da404-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="da404-120">Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="da404-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="da404-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für die Eigenschaften VON DIGITALTWINSPATCHDESCRIPTION und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="da404-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da404-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da404-122">-InputObject</span></span>
<span data-ttu-id="da404-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="da404-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da404-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da404-124">-ResourceGroupName</span></span>
<span data-ttu-id="da404-125">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="da404-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da404-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="da404-126">-ResourceName</span></span>
<span data-ttu-id="da404-127">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="da404-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da404-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da404-128">-SubscriptionId</span></span>
<span data-ttu-id="da404-129">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="da404-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da404-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="da404-130">-Tag</span></span>
<span data-ttu-id="da404-131">Instanztags</span><span class="sxs-lookup"><span data-stu-id="da404-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da404-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da404-132">-Confirm</span></span>
<span data-ttu-id="da404-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da404-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da404-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da404-134">-WhatIf</span></span>
<span data-ttu-id="da404-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da404-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da404-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da404-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da404-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da404-137">CommonParameters</span></span>
<span data-ttu-id="da404-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da404-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da404-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da404-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da404-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da404-140">INPUTS</span></span>

### <span data-ttu-id="da404-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="da404-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="da404-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="da404-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="da404-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da404-143">OUTPUTS</span></span>

### <span data-ttu-id="da404-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="da404-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="da404-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da404-145">NOTES</span></span>

<span data-ttu-id="da404-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="da404-146">ALIASES</span></span>

<span data-ttu-id="da404-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="da404-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da404-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da404-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da404-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da404-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da404-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="da404-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="da404-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instanztags</span><span class="sxs-lookup"><span data-stu-id="da404-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="da404-152">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="da404-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="da404-153">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="da404-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da404-154">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="da404-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="da404-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="da404-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da404-156">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="da404-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="da404-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="da404-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="da404-158">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="da404-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="da404-159">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="da404-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="da404-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da404-160">RELATED LINKS</span></span>

