---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003737"
---
# <span data-ttu-id="76d49-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="76d49-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="76d49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76d49-102">SYNOPSIS</span></span>
<span data-ttu-id="76d49-103">Legt Wiederherstellungseigenschaften wie das Zielnetzwerk und die Größe des virtuellen Computers für das angegebene Replikations geschützte Element fest.</span><span class="sxs-lookup"><span data-stu-id="76d49-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="76d49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d49-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76d49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76d49-105">DESCRIPTION</span></span>
<span data-ttu-id="76d49-106">Das Cmdlet " **Set-AzRecoveryServicesAsrReplicationProtectedItem** " legt die Wiederherstellungseigenschaften für ein geschütztes Replikations Element fest.</span><span class="sxs-lookup"><span data-stu-id="76d49-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="76d49-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76d49-107">EXAMPLES</span></span>

### <span data-ttu-id="76d49-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76d49-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="76d49-109">Startet den Vorgang des Aktualisierens der Einstellungen für die Replikations geschützten Elemente unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="76d49-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76d49-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="76d49-111">Startet den Vorgang des Aktualisierens der Netzwerkschnittstellenkarten-Einstellungen (NIC Reduction) des Replikations geschützten Elements mithilfe der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="76d49-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="76d49-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="76d49-113">Startet den Vorgang des Aktualisierens der primären NIC für die Replikations geschützten Elemente (für die Verwendung für wiederhergestellte VM-Einstellungen) unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="76d49-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="76d49-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="76d49-115">Startet den Vorgang des Aktualisierens der NIC (für wiederhergestellte VM-Einstellungen) mithilfe der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="76d49-116">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="76d49-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="76d49-117">Startet den Vorgang des Aktualisierens des Replikations geschützten Elements ausgewählte NOC TP ermöglichen eine beschleunigte Netzwerkwiederherstellung auf VM (für Azure to Azure Disaster Recovery).</span><span class="sxs-lookup"><span data-stu-id="76d49-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="76d49-118">Don t Pass-EnableAcceleratedNetworkingOnRecovery, um das beschleunigte Netzwerk zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="76d49-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="76d49-119">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="76d49-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="76d49-120">Starten Sie den Aktualisierungsvorgang für das angegebene verschlüsselte Replikat geschütztes Element, um die angegebenen Verschlüsselungsdetails für Failover-VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="76d49-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="76d49-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d49-121">PARAMETERS</span></span>

