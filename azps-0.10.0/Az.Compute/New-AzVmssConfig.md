---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844451"
---
# <span data-ttu-id="f512e-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f512e-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="f512e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f512e-102">SYNOPSIS</span></span>
<span data-ttu-id="f512e-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f512e-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="f512e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f512e-104">SYNTAX</span></span>

### <span data-ttu-id="f512e-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f512e-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f512e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f512e-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f512e-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f512e-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f512e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f512e-108">DESCRIPTION</span></span>
<span data-ttu-id="f512e-109">Das Cmdlet **New-AzVmssConfig** erstellt ein konfigurierbares lokales Virtual Manager-Skalierungs Satz Objekt (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f512e-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="f512e-110">Zum Konfigurieren des VMSS-Objekts sind andere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f512e-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="f512e-111">Diese Cmdlets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f512e-111">These cmdlets are:</span></span>

- <span data-ttu-id="f512e-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="f512e-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="f512e-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f512e-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="f512e-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f512e-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="f512e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f512e-116">EXAMPLES</span></span>

### <span data-ttu-id="f512e-117">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="f512e-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="f512e-118">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f512e-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="f512e-119">Der erste Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f512e-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="f512e-120">Der zweite Befehl verwendet das Cmdlet **New-AzVmss** zum Erstellen eines VMSS, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f512e-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="f512e-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="f512e-121">PARAMETERS</span></span>

### <span data-ttu-id="f512e-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f512e-122">-AssignIdentity</span></span>
<span data-ttu-id="f512e-123">Geben Sie die zugewiesene System Identität für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f512e-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f512e-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="f512e-125">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f512e-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f512e-126">-BootDiagnostic</span></span>
<span data-ttu-id="f512e-127">Gibt das Start Diagnose Profil für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="f512e-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-128">-DefaultProfile</span></span>
<span data-ttu-id="f512e-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f512e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-130">-Extension</span><span class="sxs-lookup"><span data-stu-id="f512e-130">-Extension</span></span>
<span data-ttu-id="f512e-131">Gibt das Erweiterungs Informationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f512e-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="f512e-132">Sie können das **Add-AzVmssExtension-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f512e-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="f512e-133">-HealthProbeId</span></span>
<span data-ttu-id="f512e-134">Gibt die ID eines Load Balancer-Prüfpunkts an, der zum Ermitteln des Zustands einer Instanz im Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f512e-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="f512e-135">HealthProbeId ist in Form von "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/loadBalancers/{loadBalancerName}/Probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="f512e-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-136">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="f512e-136">-IdentityId</span></span>
<span data-ttu-id="f512e-137">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f512e-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="f512e-138">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="f512e-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f512e-139">-IdentityType</span></span>
<span data-ttu-id="f512e-140">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f512e-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="f512e-141">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="f512e-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="f512e-142">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f512e-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="f512e-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f512e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f512e-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f512e-144">SystemAssigned</span></span>
- <span data-ttu-id="f512e-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="f512e-145">UserAssigned</span></span>
- <span data-ttu-id="f512e-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="f512e-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="f512e-147">Keine</span><span class="sxs-lookup"><span data-stu-id="f512e-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f512e-148">-LicenseType</span></span>
<span data-ttu-id="f512e-149">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="f512e-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-150">-Standort</span><span class="sxs-lookup"><span data-stu-id="f512e-150">-Location</span></span>
<span data-ttu-id="f512e-151">Gibt die Azure-Position an, an der die VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f512e-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f512e-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="f512e-153">Gibt das Netzwerkprofil Objekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f512e-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="f512e-154">Sie können das **Add-AzVmssNetworkInterfaceConfiguration-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f512e-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-155">-OsProfile</span></span>
<span data-ttu-id="f512e-156">Gibt das Betriebssystem-Profilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f512e-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="f512e-157">Sie können das Cmdlet " **Satz-AzVmssOsProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f512e-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-158">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="f512e-158">-Overprovision</span></span>
<span data-ttu-id="f512e-159">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f512e-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-160">-Planname</span><span class="sxs-lookup"><span data-stu-id="f512e-160">-PlanName</span></span>
<span data-ttu-id="f512e-161">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="f512e-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="f512e-162">-PlanProduct</span></span>
<span data-ttu-id="f512e-163">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="f512e-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="f512e-164">-PlanPromotionCode</span></span>
<span data-ttu-id="f512e-165">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="f512e-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f512e-166">-PlanPublisher</span></span>
<span data-ttu-id="f512e-167">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="f512e-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-168">-Priorität</span><span class="sxs-lookup"><span data-stu-id="f512e-168">-Priority</span></span>
<span data-ttu-id="f512e-169">Gibt die Priorität für die virtuellen Computer in der Skalierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="f512e-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f512e-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="f512e-171">Gibt die Richtlinie zum parallelen Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="f512e-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f512e-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="f512e-173">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="f512e-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f512e-174">-SkuCapacity</span></span>
<span data-ttu-id="f512e-175">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f512e-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f512e-176">-SkuName</span></span>
<span data-ttu-id="f512e-177">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f512e-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f512e-178">-SkuTier</span></span>
<span data-ttu-id="f512e-179">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="f512e-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="f512e-180">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f512e-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f512e-181">Standard</span><span class="sxs-lookup"><span data-stu-id="f512e-181">Standard</span></span>
- <span data-ttu-id="f512e-182">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="f512e-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-183">-StorageProfile</span></span>
<span data-ttu-id="f512e-184">Gibt das Speicherprofil Objekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f512e-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="f512e-185">Sie können das Cmdlet " **Satz-AzVmssStorageProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f512e-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="f512e-186">-Tag</span></span>
<span data-ttu-id="f512e-187">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f512e-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f512e-188">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f512e-188">For example:</span></span>

<span data-ttu-id="f512e-189">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f512e-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="f512e-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="f512e-191">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="f512e-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="f512e-192">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f512e-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f512e-193">Automatisch</span><span class="sxs-lookup"><span data-stu-id="f512e-193">Automatic</span></span>
- <span data-ttu-id="f512e-194">Manuell</span><span class="sxs-lookup"><span data-stu-id="f512e-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="f512e-195">-Zone</span></span>
<span data-ttu-id="f512e-196">Gibt die Zonenliste für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f512e-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-197">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f512e-197">-Confirm</span></span>
<span data-ttu-id="f512e-198">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f512e-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f512e-199">-WhatIf</span></span>
<span data-ttu-id="f512e-200">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f512e-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f512e-201">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f512e-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f512e-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f512e-202">CommonParameters</span></span>
<span data-ttu-id="f512e-203">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f512e-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f512e-204">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f512e-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f512e-205">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f512e-205">INPUTS</span></span>

### <span data-ttu-id="f512e-206">Keine</span><span class="sxs-lookup"><span data-stu-id="f512e-206">None</span></span>
<span data-ttu-id="f512e-207">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f512e-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f512e-208">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f512e-208">OUTPUTS</span></span>

### <span data-ttu-id="f512e-209">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f512e-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f512e-210">Notizen</span><span class="sxs-lookup"><span data-stu-id="f512e-210">NOTES</span></span>

## <span data-ttu-id="f512e-211">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f512e-211">RELATED LINKS</span></span>

[<span data-ttu-id="f512e-212">Satz-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="f512e-213">Satz-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f512e-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="f512e-214">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f512e-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="f512e-215">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f512e-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="f512e-216">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="f512e-216">New-AzVmss</span></span>](./New-AzVmss.md)
