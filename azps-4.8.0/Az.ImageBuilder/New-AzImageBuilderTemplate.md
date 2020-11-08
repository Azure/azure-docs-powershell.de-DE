---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166615"
---
# <span data-ttu-id="52613-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="52613-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="52613-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52613-102">SYNOPSIS</span></span>
<span data-ttu-id="52613-103">Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="52613-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="52613-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52613-104">SYNTAX</span></span>

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

## <span data-ttu-id="52613-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52613-105">DESCRIPTION</span></span>
<span data-ttu-id="52613-106">Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="52613-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="52613-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52613-107">EXAMPLES</span></span>

### <span data-ttu-id="52613-108">Beispiel 1: Erstellen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="52613-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="52613-109">Mit diesen Befehlen wird eine Bildvorlage für einen virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="52613-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="52613-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52613-110">PARAMETERS</span></span>

### <span data-ttu-id="52613-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52613-111">-AsJob</span></span>
<span data-ttu-id="52613-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="52613-112">Run the command as a job</span></span>

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

### <span data-ttu-id="52613-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="52613-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="52613-114">Maximale Dauer, die beim Erstellen der Bildvorlage gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52613-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="52613-115">Geben Sie "0" aus, um den Standardwert (4 Stunden) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="52613-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="52613-116">– Anpassen</span><span class="sxs-lookup"><span data-stu-id="52613-116">-Customize</span></span>
<span data-ttu-id="52613-117">Gibt die Eigenschaften an, mit denen die Anpassungsschritte des Bilds beschrieben werden, beispielsweise Bildquelle usw. Informationen zum Erstellen finden Sie unter Abschnitt "Notizen", um Eigenschaften anzupassen und eine Hashtabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="52613-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="52613-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52613-118">-DefaultProfile</span></span>
<span data-ttu-id="52613-119">Region ausblendenparameter die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52613-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52613-120">– Verteilen</span><span class="sxs-lookup"><span data-stu-id="52613-120">-Distribute</span></span>
<span data-ttu-id="52613-121">Die verteilungsziele, zu denen die Bildausgabe wechseln muss.</span><span class="sxs-lookup"><span data-stu-id="52613-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="52613-122">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" zum Verteilen von Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="52613-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="52613-123">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="52613-123">-ImageTemplateName</span></span>
<span data-ttu-id="52613-124">Der Name der Bildvorlage.</span><span class="sxs-lookup"><span data-stu-id="52613-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="52613-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="52613-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="52613-126">Endzeit des letzten Ausführungszeitraums (UTC).</span><span class="sxs-lookup"><span data-stu-id="52613-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="52613-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="52613-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="52613-128">Ausführliche Informationen zum letzten Ausführungszustand.</span><span class="sxs-lookup"><span data-stu-id="52613-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="52613-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="52613-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="52613-130">Der Zustand der letzten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="52613-130">State of the last run.</span></span>

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

### <span data-ttu-id="52613-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="52613-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="52613-132">Der unter Status des letzten Laufs.</span><span class="sxs-lookup"><span data-stu-id="52613-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="52613-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="52613-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="52613-134">Anfangszeit der letzten Ausführung (UTC).</span><span class="sxs-lookup"><span data-stu-id="52613-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="52613-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="52613-135">-Location</span></span>
<span data-ttu-id="52613-136">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="52613-136">Resource location.</span></span>

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

### <span data-ttu-id="52613-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="52613-137">-NoWait</span></span>
<span data-ttu-id="52613-138">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="52613-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52613-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="52613-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="52613-140">Fehlercode des Bereitstellungs Fehlers.</span><span class="sxs-lookup"><span data-stu-id="52613-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="52613-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="52613-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="52613-142">Ausführliche Fehlermeldung zum Bereitstellungsfehler</span><span class="sxs-lookup"><span data-stu-id="52613-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="52613-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52613-143">-ResourceGroupName</span></span>
<span data-ttu-id="52613-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52613-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="52613-145">-Source</span><span class="sxs-lookup"><span data-stu-id="52613-145">-Source</span></span>
<span data-ttu-id="52613-146">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, anpassen und verteilen.</span><span class="sxs-lookup"><span data-stu-id="52613-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="52613-147">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Quelleigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="52613-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="52613-148">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="52613-148">-SubscriptionId</span></span>
<span data-ttu-id="52613-149">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="52613-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="52613-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="52613-150">-Tag</span></span>
<span data-ttu-id="52613-151">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="52613-151">Resource tags.</span></span>

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

