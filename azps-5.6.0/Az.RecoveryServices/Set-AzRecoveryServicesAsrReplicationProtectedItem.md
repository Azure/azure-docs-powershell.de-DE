---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ad3f2c07d358819917706253df05bfd899c3b53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942280"
---
# <span data-ttu-id="a44e5-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a44e5-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="a44e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a44e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a44e5-103">Legt Wiederherstellungseigenschaften wie Zielnetzwerk und Größe virtueller Computer für das angegebene replikationsgeschützte Element fest.</span><span class="sxs-lookup"><span data-stu-id="a44e5-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="a44e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a44e5-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
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

## <span data-ttu-id="a44e5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a44e5-105">DESCRIPTION</span></span>
<span data-ttu-id="a44e5-106">Das **Cmdlet Set-AzRecoveryServicesAsrReplicationProtectedItem** legt die Wiederherstellungseigenschaften für ein replikationsgeschütztes Element fest.</span><span class="sxs-lookup"><span data-stu-id="a44e5-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="a44e5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a44e5-107">EXAMPLES</span></span>

### <span data-ttu-id="a44e5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a44e5-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="a44e5-109">Startet den Vorgang zum Aktualisieren der replikationsgeschützten Elementeinstellungen mithilfe der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a44e5-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a44e5-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a44e5-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="a44e5-111">Startet den Vorgang zum Aktualisieren der Einstellungen für die netzwerkschnittstellengeschützte Netzwerkschnittstellenkarte (NIC Reduction) mithilfe der angegebenen Parameter und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="a44e5-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a44e5-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a44e5-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="a44e5-113">Startet den Vorgang zum Aktualisieren der primären NIC für replikationsgeschützte Elemente (zur Verwendung für wiederhergestellte vm )-Einstellungen mithilfe der angegebenen Parameter und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="a44e5-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a44e5-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a44e5-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="a44e5-115">Startet den Vorgang zum Aktualisieren der replikationsgeschützten Element-NIC (zur Verwendung für wiederhergestellte vm )-Einstellungen mithilfe der angegebenen Parameter und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="a44e5-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a44e5-116">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="a44e5-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="a44e5-117">Startet den Vorgang zum Aktualisieren des replikationsgeschützten Elements ausgewählt noc tp aktivieren beschleunigtes Netzwerk auf der Wiederherstellungs-VM (für Azure zu Azure Disaster Recovery).</span><span class="sxs-lookup"><span data-stu-id="a44e5-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="a44e5-118">Übergeben Sie -EnableAcceleratedNetworkingOnRecovery nicht, um das beschleunigte Netzwerk zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a44e5-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="a44e5-119">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="a44e5-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="a44e5-120">Starten Sie den Aktualisierungsvorgang für das angegebene verschlüsselte replikationsgeschützte Element, um die angegebenen Verschlüsselungsdetails für die Failover-VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a44e5-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="a44e5-121">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="a44e5-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="a44e5-122">Starten Sie den Aktualisierungsvorgang für das angegebene replikationsgeschützte Element, um die angegebene Näherungsplatzierungsgruppe für die Failover-VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a44e5-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="a44e5-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a44e5-123">PARAMETERS</span></span>

