---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156545"
---
# <span data-ttu-id="1a3a8-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1a3a8-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="1a3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3a8-103">Erstellt eine ASR-NIC-Konfiguration, die die Konfigurationsdetails für Failover und Test failover enthält.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="1a3a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a3a8-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a3a8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="1a3a8-106">Das **Cmdlet "New-AzRecoveryServicesAsrVMNicConfig"** erstellt ein ASR-NIC-Konfigurationsobjekt, das die Failover- und Test failoverbezogenen Details enthält.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="1a3a8-107">Falls keine Informationen übergeben werden, werden die entsprechenden Werte aus dem replikationsgeschützten Element ausgewählt, um zu verhindern, dass diese Werte auf NULL aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="1a3a8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a3a8-108">EXAMPLES</span></span>

### <span data-ttu-id="1a3a8-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a3a8-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="1a3a8-110">Erstellt ein ASRVmNicConfig-Objekt mit den für die NIC konfigurierten Failover- und Test-Faiover-Netzwerkeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="1a3a8-111">Jede Eigenschaft, die nicht oben übergeben wird, wird von dem übergebenen geschützten Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="1a3a8-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1a3a8-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="1a3a8-113">Erstellt ein ASRVmNicConfig-Objekt mit den für die Umbenennung der NIC konfigurierten Test-faiover-Netzwerkeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="1a3a8-114">Jede Eigenschaft, die nicht oben übergeben wird, wird von dem übergebenen geschützten Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="1a3a8-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1a3a8-115">Example 3</span></span>

<span data-ttu-id="1a3a8-116">Erstellt eine ASR-NIC-Konfiguration, die die Konfigurationsdetails für Failover und Test failover enthält.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="1a3a8-117">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="1a3a8-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="1a3a8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a3a8-118">PARAMETERS</span></span>

### <span data-ttu-id="1a3a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3a8-119">-DefaultProfile</span></span>
<span data-ttu-id="1a3a8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a3a8-121">-EnableAcce inNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="1a3a8-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="1a3a8-122">Gibt an, ob beschleunigtes Netzwerk auf der Wiederherstellungs-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="1a3a8-123">-EnableAcce 2010NetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="1a3a8-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="1a3a8-124">Gibt an, ob beschleunigtes Netzwerk auf der Failover-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="1a3a8-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-125">-NicId</span></span>
<span data-ttu-id="1a3a8-126">Geben Sie die ASR-NIC-GUID an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="1a3a8-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="1a3a8-128">Gibt die IDs der Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3a8-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="1a3a8-130">Gibt die ID des NSG an, das der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1a3a8-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-131">-RecoveryNicName</span></span>
<span data-ttu-id="1a3a8-132">Gibt den Namen der Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="1a3a8-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="1a3a8-134">Gibt den Namen der Wiederherstellungs-NIC-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="1a3a8-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1a3a8-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1a3a8-136">Gibt die IP-Adresse der Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="1a3a8-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="1a3a8-138">Gibt die ID der öffentlichen IP-Adresse an, die der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1a3a8-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="1a3a8-140">Gibt die ID des virtuellen Wiederherstellungsnetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="1a3a8-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="1a3a8-142">Gibt den Namen des Wiederherstellungssubnetzs an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="1a3a8-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a3a8-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1a3a8-144">Geben Sie das geschützte Element für die ASR-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3a8-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="1a3a8-145">-ReuseExistingNic</span></span>
<span data-ttu-id="1a3a8-146">Gibt an, ob eine vorhandene NIC während eines Failovers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="1a3a8-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="1a3a8-148">Gibt die IDs der Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3a8-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="1a3a8-150">Gibt die ID der NSG an, die der Test failover NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1a3a8-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-151">-TfoNicName</span></span>
<span data-ttu-id="1a3a8-152">Gibt den Namen der Test-Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="1a3a8-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="1a3a8-154">Gibt den Namen der Test-Failover-NIC-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="1a3a8-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1a3a8-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="1a3a8-156">Gibt die IP-Adresse der Test-Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="1a3a8-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="1a3a8-158">Gibt die ID der öffentlichen IP-Adresse an, die der Test failover NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1a3a8-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="1a3a8-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="1a3a8-160">Gibt an, ob eine vorhandene NIC während eines Test failover verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="1a3a8-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1a3a8-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="1a3a8-162">Gibt die ID des virtuellen Test failovernetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="1a3a8-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1a3a8-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="1a3a8-164">Gibt den Namen des Test-Failover-Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="1a3a8-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a3a8-165">-Confirm</span></span>
<span data-ttu-id="1a3a8-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a3a8-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a3a8-167">-WhatIf</span></span>
<span data-ttu-id="1a3a8-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a3a8-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a3a8-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3a8-170">CommonParameters</span></span>
<span data-ttu-id="1a3a8-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a3a8-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3a8-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a3a8-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3a8-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a3a8-173">INPUTS</span></span>

### <span data-ttu-id="1a3a8-174">Keine</span><span class="sxs-lookup"><span data-stu-id="1a3a8-174">None</span></span>

## <span data-ttu-id="1a3a8-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a3a8-175">OUTPUTS</span></span>

### <span data-ttu-id="1a3a8-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1a3a8-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="1a3a8-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a3a8-177">NOTES</span></span>

## <span data-ttu-id="1a3a8-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a3a8-178">RELATED LINKS</span></span>
