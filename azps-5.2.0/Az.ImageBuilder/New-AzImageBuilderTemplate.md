---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297274"
---
# <span data-ttu-id="d817c-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="d817c-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="d817c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d817c-102">SYNOPSIS</span></span>
<span data-ttu-id="d817c-103">Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d817c-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="d817c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d817c-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d817c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d817c-105">DESCRIPTION</span></span>
<span data-ttu-id="d817c-106">Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d817c-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="d817c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d817c-107">EXAMPLES</span></span>

### <span data-ttu-id="d817c-108">Beispiel 1: Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d817c-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="d817c-109">Mit diesen Befehlen wird eine Bildvorlage für einen virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="d817c-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="d817c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d817c-110">PARAMETERS</span></span>

### <span data-ttu-id="d817c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d817c-111">-AsJob</span></span>
<span data-ttu-id="d817c-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d817c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d817c-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="d817c-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="d817c-114">Maximale Wartezeit beim Erstellen der Bildvorlage.</span><span class="sxs-lookup"><span data-stu-id="d817c-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="d817c-115">Lassen Sie "0" weg, oder geben Sie "0" an, um den Standardwert (4 Stunden) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d817c-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-116">-Customize</span><span class="sxs-lookup"><span data-stu-id="d817c-116">-Customize</span></span>
<span data-ttu-id="d817c-117">Gibt die Eigenschaften an, die verwendet werden, um die Anpassungsschritte des Bilds zu beschreiben, z. B. Bildquelle usw. Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für "ANPASSEN"-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d817c-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d817c-118">-DefaultProfile</span></span>
<span data-ttu-id="d817c-119">Region HideParameter Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d817c-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d817c-120">-Distribute</span><span class="sxs-lookup"><span data-stu-id="d817c-120">-Distribute</span></span>
<span data-ttu-id="d817c-121">Die Verteilung zielt ab, an die die Bildausgabe gehen muss.</span><span class="sxs-lookup"><span data-stu-id="d817c-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="d817c-122">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d817c-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="d817c-123">-ImageTemplateName</span></span>
<span data-ttu-id="d817c-124">Der Name der Bildvorlage.</span><span class="sxs-lookup"><span data-stu-id="d817c-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="d817c-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="d817c-126">Endzeit der letzten Ausführung (UTC).</span><span class="sxs-lookup"><span data-stu-id="d817c-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="d817c-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="d817c-128">Ausführliche Informationen zum Zustand der letzten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="d817c-128">Verbose information about the last run state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="d817c-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="d817c-130">Status der letzten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="d817c-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="d817c-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="d817c-132">Unterzustand der letzten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="d817c-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="d817c-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="d817c-134">Startzeit der letzten Ausführung (UTC).</span><span class="sxs-lookup"><span data-stu-id="d817c-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-135">-Location</span><span class="sxs-lookup"><span data-stu-id="d817c-135">-Location</span></span>
<span data-ttu-id="d817c-136">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="d817c-136">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d817c-137">-NoWait</span></span>
<span data-ttu-id="d817c-138">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d817c-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d817c-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="d817c-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="d817c-140">Fehlercode des Bereitstellungsfehlers.</span><span class="sxs-lookup"><span data-stu-id="d817c-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d817c-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="d817c-142">Ausführliche Fehlermeldung zum Bereitstellungsfehler.</span><span class="sxs-lookup"><span data-stu-id="d817c-142">Verbose error message about the provisioning failure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d817c-143">-ResourceGroupName</span></span>
<span data-ttu-id="d817c-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d817c-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="d817c-145">-Source</span><span class="sxs-lookup"><span data-stu-id="d817c-145">-Source</span></span>
<span data-ttu-id="d817c-146">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="d817c-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="d817c-147">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d817c-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d817c-148">-SubscriptionId</span></span>
<span data-ttu-id="d817c-149">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d817c-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="d817c-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="d817c-150">-Tag</span></span>
<span data-ttu-id="d817c-151">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="d817c-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="d817c-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="d817c-153">Die ID der vom Benutzer zugewiesenen Identität.</span><span class="sxs-lookup"><span data-stu-id="d817c-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="d817c-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="d817c-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="d817c-155">Die Größe des Betriebssystemdatenträgers in GB.</span><span class="sxs-lookup"><span data-stu-id="d817c-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="d817c-156">Geben Sie "0" aus, um die standardmäßige Betriebssystemdatenträgergröße von Azure zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d817c-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="d817c-157">-VMProfileVmSize</span></span>
<span data-ttu-id="d817c-158">Die Größe des virtuellen Computers, der zum Erstellen, Anpassen und Erfassen von Bildern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d817c-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="d817c-159">Lassen Sie eine leere Zeichenfolge weg, oder geben Sie sie an, um die Standardzeichenfolge (Standard_D1_v2) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d817c-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="d817c-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="d817c-161">Ressourcen-ID eines bereits vorhandenen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="d817c-161">Resource id of a pre-existing subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d817c-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d817c-162">-Confirm</span></span>
<span data-ttu-id="d817c-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d817c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d817c-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d817c-164">-WhatIf</span></span>
<span data-ttu-id="d817c-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d817c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d817c-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d817c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d817c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d817c-167">CommonParameters</span></span>
<span data-ttu-id="d817c-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d817c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d817c-169">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d817c-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d817c-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d817c-170">INPUTS</span></span>

## <span data-ttu-id="d817c-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d817c-171">OUTPUTS</span></span>

### <span data-ttu-id="d817c-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="d817c-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="d817c-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d817c-173">NOTES</span></span>

<span data-ttu-id="d817c-174">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d817c-174">ALIASES</span></span>

<span data-ttu-id="d817c-175">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d817c-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d817c-176">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d817c-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d817c-177">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d817c-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d817c-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Gibt die Eigenschaften an, die verwendet werden, um die Anpassungsschritte des Bilds zu beschreiben, z. B. Bildquelle usw.</span><span class="sxs-lookup"><span data-stu-id="d817c-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="d817c-179">`Type <String>`: Der Typ des Anpassungstools, den Sie für das Bild verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="d817c-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="d817c-180">"Shell" kann z. B. ein Shell-Customizer sein.</span><span class="sxs-lookup"><span data-stu-id="d817c-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="d817c-181">`[Name <String>]`: Anzeigename, der Kontext zu den Durchschritten dieses Anpassungsschritts bietet</span><span class="sxs-lookup"><span data-stu-id="d817c-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="d817c-182">DISTRIBUTE <IImageTemplateDistributor[]>: Die Verteilungsziele, an die die Bildausgabe übergeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d817c-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="d817c-183">`RunOutputName <String>`: Der Name, der für den zugeordneten RunOutput verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d817c-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="d817c-184">`Type <String>`: Verteilungsart</span><span class="sxs-lookup"><span data-stu-id="d817c-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="d817c-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags, die auf das Artefakt angewendet werden, nachdem es vom Distributor erstellt/aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d817c-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="d817c-186">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="d817c-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="d817c-187">SOURCE : Beschreibt eine Bildquelle für einen virtuellen Computer zum <IImageTemplateSource> Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="d817c-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="d817c-188">`Type <String>`: Gibt den Typ des Quellbilds an, mit dem Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="d817c-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="d817c-189">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d817c-189">RELATED LINKS</span></span>

