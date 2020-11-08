---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997388"
---
# <span data-ttu-id="9a755-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="9a755-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="9a755-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a755-102">SYNOPSIS</span></span>
<span data-ttu-id="9a755-103">Erstellt eine ASR-NIC-Konfiguration, die die Konfigurationsdetails Failover und Test für Failover enthält.</span><span class="sxs-lookup"><span data-stu-id="9a755-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="9a755-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a755-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a755-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a755-105">DESCRIPTION</span></span>
<span data-ttu-id="9a755-106">Mit dem Cmdlet **New-AzRecoveryServicesAsrVMNicConfig** wird ein ASR-NIC-Konfigurationsobjekt erstellt, das die Details zum Failover und zum Testen des Failovers enthält.</span><span class="sxs-lookup"><span data-stu-id="9a755-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="9a755-107">Wenn keine Informationen übergeben werden, werden die entsprechenden Werte aus dem geschützten Replikat Element ausgewählt, um zu vermeiden, dass diese Werte auf NULL aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a755-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="9a755-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a755-108">EXAMPLES</span></span>

### <span data-ttu-id="9a755-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a755-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="9a755-110">Erstellt ein ASRVmNicConfig-Objekt mit den für die NIC konfigurierten Failover-und Test-faiover-Netzwerkeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9a755-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="9a755-111">Eine Eigenschaft, die nicht überschritten wird, wird aus dem übergebenen geschützten Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9a755-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="9a755-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a755-112">PARAMETERS</span></span>

### <span data-ttu-id="9a755-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a755-113">-DefaultProfile</span></span>
<span data-ttu-id="9a755-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a755-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a755-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="9a755-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="9a755-116">Gibt an, ob das beschleunigte Netzwerk auf der Wiederherstellungs-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="9a755-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="9a755-118">Gibt an, ob das beschleunigte Netzwerk auf der Test-Failover-NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="9a755-119">-Nicid</span><span class="sxs-lookup"><span data-stu-id="9a755-119">-NicId</span></span>
<span data-ttu-id="9a755-120">Geben Sie die GUID der ASR-NIC an.</span><span class="sxs-lookup"><span data-stu-id="9a755-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="9a755-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a755-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="9a755-122">Gibt die IDs von Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="9a755-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9a755-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="9a755-124">Gibt die ID der NSG an, die der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a755-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="9a755-126">Gibt die IP-Adresse der Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="9a755-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9a755-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="9a755-128">Gibt die ID der öffentlichen IP-Adresse an, die der Wiederherstellungs-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9a755-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="9a755-130">Gibt die ID des virtuellen wiederherstellungsnetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="9a755-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="9a755-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="9a755-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="9a755-132">Gibt den Namen des Wiederherstellungs-Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="9a755-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="9a755-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a755-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9a755-134">Geben Sie das geschützte ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="9a755-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="9a755-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a755-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="9a755-136">Gibt die IDs von Back-End-Adresspools für die Wiederherstellungs-NIC an.</span><span class="sxs-lookup"><span data-stu-id="9a755-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="9a755-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9a755-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="9a755-138">Gibt die ID der NSG an, die der Test-Failover-NIC zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="9a755-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a755-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="9a755-140">Gibt die IP-Adresse der Test-Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="9a755-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="9a755-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9a755-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="9a755-142">Gibt die ID der öffentlichen IP-Adresse an, die mit der Test-Failover-NIC verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9a755-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="9a755-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9a755-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="9a755-144">Gibt die ID des virtuellen testfailover-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="9a755-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="9a755-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="9a755-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="9a755-146">Gibt den Namen des Test-Failover-Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="9a755-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="9a755-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a755-147">CommonParameters</span></span>
<span data-ttu-id="9a755-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a755-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a755-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a755-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a755-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a755-150">INPUTS</span></span>

### <span data-ttu-id="9a755-151">Keine</span><span class="sxs-lookup"><span data-stu-id="9a755-151">None</span></span>

## <span data-ttu-id="9a755-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a755-152">OUTPUTS</span></span>

### <span data-ttu-id="9a755-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="9a755-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="9a755-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a755-154">NOTES</span></span>

## <span data-ttu-id="9a755-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a755-155">RELATED LINKS</span></span>