### <span data-ttu-id="52613-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="52613-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="52613-153">Die ID der Benutzer zugewiesenen Identität.</span><span class="sxs-lookup"><span data-stu-id="52613-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="52613-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="52613-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="52613-155">Die Größe der Betriebssystemfestplatte in GB.</span><span class="sxs-lookup"><span data-stu-id="52613-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="52613-156">Geben Sie 0 aus, um die Standardfestplatten Größe von Azure zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="52613-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="52613-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="52613-157">-VMProfileVmSize</span></span>
<span data-ttu-id="52613-158">Die Größe des virtuellen Computers, der zum Erstellen, anpassen und Aufzeichnen von Bildern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52613-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="52613-159">Geben Sie eine leere Zeichenfolge aus, um den Standardwert (Standard_D1_v2) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="52613-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="52613-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="52613-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="52613-161">Die Ressourcen-ID eines bereits vorhandenen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="52613-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="52613-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52613-162">-Confirm</span></span>
<span data-ttu-id="52613-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52613-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52613-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52613-164">-WhatIf</span></span>
<span data-ttu-id="52613-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52613-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52613-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52613-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52613-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52613-167">CommonParameters</span></span>
<span data-ttu-id="52613-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52613-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52613-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52613-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52613-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52613-170">INPUTS</span></span>

## <span data-ttu-id="52613-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52613-171">OUTPUTS</span></span>

### <span data-ttu-id="52613-172">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="52613-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="52613-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="52613-173">NOTES</span></span>

<span data-ttu-id="52613-174">Aliase</span><span class="sxs-lookup"><span data-stu-id="52613-174">ALIASES</span></span>

<span data-ttu-id="52613-175">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52613-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52613-176">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52613-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52613-177">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="52613-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52613-178">Anpassen <IImageTemplateCustomizer [] >: gibt die Eigenschaften an, mit denen die Anpassungsschritte des Bilds beschrieben werden, beispielsweise Bildquelle usw.</span><span class="sxs-lookup"><span data-stu-id="52613-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="52613-179">`Type <String>`: Der Typ des Anpassungstools, das Sie für das Bild verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="52613-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="52613-180">"Shell" kann beispielsweise Shell Customizer sein.</span><span class="sxs-lookup"><span data-stu-id="52613-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="52613-181">`[Name <String>]`: Anzeige Name zum Bereitstellen des Kontexts für diesen Anpassungs Schritt</span><span class="sxs-lookup"><span data-stu-id="52613-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="52613-182">Verteilen Sie <IImageTemplateDistributor [] >: die verteilungsziele, zu denen die Bildausgabe wechseln muss.</span><span class="sxs-lookup"><span data-stu-id="52613-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="52613-183">`RunOutputName <String>`: Der Name, der für das zugeordnete RunOutput verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52613-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="52613-184">`Type <String>`: Art der Verteilung.</span><span class="sxs-lookup"><span data-stu-id="52613-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="52613-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags, die auf das Artefakt angewendet werden, nachdem es vom Verteiler erstellt/aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="52613-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="52613-186">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="52613-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="52613-187">Quelle <IImageTemplateSource> : Beschreibt die Bildquelle eines virtuellen Computers für das Erstellen, anpassen und verteilen.</span><span class="sxs-lookup"><span data-stu-id="52613-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="52613-188">`Type <String>`: Gibt den Typ des Quellbilds an, mit dem Sie beginnen möchten.</span><span class="sxs-lookup"><span data-stu-id="52613-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="52613-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52613-189">RELATED LINKS</span></span>

