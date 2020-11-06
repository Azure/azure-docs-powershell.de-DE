---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480158"
---
# <span data-ttu-id="cca5d-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cca5d-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="cca5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cca5d-102">SYNOPSIS</span></span>
<span data-ttu-id="cca5d-103">Legt Wiederherstellungseigenschaften wie das Zielnetzwerk und die Größe des virtuellen Computers für das angegebene Replikations geschützte Element fest.</span><span class="sxs-lookup"><span data-stu-id="cca5d-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cca5d-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cca5d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cca5d-105">DESCRIPTION</span></span>
<span data-ttu-id="cca5d-106">Das Cmdlet " **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** " legt die Wiederherstellungseigenschaften für ein geschütztes Replikations Element fest.</span><span class="sxs-lookup"><span data-stu-id="cca5d-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="cca5d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cca5d-107">EXAMPLES</span></span>

### <span data-ttu-id="cca5d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cca5d-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="cca5d-109">Startet den Vorgang des Aktualisierens der Replikations Elementeinstellungen mithilfe der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cca5d-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cca5d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cca5d-110">PARAMETERS</span></span>

### <span data-ttu-id="cca5d-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="cca5d-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="cca5d-112">Gibt den Update-Relikt-ausgelesen an.</span><span class="sxs-lookup"><span data-stu-id="cca5d-112">Specifies the update relication configration.</span></span>

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

### <span data-ttu-id="cca5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca5d-113">-DefaultProfile</span></span>
<span data-ttu-id="cca5d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cca5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cca5d-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cca5d-115">-InputObject</span></span>
<span data-ttu-id="cca5d-116">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikations geschützten Elemente, das dem zu Aktualisier geschützten Replikations Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="cca5d-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="cca5d-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cca5d-117">-LicenseType</span></span>
<span data-ttu-id="cca5d-118">Geben Sie die Lizenztyp Auswahl an, die für virtuelle Windows Server-Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cca5d-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="cca5d-119">Wenn Sie berechtigt sind, den Azure Hybrid use Benefit (Hub) für Migrationen zu verwenden, und angeben möchten, dass die Hub-Einstellung bei einem Failover dieses geschützten Elements verwendet werden soll, legen Sie den Lizenztyp auf "Windows Server" fest.</span><span class="sxs-lookup"><span data-stu-id="cca5d-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="cca5d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cca5d-120">-Name</span></span>
<span data-ttu-id="cca5d-121">Gibt den Namen des virtuellen Wiederherstellungs Computers an, der beim Failover erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cca5d-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="cca5d-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="cca5d-122">-NicSelectionType</span></span>
<span data-ttu-id="cca5d-123">Gibt die Netzwerkschnittstellenkarten Eigenschaften (NIC) an, die standardmäßig vom Benutzer festgelegt oder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cca5d-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="cca5d-124">Sie können NotSelected angeben, um zu den Standardwerten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="cca5d-124">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="cca5d-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="cca5d-125">-PrimaryNic</span></span>
<span data-ttu-id="cca5d-126">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Wiederherstellungs Netzwerk Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="cca5d-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="cca5d-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cca5d-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="cca5d-128">Verfüg barkeits Satz für Replikations geschütztes Element nach einem Failover</span><span class="sxs-lookup"><span data-stu-id="cca5d-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="cca5d-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cca5d-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="cca5d-130">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="cca5d-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="cca5d-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="cca5d-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="cca5d-132">Die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts, auf den dieser virtuelle Computer Failover durch ein Failover durch.</span><span class="sxs-lookup"><span data-stu-id="cca5d-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="cca5d-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="cca5d-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="cca5d-134">Gibt die ID des virtuellen Azure-Netzwerks an, für das ein Failover des geschützten Elements durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cca5d-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="cca5d-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="cca5d-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="cca5d-136">Gibt die statische IP-Adresse an, die der primären NIC bei der Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cca5d-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="cca5d-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="cca5d-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="cca5d-138">Gibt den Namen des Subnets im virtuellen Recovery Azure-Netzwerk an, mit dem diese NIC des geschützten Elements beim Failover verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="cca5d-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="cca5d-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cca5d-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="cca5d-140">Die ID der Azure-Ressourcengruppe im Wiederherstellungsbereich, in der das geschützte Element beim Failover wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cca5d-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="cca5d-141">-Size</span><span class="sxs-lookup"><span data-stu-id="cca5d-141">-Size</span></span>
<span data-ttu-id="cca5d-142">Gibt die Größe der virtuellen Wiederherstellungs Maschine an.</span><span class="sxs-lookup"><span data-stu-id="cca5d-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="cca5d-143">Der Wert sollte aus den von Azure Virtual Machines unterstützten Größen Sätzen sein.</span><span class="sxs-lookup"><span data-stu-id="cca5d-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="cca5d-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="cca5d-144">-UseManagedDisk</span></span>
<span data-ttu-id="cca5d-145">Gibt an, ob der beim Failover erstellte Azure Virtual Machine verwaltete Datenträger verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="cca5d-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="cca5d-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cca5d-146">-Confirm</span></span>
<span data-ttu-id="cca5d-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cca5d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca5d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca5d-148">-WhatIf</span></span>
<span data-ttu-id="cca5d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cca5d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cca5d-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cca5d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca5d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca5d-151">CommonParameters</span></span>
<span data-ttu-id="cca5d-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca5d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca5d-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca5d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca5d-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cca5d-154">INPUTS</span></span>

### <span data-ttu-id="cca5d-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cca5d-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cca5d-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cca5d-156">OUTPUTS</span></span>

### <span data-ttu-id="cca5d-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cca5d-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cca5d-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="cca5d-158">NOTES</span></span>

## <span data-ttu-id="cca5d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cca5d-159">RELATED LINKS</span></span>

[<span data-ttu-id="cca5d-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cca5d-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cca5d-161">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cca5d-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cca5d-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cca5d-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