### <span data-ttu-id="a44e5-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="a44e5-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="a44e5-125">Gibt die Konfigurationsdetails der Test-Failover- und Failover-NIC an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="a44e5-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a44e5-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="a44e5-127">Gibt die Datenträgerkonfiguration an, die für verwaltete Datenträger vm (Azure zu Azure DR scenrio) udpated werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="a44e5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44e5-128">-DefaultProfile</span></span>
<span data-ttu-id="a44e5-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a44e5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a44e5-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="a44e5-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="a44e5-131">Gibt die geheime URL der Datenträgerverschlüsselung mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="a44e5-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a44e5-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="a44e5-133">Gibt die Geheimschlüssel-Tresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="a44e5-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="a44e5-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="a44e5-135">Das Wörterbuch der Datenträgerressourcen-ID zum Datenträgerverschlüsselungssatz ARM ID.</span><span class="sxs-lookup"><span data-stu-id="a44e5-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="a44e5-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="a44e5-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="a44e5-137">Gibt die angegebene NIC auf der Wiederherstellungs-VM an, nachdem ein Failover beschleunigtes Netzwerk verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="a44e5-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="a44e5-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a44e5-138">-InputObject</span></span>
<span data-ttu-id="a44e5-139">Das Eingabeobjekt für das Cmdlet: Das asr-replikationsgeschützte Elementobjekt, das dem zu aktualisierende replikationsgeschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="a44e5-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="a44e5-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a44e5-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a44e5-141">Gibt die URL-Version des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="a44e5-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a44e5-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="a44e5-143">Gibt den Datenträgerverschlüsselungsschlüssel keyVault ID(Azure Disk Encryption) an, der nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="a44e5-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a44e5-144">-LicenseType</span></span>
<span data-ttu-id="a44e5-145">Geben Sie die Lizenztypauswahl an, die für virtuelle Windows Server-Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="a44e5-146">Wenn Sie berechtigt sind, den Azure Hybrid Use Benefit (HUB) für Migrationen zu verwenden, und angeben möchten, dass die HUB-Einstellung verwendet wird, während ein Fehler bei diesem geschützten Element vor sich geht, legen Sie den Lizenztyp auf WindowsServer fest.</span><span class="sxs-lookup"><span data-stu-id="a44e5-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="a44e5-147">-Name</span><span class="sxs-lookup"><span data-stu-id="a44e5-147">-Name</span></span>
<span data-ttu-id="a44e5-148">Gibt den Namen des virtuellen Wiederherstellungscomputers an, der beim Failover erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a44e5-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="a44e5-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="a44e5-149">-NicSelectionType</span></span>
<span data-ttu-id="a44e5-150">Gibt die vom Benutzer festgelegten oder standardmäßig festgelegten Eigenschaften der Netzwerkschnittstellenkarte (NIC) an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="a44e5-151">Sie können NotSelected angeben, um zu den Standardwerten zurück zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a44e5-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="a44e5-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="a44e5-152">-PrimaryNic</span></span>
<span data-ttu-id="a44e5-153">Gibt die NIC an, die nach dem Failover als primäre NIC für die recvcovery-VM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a44e5-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="a44e5-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a44e5-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="a44e5-155">Verfügbarkeitssatz für das replikationsgeschützte Element nach dem Failover.</span><span class="sxs-lookup"><span data-stu-id="a44e5-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="a44e5-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="a44e5-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="a44e5-157">Gibt die Verfügbarkeitszone für das replikationsgeschützte Element nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="a44e5-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a44e5-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="a44e5-159">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung von azure VM an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="a44e5-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="a44e5-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="a44e5-161">Die Ressourcen-ID des Wiederherstellungs-Clouddiensts, auf den dieser virtuelle Computer failovern soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="a44e5-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a44e5-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="a44e5-163">Gibt die Ziel-Back-End-Adresspools an, die der Wiederherstellungs-NIC zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a44e5-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="a44e5-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="a44e5-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="a44e5-165">Gibt die ID des virtuellen Azure-Netzwerks an, für das das geschützte Element fehlgeschlagen sein soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="a44e5-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a44e5-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="a44e5-167">Gibt die ID der Netzwerksicherheitsgruppe an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="a44e5-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a44e5-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a44e5-169">Gibt die statische IP-Adresse an, die der primären NIC bei der Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="a44e5-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="a44e5-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="a44e5-171">Gibt den Namen des Subnetzes im virtuellen Azure-Wiederherstellungsnetzwerk an, mit dem diese NIC des geschützten Elements bei einem Failover verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="a44e5-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a44e5-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="a44e5-173">Gibt die Ressourcen-ID der Platzierungsgruppe für die Wiederherstellungsnäherung an, auf die der virtuelle Computer failovern soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="a44e5-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a44e5-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="a44e5-175">Gibt die ID der öffentlichen IP-Adressressource an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="a44e5-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a44e5-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a44e5-177">Die ID der Azure-Ressourcengruppe im Wiederherstellungsbereich, in dem das geschützte Element beim Failover wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a44e5-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="a44e5-178">-Size</span><span class="sxs-lookup"><span data-stu-id="a44e5-178">-Size</span></span>
<span data-ttu-id="a44e5-179">Gibt die Größe des virtuellen Wiederherstellungscomputers an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="a44e5-180">Der Wert sollte aus der Gruppe von Größen kommen, die von virtuellen Azure-Computern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a44e5-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="a44e5-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="a44e5-181">-TfoAzureVMName</span></span>
<span data-ttu-id="a44e5-182">Gibt den Namen der Test-Failover-VM an.</span><span class="sxs-lookup"><span data-stu-id="a44e5-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="a44e5-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="a44e5-183">-UpdateNic</span></span>
<span data-ttu-id="a44e5-184">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet festgelegt hat, dass die Wiederherstellungsnetzwerkeigenschaft udpated sein muss.</span><span class="sxs-lookup"><span data-stu-id="a44e5-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="a44e5-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a44e5-185">-UseManagedDisk</span></span>
<span data-ttu-id="a44e5-186">Gibt an, ob der virtuelle Azure-Computer, der beim Failover erstellt wird, verwaltete Datenträger verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a44e5-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="a44e5-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a44e5-187">-Confirm</span></span>
<span data-ttu-id="a44e5-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a44e5-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a44e5-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a44e5-189">-WhatIf</span></span>
<span data-ttu-id="a44e5-190">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a44e5-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a44e5-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a44e5-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a44e5-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44e5-192">CommonParameters</span></span>
<span data-ttu-id="a44e5-193">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44e5-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44e5-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a44e5-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44e5-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a44e5-195">INPUTS</span></span>

### <span data-ttu-id="a44e5-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a44e5-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a44e5-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a44e5-197">OUTPUTS</span></span>

### <span data-ttu-id="a44e5-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a44e5-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a44e5-199">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a44e5-199">NOTES</span></span>

## <span data-ttu-id="a44e5-200">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a44e5-200">RELATED LINKS</span></span>

[<span data-ttu-id="a44e5-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a44e5-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a44e5-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a44e5-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a44e5-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a44e5-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
