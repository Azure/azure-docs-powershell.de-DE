---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174469"
---
# <span data-ttu-id="a5cb9-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a5cb9-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="a5cb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cb9-103">Erstellt eine ASR-NIC-Konfiguration, die die Konfigurationsdetails Failover und Test für Failover enthält.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="a5cb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5cb9-104">SYNTAX</span></span>

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

## <span data-ttu-id="a5cb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cb9-106">Mit dem Cmdlet **New-AzRecoveryServicesAsrVMNicConfig** wird ein ASR-NIC-Konfigurationsobjekt erstellt, das die Details zum Failover und zum Testen des Failovers enthält.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="a5cb9-107">Wenn keine Informationen übergeben werden, werden die entsprechenden Werte aus dem geschützten Replikat Element ausgewählt, um zu vermeiden, dass diese Werte auf NULL aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="a5cb9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5cb9-108">EXAMPLES</span></span>

### <span data-ttu-id="a5cb9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5cb9-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="a5cb9-110">Erstellt ein ASRVmNicConfig-Objekt mit den für die NIC konfigurierten Failover-und Test-faiover-Netzwerkeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="a5cb9-111">Eine Eigenschaft, die nicht überschritten wird, wird aus dem übergebenen geschützten Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="a5cb9-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5cb9-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="a5cb9-113">Erstellt ein ASRVmNicConfig-Objekt mit den Test-faiover-Netzwerkeinstellungen, die für die NIC-Umbenennung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="a5cb9-114">Eine Eigenschaft, die nicht überschritten wird, wird aus dem übergebenen geschützten Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="a5cb9-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a5cb9-115">Example 3</span></span>

<span data-ttu-id="a5cb9-116">Erstellt eine ASR-NIC-Konfiguration, die die Konfigurationsdetails Failover und Test für Failover enthält.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="a5cb9-117">automatisch</span><span class="sxs-lookup"><span data-stu-id="a5cb9-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="a5cb9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5cb9-118">PARAMETERS</span></span>

### <span data-ttu-id="a5cb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cb9-119">-DefaultProfile</span></span>
<span data-ttu-id="a5cb9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5cb9-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="a5cb9-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="a5cb9-122">Gibt an, ob das beschleunigte Netzwerk auf der Wiederherstellungs-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="a5cb9-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="a5cb9-124">Gibt an, ob das beschleunigte Netzwerk auf der Test-Failover-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="a5cb9-125">-Nicid</span><span class="sxs-lookup"><span data-stu-id="a5cb9-125">-NicId</span></span>
<span data-ttu-id="a5cb9-126">Geben Sie die GUID der ASR-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="a5cb9-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="a5cb9-128">Gibt die IDs von Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="a5cb9-130">Gibt die ID der NSG an, die der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-131">-RecoveryNicName</span></span>
<span data-ttu-id="a5cb9-132">Gibt den Namen der Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="a5cb9-134">Gibt den Namen der Wiederherstellungs-NIC-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="a5cb9-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5cb9-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a5cb9-136">Gibt die IP-Adresse der Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="a5cb9-138">Gibt die ID der öffentlichen IP-Adresse an, die der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="a5cb9-140">Gibt die ID des virtuellen wiederherstellungsnetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="a5cb9-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="a5cb9-142">Gibt den Namen des Wiederherstellungs-Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="a5cb9-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a5cb9-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a5cb9-144">Geben Sie das geschützte ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="a5cb9-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a5cb9-145">-ReuseExistingNic</span></span>
<span data-ttu-id="a5cb9-146">Gibt an, ob eine vorhandene NIC während eines Failovers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="a5cb9-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="a5cb9-148">Gibt die IDs von Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a5cb9-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="a5cb9-150">Gibt die ID der NSG an, die der Test-Failover-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a5cb9-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-151">-TfoNicName</span></span>
<span data-ttu-id="a5cb9-152">Gibt den Namen der Test-Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="a5cb9-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="a5cb9-154">Gibt den Namen der Failover-NIC-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="a5cb9-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5cb9-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="a5cb9-156">Gibt die IP-Adresse der Test-Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="a5cb9-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="a5cb9-158">Gibt die ID der öffentlichen IP-Adresse an, die mit der Test-Failover-NIC verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a5cb9-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a5cb9-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="a5cb9-160">Gibt an, ob eine vorhandene NIC während des Test Failovers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="a5cb9-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a5cb9-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="a5cb9-162">Gibt die ID des virtuellen testfailover-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="a5cb9-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a5cb9-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="a5cb9-164">Gibt den Namen des Test-Failover-Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="a5cb9-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5cb9-165">-Confirm</span></span>
<span data-ttu-id="a5cb9-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cb9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cb9-167">-WhatIf</span></span>
<span data-ttu-id="a5cb9-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5cb9-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cb9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cb9-170">CommonParameters</span></span>
<span data-ttu-id="a5cb9-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cb9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cb9-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5cb9-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cb9-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5cb9-173">INPUTS</span></span>

### <span data-ttu-id="a5cb9-174">Keine</span><span class="sxs-lookup"><span data-stu-id="a5cb9-174">None</span></span>

## <span data-ttu-id="a5cb9-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5cb9-175">OUTPUTS</span></span>

### <span data-ttu-id="a5cb9-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a5cb9-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="a5cb9-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5cb9-177">NOTES</span></span>

## <span data-ttu-id="a5cb9-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5cb9-178">RELATED LINKS</span></span>
