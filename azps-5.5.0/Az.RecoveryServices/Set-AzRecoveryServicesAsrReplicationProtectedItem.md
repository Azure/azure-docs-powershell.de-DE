---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 21c924d02a18ae60f07abd616809358208256039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158548"
---
# <span data-ttu-id="f99b2-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f99b2-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f99b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f99b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f99b2-103">Legt Wiederherstellungseigenschaften wie Zielnetzwerk und Größe virtueller Computer für das angegebene replikationsgeschützte Element fest.</span><span class="sxs-lookup"><span data-stu-id="f99b2-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="f99b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f99b2-104">SYNTAX</span></span>

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

## <span data-ttu-id="f99b2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f99b2-106">Das **Cmdlet "Set-AzRecoveryServicesAsrReplicationProtectedItem"** legt die Wiederherstellungseigenschaften für ein replikationsgeschütztes Element fest.</span><span class="sxs-lookup"><span data-stu-id="f99b2-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="f99b2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f99b2-107">EXAMPLES</span></span>

### <span data-ttu-id="f99b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f99b2-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="f99b2-109">Startet den Vorgang zum Aktualisieren der einstellungen für replikationsgeschützte Elemente mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f99b2-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f99b2-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="f99b2-111">Startet den Vorgang der Aktualisierung der Einstellungen für die replikationsgeschützte Netzwerkschnittstellenkarte (NIC Reduction) unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f99b2-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f99b2-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="f99b2-113">Startet den Vorgang der Aktualisierung der primären NIC (für die für wiederhergestellte vm )-Einstellungen verwendete replikationsgeschützte Element mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f99b2-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f99b2-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="f99b2-115">Startet den Vorgang der Aktualisierung der NIC für replikationsgeschützte Elemente (zur Verwendung für wiederhergestellte vm )-Einstellungen unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f99b2-116">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="f99b2-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="f99b2-117">Startet den Vorgang zum Aktualisieren des durch die Replikation geschützten Elements, für das "noc tp" ausgewählt wurde, das beschleunigte Netzwerk auf wiederherstellungs-VM(für Azure zu Azure-Notfallwiederherstellung).</span><span class="sxs-lookup"><span data-stu-id="f99b2-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="f99b2-118">Übergeben Sie "-EnableAccepharmaNetworkingOnRecovery" nicht, um beschleunigtes Netzwerk zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f99b2-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="f99b2-119">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="f99b2-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="f99b2-120">Starten Sie den Aktualisierungsvorgang für das angegebene verschlüsselte replikationsgeschützte Element, um die angegebenen Verschlüsselungsdetails für Failover-VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f99b2-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="f99b2-121">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="f99b2-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="f99b2-122">Starten Sie den Aktualisierungsvorgang für das angegebene replikationsgeschützte Element, um die bereitgestellte Näherungsplatzierungsgruppe für Failover-VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f99b2-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="f99b2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f99b2-123">PARAMETERS</span></span>

