---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 967b50b024e02d4a88fa2a1d91905acad5385b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935096"
---
# <span data-ttu-id="b2b70-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b2b70-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b2b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b70-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b70-103">Aktualisieren Sie Metadaten von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b2b70-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b2b70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2b70-104">SYNTAX</span></span>

### <span data-ttu-id="b2b70-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2b70-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2b70-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b2b70-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2b70-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2b70-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2b70-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b2b70-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2b70-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2b70-109">DESCRIPTION</span></span>
<span data-ttu-id="b2b70-110">Aktualisieren Sie Metadaten von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b2b70-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b2b70-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2b70-111">EXAMPLES</span></span>

### <span data-ttu-id="b2b70-112">Beispiel 1: UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2b70-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b2b70-113">Aktualisieren des angegebenen DigitalTwinsInstance von ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b70-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="b2b70-114">Beispiel 2: Aktualisieren der AzDigitalTwinsInstance durch ein anderes AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b2b70-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b2b70-115">Aktualisieren der AzDigitalTwinsInstance durch eine andere AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b2b70-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b2b70-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2b70-116">PARAMETERS</span></span>

### <span data-ttu-id="b2b70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b70-117">-DefaultProfile</span></span>
<span data-ttu-id="b2b70-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2b70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b70-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="b2b70-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="b2b70-120">Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="b2b70-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="b2b70-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu digitalTWINSPATCHDESCRIPTION-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b2b70-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2b70-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2b70-122">-InputObject</span></span>
<span data-ttu-id="b2b70-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b2b70-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2b70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b70-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2b70-125">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="b2b70-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b2b70-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b2b70-126">-ResourceName</span></span>
<span data-ttu-id="b2b70-127">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b2b70-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b2b70-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2b70-128">-SubscriptionId</span></span>
<span data-ttu-id="b2b70-129">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2b70-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="b2b70-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2b70-130">-Tag</span></span>
<span data-ttu-id="b2b70-131">Instanztags</span><span class="sxs-lookup"><span data-stu-id="b2b70-131">Instance tags</span></span>

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

### <span data-ttu-id="b2b70-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2b70-132">-Confirm</span></span>
<span data-ttu-id="b2b70-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2b70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b70-134">-WhatIf</span></span>
<span data-ttu-id="b2b70-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2b70-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b70-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2b70-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b70-137">CommonParameters</span></span>
<span data-ttu-id="b2b70-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b70-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2b70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b70-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2b70-140">INPUTS</span></span>

### <span data-ttu-id="b2b70-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="b2b70-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="b2b70-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b2b70-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b2b70-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2b70-143">OUTPUTS</span></span>

### <span data-ttu-id="b2b70-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b2b70-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b2b70-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2b70-145">NOTES</span></span>

<span data-ttu-id="b2b70-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b2b70-146">ALIASES</span></span>

<span data-ttu-id="b2b70-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b2b70-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2b70-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b2b70-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2b70-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2b70-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2b70-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="b2b70-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="b2b70-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instanztags</span><span class="sxs-lookup"><span data-stu-id="b2b70-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="b2b70-152">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2b70-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="b2b70-153">INPUTOBJECT <IDigitalTwinsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b2b70-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2b70-154">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="b2b70-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b2b70-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b2b70-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2b70-156">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b2b70-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b2b70-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="b2b70-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b2b70-158">`[ResourceName <String>]`: Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b2b70-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b2b70-159">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2b70-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b2b70-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2b70-160">RELATED LINKS</span></span>

