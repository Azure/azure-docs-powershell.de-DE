---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661505"
---
# <span data-ttu-id="5da74-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5da74-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="5da74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5da74-102">SYNOPSIS</span></span>
<span data-ttu-id="5da74-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5da74-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="5da74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da74-104">SYNTAX</span></span>

### <span data-ttu-id="5da74-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5da74-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da74-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5da74-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da74-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5da74-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5da74-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5da74-108">DESCRIPTION</span></span>
<span data-ttu-id="5da74-109">Das Cmdlet **New-AzVmssConfig** erstellt ein konfigurierbares lokales Virtual Manager-Skalierungs Satz Objekt (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5da74-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="5da74-110">Zum Konfigurieren des VMSS-Objekts sind andere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5da74-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="5da74-111">Diese Cmdlets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5da74-111">These cmdlets are:</span></span>
- <span data-ttu-id="5da74-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="5da74-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="5da74-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da74-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="5da74-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5da74-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="5da74-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5da74-116">EXAMPLES</span></span>

### <span data-ttu-id="5da74-117">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="5da74-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="5da74-118">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="5da74-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="5da74-119">Der erste Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5da74-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="5da74-120">Der zweite Befehl verwendet das Cmdlet **New-AzVmss** zum Erstellen eines VMSS, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5da74-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="5da74-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="5da74-121">PARAMETERS</span></span>

### <span data-ttu-id="5da74-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5da74-122">-AssignIdentity</span></span>
<span data-ttu-id="5da74-123">Geben Sie die zugewiesene System Identität für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="5da74-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5da74-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="5da74-125">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5da74-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="5da74-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5da74-126">-BootDiagnostic</span></span>
<span data-ttu-id="5da74-127">Gibt das Start Diagnose Profil für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5da74-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="5da74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-128">-DefaultProfile</span></span>
<span data-ttu-id="5da74-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5da74-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da74-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="5da74-130">-DisableAutoRollback</span></span>
<span data-ttu-id="5da74-131">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="5da74-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5da74-132">-EnableUltraSSD</span></span>
<span data-ttu-id="5da74-133">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine besitzt.</span><span class="sxs-lookup"><span data-stu-id="5da74-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="5da74-134">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5da74-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5da74-135">-EvictionPolicy</span></span>
<span data-ttu-id="5da74-136">Gibt die Räumungs Richtlinie für die virtuellen Computer in der Skalierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="5da74-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="5da74-137">-Extension</span><span class="sxs-lookup"><span data-stu-id="5da74-137">-Extension</span></span>
<span data-ttu-id="5da74-138">Gibt das Erweiterungs Informationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5da74-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="5da74-139">Sie können das **Add-AzVmssExtension-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5da74-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5da74-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="5da74-140">-HealthProbeId</span></span>
<span data-ttu-id="5da74-141">Gibt die ID eines Load Balancer-Prüfpunkts an, der zum Ermitteln des Zustands einer Instanz im Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5da74-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="5da74-142">HealthProbeId ist in Form von "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/loadBalancers/{loadBalancerName}/Probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="5da74-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="5da74-143">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="5da74-143">-IdentityId</span></span>
<span data-ttu-id="5da74-144">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5da74-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5da74-145">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="5da74-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5da74-146">-IdentityType</span></span>
<span data-ttu-id="5da74-147">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5da74-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="5da74-148">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="5da74-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="5da74-149">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="5da74-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="5da74-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5da74-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5da74-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5da74-151">SystemAssigned</span></span>
- <span data-ttu-id="5da74-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="5da74-152">UserAssigned</span></span>
- <span data-ttu-id="5da74-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="5da74-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="5da74-154">Keine</span><span class="sxs-lookup"><span data-stu-id="5da74-154">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5da74-155">-LicenseType</span></span>
<span data-ttu-id="5da74-156">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="5da74-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5da74-157">-Standort</span><span class="sxs-lookup"><span data-stu-id="5da74-157">-Location</span></span>
<span data-ttu-id="5da74-158">Gibt die Azure-Position an, an der die VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5da74-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="5da74-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da74-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="5da74-160">Gibt das Netzwerkprofil Objekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5da74-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="5da74-161">Sie können das **Add-AzVmssNetworkInterfaceConfiguration-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5da74-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5da74-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-162">-OsProfile</span></span>
<span data-ttu-id="5da74-163">Gibt das Betriebssystem-Profilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5da74-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="5da74-164">Sie können das Cmdlet " **Satz-AzVmssOsProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5da74-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5da74-165">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="5da74-165">-Overprovision</span></span>
<span data-ttu-id="5da74-166">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5da74-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="5da74-167">-Planname</span><span class="sxs-lookup"><span data-stu-id="5da74-167">-PlanName</span></span>
<span data-ttu-id="5da74-168">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="5da74-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="5da74-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5da74-169">-PlanProduct</span></span>
<span data-ttu-id="5da74-170">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="5da74-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="5da74-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5da74-171">-PlanPromotionCode</span></span>
<span data-ttu-id="5da74-172">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="5da74-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="5da74-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5da74-173">-PlanPublisher</span></span>
<span data-ttu-id="5da74-174">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="5da74-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="5da74-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="5da74-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="5da74-176">Anzahl der fehlerdomänen für jede Placement-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5da74-176">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-177">-Priorität</span><span class="sxs-lookup"><span data-stu-id="5da74-177">-Priority</span></span>
<span data-ttu-id="5da74-178">Gibt die Priorität für die virtuellen Computer in der Skalierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="5da74-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="5da74-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5da74-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="5da74-180">Gibt die Richtlinie zum parallelen Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="5da74-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="5da74-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5da74-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="5da74-182">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="5da74-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="5da74-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5da74-183">-SkuCapacity</span></span>
<span data-ttu-id="5da74-184">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5da74-184">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da74-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5da74-185">-SkuName</span></span>
<span data-ttu-id="5da74-186">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5da74-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="5da74-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5da74-187">-SkuTier</span></span>
<span data-ttu-id="5da74-188">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="5da74-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="5da74-189">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5da74-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5da74-190">Standard</span><span class="sxs-lookup"><span data-stu-id="5da74-190">Standard</span></span>
- <span data-ttu-id="5da74-191">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="5da74-191">Basic</span></span>

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

### <span data-ttu-id="5da74-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-192">-StorageProfile</span></span>
<span data-ttu-id="5da74-193">Gibt das Speicherprofil Objekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5da74-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="5da74-194">Sie können das Cmdlet " **Satz-AzVmssStorageProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5da74-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5da74-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="5da74-195">-Tag</span></span>
<span data-ttu-id="5da74-196">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="5da74-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5da74-197">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="5da74-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5da74-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5da74-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="5da74-199">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="5da74-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="5da74-200">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5da74-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5da74-201">Automatisch</span><span class="sxs-lookup"><span data-stu-id="5da74-201">Automatic</span></span>
- <span data-ttu-id="5da74-202">Manuell</span><span class="sxs-lookup"><span data-stu-id="5da74-202">Manual</span></span>

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

### <span data-ttu-id="5da74-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="5da74-203">-Zone</span></span>
<span data-ttu-id="5da74-204">Gibt die Zonenliste für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="5da74-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5da74-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="5da74-205">-ZoneBalance</span></span>
<span data-ttu-id="5da74-206">Ob eine strikte selbst Verteilung der virtuellen Computer über x-Zonen erzwungen werden soll, wenn ein Zonen Ausfall vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5da74-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="5da74-207">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5da74-207">-Confirm</span></span>
<span data-ttu-id="5da74-208">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5da74-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da74-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da74-209">-WhatIf</span></span>
<span data-ttu-id="5da74-210">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5da74-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5da74-211">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5da74-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da74-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da74-212">CommonParameters</span></span>
<span data-ttu-id="5da74-213">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da74-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da74-214">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da74-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da74-215">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5da74-215">INPUTS</span></span>

### <span data-ttu-id="5da74-216">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5da74-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5da74-217">System. String</span><span class="sxs-lookup"><span data-stu-id="5da74-217">System.String</span></span>

### <span data-ttu-id="5da74-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5da74-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5da74-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5da74-219">System.Int32</span></span>

### <span data-ttu-id="5da74-220">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5da74-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5da74-221">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="5da74-222">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="5da74-223">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="5da74-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="5da74-224">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="5da74-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="5da74-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="5da74-225">System.String[]</span></span>

### <span data-ttu-id="5da74-226">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5da74-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="5da74-227">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5da74-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5da74-228">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5da74-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="5da74-229">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5da74-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5da74-230">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5da74-230">OUTPUTS</span></span>

### <span data-ttu-id="5da74-231">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5da74-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5da74-232">Notizen</span><span class="sxs-lookup"><span data-stu-id="5da74-232">NOTES</span></span>

## <span data-ttu-id="5da74-233">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5da74-233">RELATED LINKS</span></span>

[<span data-ttu-id="5da74-234">Satz-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="5da74-235">Satz-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5da74-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="5da74-236">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da74-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5da74-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5da74-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="5da74-238">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="5da74-238">New-AzVmss</span></span>](./New-AzVmss.md)
