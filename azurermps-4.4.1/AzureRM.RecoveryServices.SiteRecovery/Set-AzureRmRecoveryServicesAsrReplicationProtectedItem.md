---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663859"
---
# <span data-ttu-id="f220a-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f220a-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f220a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f220a-102">SYNOPSIS</span></span>
<span data-ttu-id="f220a-103">Legt Wiederherstellungseigenschaften wie das Zielnetzwerk und die Größe des virtuellen Computers für das angegebene Replikations geschützte Element fest.</span><span class="sxs-lookup"><span data-stu-id="f220a-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f220a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f220a-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f220a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f220a-105">DESCRIPTION</span></span>
<span data-ttu-id="f220a-106">Das Cmdlet " **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** " legt die Wiederherstellungseigenschaften für ein geschütztes Replikations Element fest.</span><span class="sxs-lookup"><span data-stu-id="f220a-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="f220a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f220a-107">EXAMPLES</span></span>

### <span data-ttu-id="f220a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f220a-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="f220a-109">Startet den Vorgang des Aktualisierens der Replikations Elementeinstellungen mithilfe der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f220a-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f220a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f220a-110">PARAMETERS</span></span>

### <span data-ttu-id="f220a-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f220a-111">-InputObject</span></span>
<span data-ttu-id="f220a-112">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikations geschützten Elemente, das dem zu Aktualisier geschützten Replikations Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="f220a-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f220a-113">-LicenseType</span></span>
<span data-ttu-id="f220a-114">Geben Sie die Lizenztyp Auswahl an, die für virtuelle Windows Server-Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f220a-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="f220a-115">Wenn Sie berechtigt sind, den Azure Hybrid use Benefit (Hub) für Migrationen zu verwenden, und angeben möchten, dass die Hub-Einstellung bei einem Failover dieses geschützten Elements verwendet werden soll, legen Sie den Lizenztyp auf "Windows Server" fest.</span><span class="sxs-lookup"><span data-stu-id="f220a-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f220a-116">-Name</span></span>
<span data-ttu-id="f220a-117">Gibt den Namen des virtuellen Wiederherstellungs Computers an, der beim Failover erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f220a-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="f220a-118">-NicSelectionType</span></span>
<span data-ttu-id="f220a-119">Gibt die Netzwerkschnittstellenkarten Eigenschaften (NIC) an, die standardmäßig vom Benutzer festgelegt oder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f220a-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="f220a-120">Sie können NotSelected angeben, um zu den Standardwerten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f220a-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="f220a-121">-PrimaryNic</span></span>
<span data-ttu-id="f220a-122">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Wiederherstellungs Netzwerk Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="f220a-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="f220a-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="f220a-124">Gibt die ID des virtuellen Azure-Netzwerks an, für das ein Failover des geschützten Elements durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f220a-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="f220a-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="f220a-126">Gibt die statische IP-Adresse an, die der primären NIC bei der Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f220a-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="f220a-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="f220a-128">Gibt den Namen des Subnets im virtuellen Recovery Azure-Netzwerk an, mit dem diese NIC des geschützten Elements beim Failover verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="f220a-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f220a-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f220a-130">Die ID der Azure-Ressourcengruppe im Wiederherstellungsbereich, in der das geschützte Element beim Failover wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f220a-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-131">-Size</span><span class="sxs-lookup"><span data-stu-id="f220a-131">-Size</span></span>
<span data-ttu-id="f220a-132">Gibt die Größe der virtuellen Wiederherstellungs Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f220a-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="f220a-133">Der Wert sollte aus den von Azure Virtual Machines unterstützten Größen Sätzen sein.</span><span class="sxs-lookup"><span data-stu-id="f220a-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f220a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f220a-134">-Confirm</span></span>
<span data-ttu-id="f220a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f220a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f220a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f220a-136">-WhatIf</span></span>
<span data-ttu-id="f220a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f220a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f220a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f220a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f220a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f220a-139">CommonParameters</span></span>
<span data-ttu-id="f220a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f220a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f220a-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f220a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f220a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f220a-142">INPUTS</span></span>

### <span data-ttu-id="f220a-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f220a-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f220a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f220a-144">OUTPUTS</span></span>

### <span data-ttu-id="f220a-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f220a-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f220a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f220a-146">NOTES</span></span>

## <span data-ttu-id="f220a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f220a-147">RELATED LINKS</span></span>

[<span data-ttu-id="f220a-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f220a-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f220a-149">Neu – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f220a-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f220a-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f220a-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