### <span data-ttu-id="76d49-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="76d49-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="76d49-123">Gibt die Konfigurationsdetails des Test Failovers und der Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="76d49-123">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="76d49-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="76d49-125">Gibt die Datenträgerkonfiguration für UDPATED für verwaltete Datenträger VM an (Azure to Azure Dr scenrio).</span><span class="sxs-lookup"><span data-stu-id="76d49-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d49-126">-DefaultProfile</span></span>
<span data-ttu-id="76d49-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76d49-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="76d49-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="76d49-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="76d49-129">Gibt die geheim-URL der Datenträgerverschlüsselung mit der Version (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="76d49-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="76d49-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="76d49-131">Gibt den geheimen Schlüssel für die Datenträgerverschlüsselung an (Azure Disk Encryption), der als Wiederherstellungs-VM nach einem Failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="76d49-132">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="76d49-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="76d49-133">Das Wörterbuch der Datenträger-Ressourcen-ID, um die Datenträgerverschlüsselung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="76d49-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="76d49-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="76d49-135">Gibt die angegebene NIC auf der Wiederherstellungs-VM an, nachdem das Failover das beschleunigte Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="76d49-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="76d49-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76d49-136">-InputObject</span></span>
<span data-ttu-id="76d49-137">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikations geschützten Elemente, das dem zu Aktualisier geschützten Replikations Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="76d49-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="76d49-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="76d49-139">Gibt die URL-Version des Datenträger Verschlüsselungsschlüssels (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="76d49-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="76d49-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="76d49-141">Gibt den Datenträgerverschlüsselungsschlüssel keyvault-ID (Azure Disk Encryption) an, der als Wiederherstellungs-VM nach einem Failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="76d49-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="76d49-142">-LicenseType</span></span>
<span data-ttu-id="76d49-143">Geben Sie die Lizenztyp Auswahl an, die für virtuelle Windows Server-Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="76d49-144">Wenn Sie berechtigt sind, den Azure Hybrid use Benefit (Hub) für Migrationen zu verwenden, und angeben möchten, dass die Hub-Einstellung bei einem Failover dieses geschützten Elements verwendet werden soll, legen Sie den Lizenztyp auf "Windows Server" fest.</span><span class="sxs-lookup"><span data-stu-id="76d49-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-145">-Name</span><span class="sxs-lookup"><span data-stu-id="76d49-145">-Name</span></span>
<span data-ttu-id="76d49-146">Gibt den Namen des virtuellen Wiederherstellungs Computers an, der beim Failover erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="76d49-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="76d49-147">-NicSelectionType</span></span>
<span data-ttu-id="76d49-148">Gibt die Netzwerkschnittstellenkarten Eigenschaften (NIC) an, die standardmäßig vom Benutzer festgelegt oder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="76d49-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="76d49-149">Sie können NotSelected angeben, um zu den Standardwerten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="76d49-149">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-150">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="76d49-150">-PrimaryNic</span></span>
<span data-ttu-id="76d49-151">Gibt die NIC an, die nach dem Failover als primäre NIC für recvcovery VM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="76d49-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76d49-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="76d49-153">Verfüg barkeits Satz für Replikations geschütztes Element nach einem Failover</span><span class="sxs-lookup"><span data-stu-id="76d49-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="76d49-154">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="76d49-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="76d49-155">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="76d49-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="76d49-156">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="76d49-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="76d49-157">Die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts, auf den dieser virtuelle Computer Failover durch ein Failover durch.</span><span class="sxs-lookup"><span data-stu-id="76d49-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="76d49-158">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="76d49-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="76d49-159">Gibt die Ziel-Back-End-Adresspools an, die der Wiederherstellungs-NIC zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76d49-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="76d49-160">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="76d49-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="76d49-161">Gibt die ID des virtuellen Azure-Netzwerks an, für das ein Failover des geschützten Elements durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="76d49-162">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="76d49-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="76d49-163">Gibt die ID der Netzwerksicherheitsgruppe an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="76d49-164">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="76d49-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="76d49-165">Gibt die statische IP-Adresse an, die der primären NIC bei der Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="76d49-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="76d49-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="76d49-167">Gibt den Namen des Subnets im virtuellen Recovery Azure-Netzwerk an, mit dem diese NIC des geschützten Elements beim Failover verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="76d49-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="76d49-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="76d49-169">Gibt die ID der öffentlichen IP-Adressen Ressource an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="76d49-170">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="76d49-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="76d49-171">Die ID der Azure-Ressourcengruppe im Wiederherstellungsbereich, in der das geschützte Element beim Failover wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="76d49-172">-Size</span><span class="sxs-lookup"><span data-stu-id="76d49-172">-Size</span></span>
<span data-ttu-id="76d49-173">Gibt die Größe der virtuellen Wiederherstellungs Maschine an.</span><span class="sxs-lookup"><span data-stu-id="76d49-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="76d49-174">Der Wert sollte aus den von Azure Virtual Machines unterstützten Größen Sätzen sein.</span><span class="sxs-lookup"><span data-stu-id="76d49-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="76d49-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="76d49-175">-TfoAzureVMName</span></span>
<span data-ttu-id="76d49-176">Gibt den Namen des Test-Failover-VM an.</span><span class="sxs-lookup"><span data-stu-id="76d49-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="76d49-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="76d49-177">-UpdateNic</span></span>
<span data-ttu-id="76d49-178">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Wiederherstellungs Netzwerk Eigenschaft für UDPATED festlegt.</span><span class="sxs-lookup"><span data-stu-id="76d49-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="76d49-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="76d49-179">-UseManagedDisk</span></span>
<span data-ttu-id="76d49-180">Gibt an, ob der beim Failover erstellte Azure Virtual Machine verwaltete Datenträger verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="76d49-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d49-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76d49-181">-Confirm</span></span>
<span data-ttu-id="76d49-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76d49-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d49-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d49-183">-WhatIf</span></span>
<span data-ttu-id="76d49-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76d49-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76d49-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76d49-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d49-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d49-186">CommonParameters</span></span>
<span data-ttu-id="76d49-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d49-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d49-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76d49-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d49-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76d49-189">INPUTS</span></span>

### <span data-ttu-id="76d49-190">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="76d49-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="76d49-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76d49-191">OUTPUTS</span></span>

### <span data-ttu-id="76d49-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="76d49-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="76d49-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="76d49-193">NOTES</span></span>

## <span data-ttu-id="76d49-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76d49-194">RELATED LINKS</span></span>

[<span data-ttu-id="76d49-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="76d49-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="76d49-196">Neu – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="76d49-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="76d49-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="76d49-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
