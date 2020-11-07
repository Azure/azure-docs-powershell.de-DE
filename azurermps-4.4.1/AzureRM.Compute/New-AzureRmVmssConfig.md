---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664778"
---
# <span data-ttu-id="5cd19-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5cd19-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="5cd19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cd19-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd19-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5cd19-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cd19-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cd19-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd19-106">Das Cmdlet **New-AzureRmVmssConfig** erstellt ein konfigurierbares lokales Virtual Manager-Skalierungs Satz Objekt (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5cd19-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="5cd19-107">Zum Konfigurieren des VMSS-Objekts sind andere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cd19-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="5cd19-108">Diese Cmdlets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5cd19-108">These cmdlets are:</span></span>

- <span data-ttu-id="5cd19-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="5cd19-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="5cd19-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cd19-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="5cd19-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5cd19-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="5cd19-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cd19-113">EXAMPLES</span></span>

### <span data-ttu-id="5cd19-114">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="5cd19-114">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="5cd19-115">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="5cd19-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="5cd19-116">Der erste Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5cd19-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="5cd19-117">Der zweite Befehl verwendet das Cmdlet **New-AzureRmVmss** zum Erstellen eines VMSS, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cd19-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="5cd19-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cd19-118">PARAMETERS</span></span>

### <span data-ttu-id="5cd19-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5cd19-119">-AssignIdentity</span></span>
<span data-ttu-id="5cd19-120">Geben Sie die zugewiesene System Identität für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5cd19-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="5cd19-122">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5cd19-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5cd19-123">-BootDiagnostic</span></span>
<span data-ttu-id="5cd19-124">Gibt das Start Diagnose Profil für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-125">-DefaultProfile</span></span>
<span data-ttu-id="5cd19-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cd19-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd19-127">-Extension</span><span class="sxs-lookup"><span data-stu-id="5cd19-127">-Extension</span></span>
<span data-ttu-id="5cd19-128">Gibt das Erweiterungs Informationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="5cd19-129">Sie können das **Add-AzureRmVmssExtension-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5cd19-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="5cd19-130">-HealthProbeId</span></span>
<span data-ttu-id="5cd19-131">Geben Sie die ID eines Load Balancer-Prüfpunkts an, der zum Ermitteln des Zustands einer Instanz im Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cd19-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="5cd19-132">HealthProbeId ist in Form von "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/loadBalancers/{loadBalancerName}/Probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="5cd19-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5cd19-133">-IdentityType</span></span>
<span data-ttu-id="5cd19-134">Geben Sie die Identität des Skalierungs Satzes für virtuelle Maschinen an, wenn Sie konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="5cd19-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5cd19-135">-LicenseType</span></span>
<span data-ttu-id="5cd19-136">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="5cd19-136">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="5cd19-137">-Location</span></span>
<span data-ttu-id="5cd19-138">Gibt die Azure-Position an, an der die VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5cd19-138">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cd19-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="5cd19-140">Gibt das Netzwerkprofil Objekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5cd19-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="5cd19-141">Sie können das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5cd19-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-142">-OsProfile</span></span>
<span data-ttu-id="5cd19-143">Gibt das Betriebssystem-Profilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5cd19-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="5cd19-144">Sie können das Cmdlet " **Satz-AzureRmVmssOsProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5cd19-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-145">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="5cd19-145">-Overprovision</span></span>
<span data-ttu-id="5cd19-146">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5cd19-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-147">-Planname</span><span class="sxs-lookup"><span data-stu-id="5cd19-147">-PlanName</span></span>
<span data-ttu-id="5cd19-148">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-148">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5cd19-149">-PlanProduct</span></span>
<span data-ttu-id="5cd19-150">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-150">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5cd19-151">-PlanPromotionCode</span></span>
<span data-ttu-id="5cd19-152">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-152">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5cd19-153">-PlanPublisher</span></span>
<span data-ttu-id="5cd19-154">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-154">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="5cd19-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="5cd19-156">Geben Sie die Wiederherstellungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5cd19-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="5cd19-158">Gibt die Richtlinie zum parallelen Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-158">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5cd19-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="5cd19-160">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-160">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5cd19-161">-SkuCapacity</span></span>
<span data-ttu-id="5cd19-162">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5cd19-163">-SkuName</span></span>
<span data-ttu-id="5cd19-164">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-164">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5cd19-165">-SkuTier</span></span>
<span data-ttu-id="5cd19-166">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="5cd19-167">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5cd19-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cd19-168">Standard</span><span class="sxs-lookup"><span data-stu-id="5cd19-168">Standard</span></span>
- <span data-ttu-id="5cd19-169">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="5cd19-169">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-170">-StorageProfile</span></span>
<span data-ttu-id="5cd19-171">Gibt das Speicherprofil Objekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5cd19-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="5cd19-172">Sie können das Cmdlet " **Satz-AzureRmVmssStorageProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5cd19-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cd19-173">-Tag</span></span>
<span data-ttu-id="5cd19-174">Gibt die Tags an, die dem VMSS zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5cd19-174">Specifies the tags that will be assigned to the VMSS.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5cd19-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="5cd19-176">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="5cd19-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="5cd19-177">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5cd19-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cd19-178">Automatisch</span><span class="sxs-lookup"><span data-stu-id="5cd19-178">Automatic</span></span>
- <span data-ttu-id="5cd19-179">Manuell</span><span class="sxs-lookup"><span data-stu-id="5cd19-179">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="5cd19-180">-Zone</span></span>
<span data-ttu-id="5cd19-181">Gibt die Zonenliste für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="5cd19-181">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd19-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cd19-182">-Confirm</span></span>
<span data-ttu-id="5cd19-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cd19-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd19-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd19-184">-WhatIf</span></span>
<span data-ttu-id="5cd19-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cd19-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cd19-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cd19-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd19-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd19-187">CommonParameters</span></span>
<span data-ttu-id="5cd19-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd19-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd19-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd19-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd19-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cd19-190">INPUTS</span></span>

## <span data-ttu-id="5cd19-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cd19-191">OUTPUTS</span></span>

### <span data-ttu-id="5cd19-192">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5cd19-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5cd19-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cd19-193">NOTES</span></span>

## <span data-ttu-id="5cd19-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cd19-194">RELATED LINKS</span></span>

[<span data-ttu-id="5cd19-195">Satz-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="5cd19-196">Satz-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5cd19-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="5cd19-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cd19-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5cd19-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5cd19-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="5cd19-199">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5cd19-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