### <span data-ttu-id="f99b2-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="f99b2-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="f99b2-125">Gibt die Details der Test failover- und failover-NIC-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="f99b2-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="f99b2-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f99b2-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="f99b2-127">Gibt die Datenträgerkonfiguration an, die für verwaltete Datenträger vm (Azure zu Azure DR scenrio) udpated werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="f99b2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99b2-128">-DefaultProfile</span></span>
<span data-ttu-id="f99b2-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f99b2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f99b2-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="f99b2-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="f99b2-131">Gibt die geheime Festplattenverschlüsselungs-URL mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f99b2-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f99b2-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="f99b2-133">Gibt die Schlüsseltresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f99b2-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="f99b2-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="f99b2-135">Das Wörterbuch der Datenträgerressourcen-ID für die Datenträgerverschlüsselung, für das die ARM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f99b2-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="f99b2-136">-EnableAcce inNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="f99b2-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="f99b2-137">Gibt die angegebene NIC für die Wiederherstellungs-VM an, nachdem failoverbeschleunigtes Netzwerk verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f99b2-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="f99b2-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f99b2-138">-InputObject</span></span>
<span data-ttu-id="f99b2-139">Das Eingabeobjekt für das Cmdlet: Das asR-replikationsgeschützte Elementobjekt, das dem zu aktualisierende replikationsgeschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="f99b2-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="f99b2-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f99b2-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f99b2-141">Gibt die URL-Version des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f99b2-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f99b2-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="f99b2-143">Gibt die Schlüssel-ID des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="f99b2-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f99b2-144">-LicenseType</span></span>
<span data-ttu-id="f99b2-145">Geben Sie die Lizenztypauswahl an, die für virtuelle Windows Server-Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="f99b2-146">Wenn Sie berechtigt sind, den Azure Hybrid Use Benefit (HUB) für Migrationen zu verwenden, und angeben möchten, dass die Hubeinstellung verwendet wird, während ein Fehler bei diesem geschützten Element vor sich geht, legen Sie den Lizenztyp auf "WindowsServer" fest.</span><span class="sxs-lookup"><span data-stu-id="f99b2-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="f99b2-147">-Name</span><span class="sxs-lookup"><span data-stu-id="f99b2-147">-Name</span></span>
<span data-ttu-id="f99b2-148">Gibt den Namen des virtuellen Wiederherstellungscomputers an, der bei einem Failover erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="f99b2-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="f99b2-149">-NicSelectionType</span></span>
<span data-ttu-id="f99b2-150">Gibt die Eigenschaften der Netzwerkschnittstellenkarte (NIC) an, die von einem Benutzer oder standardmäßig festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99b2-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="f99b2-151">Sie können "NotSelected" angeben, um zu den Standardwerten zurück zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="f99b2-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="f99b2-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="f99b2-152">-PrimaryNic</span></span>
<span data-ttu-id="f99b2-153">Gibt die NIC an, die nach dem Failover als primäre NIC für recvcovery VM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="f99b2-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f99b2-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="f99b2-155">Verfügbarkeitssatz für replikationsgeschütztes Element nach dem Failover.</span><span class="sxs-lookup"><span data-stu-id="f99b2-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="f99b2-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="f99b2-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="f99b2-157">Gibt die Verfügbarkeitszone für replikationsgeschützte Elemente nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="f99b2-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="f99b2-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f99b2-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="f99b2-159">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung der Azure VM an.</span><span class="sxs-lookup"><span data-stu-id="f99b2-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="f99b2-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="f99b2-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="f99b2-161">Die Ressourcen-ID des Wiederherstellungs-Clouddiensts für den Failover dieses virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f99b2-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="f99b2-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f99b2-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="f99b2-163">Gibt die Ziel-Back-End-Adresspools an, die der Wiederherstellungs-NIC zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f99b2-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="f99b2-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="f99b2-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="f99b2-165">Gibt die ID des virtuellen Azure-Netzwerks an, für das ein Fehler beim geschützten Element ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="f99b2-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f99b2-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="f99b2-167">Gibt die ID der Netzwerksicherheitsgruppe an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="f99b2-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="f99b2-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="f99b2-169">Gibt die statische IP-Adresse an, die der primären NIC für die Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="f99b2-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="f99b2-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="f99b2-171">Gibt den Namen des Subnetzes im virtuellen Wiederherstellungsnetzwerk von Azure an, mit dem diese NIC des geschützten Elements bei einem Failover verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="f99b2-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f99b2-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="f99b2-173">Gibt die Ressourcen-ID der Näherungsplatzierungsgruppe für die Wiederherstellung an, zu der der virtuelle Computer über einen Failover führen soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="f99b2-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="f99b2-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="f99b2-175">Gibt die ID der öffentlichen IP-Adressressource an, die der Wiederherstellungs-NIC zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="f99b2-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f99b2-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f99b2-177">Die ID der Azure-Ressourcengruppe in der Wiederherstellungsregion, in der das geschützte Element bei einem Failover wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="f99b2-178">-Size</span><span class="sxs-lookup"><span data-stu-id="f99b2-178">-Size</span></span>
<span data-ttu-id="f99b2-179">Gibt die Größe des virtuellen Wiederherstellungscomputers an.</span><span class="sxs-lookup"><span data-stu-id="f99b2-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="f99b2-180">Der Wert sollte aus der Reihe von Größen kommen, die von virtuellen Computern von Azure unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f99b2-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="f99b2-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="f99b2-181">-TfoAzureVMName</span></span>
<span data-ttu-id="f99b2-182">Gibt den Namen der Test failover VM an.</span><span class="sxs-lookup"><span data-stu-id="f99b2-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="f99b2-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="f99b2-183">-UpdateNic</span></span>
<span data-ttu-id="f99b2-184">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Eigenschaft des Wiederherstellungsnetzwerks auf udpated setzt.</span><span class="sxs-lookup"><span data-stu-id="f99b2-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="f99b2-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f99b2-185">-UseManagedDisk</span></span>
<span data-ttu-id="f99b2-186">Gibt an, ob der im Failover erstellte virtuelle Azure-Computer verwaltete Datenträger verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="f99b2-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="f99b2-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f99b2-187">-Confirm</span></span>
<span data-ttu-id="f99b2-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f99b2-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99b2-189">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f99b2-189">-WhatIf</span></span>
<span data-ttu-id="f99b2-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f99b2-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f99b2-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f99b2-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99b2-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99b2-192">CommonParameters</span></span>
<span data-ttu-id="f99b2-193">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f99b2-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99b2-194">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f99b2-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99b2-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f99b2-195">INPUTS</span></span>

### <span data-ttu-id="f99b2-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f99b2-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f99b2-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f99b2-197">OUTPUTS</span></span>

### <span data-ttu-id="f99b2-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f99b2-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f99b2-199">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f99b2-199">NOTES</span></span>

## <span data-ttu-id="f99b2-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f99b2-200">RELATED LINKS</span></span>

[<span data-ttu-id="f99b2-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f99b2-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f99b2-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f99b2-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f99b2-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f99b2-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
