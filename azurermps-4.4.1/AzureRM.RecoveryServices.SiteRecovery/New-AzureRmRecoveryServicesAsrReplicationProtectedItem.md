---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481689"
---
# <span data-ttu-id="44f4c-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="44f4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="44f4c-103">Aktiviert die Replikation für ein ASR-geschütztes Element, indem ein geschütztes Replikat Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44f4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44f4c-104">SYNTAX</span></span>

### <span data-ttu-id="44f4c-105">Disabled (Standard)</span><span class="sxs-lookup"><span data-stu-id="44f4c-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44f4c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="44f4c-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44f4c-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="44f4c-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f4c-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="44f4c-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44f4c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44f4c-109">DESCRIPTION</span></span>
<span data-ttu-id="44f4c-110">Mit dem Cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** wird ein neues geschütztes Replikat Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="44f4c-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="44f4c-111">Verwenden Sie dieses Cmdlet, um die Replikation für ein ASR-geschütztes Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="44f4c-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="44f4c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44f4c-112">EXAMPLES</span></span>

### <span data-ttu-id="44f4c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44f4c-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="44f4c-114">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="44f4c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="44f4c-115">PARAMETERS</span></span>

### <span data-ttu-id="44f4c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="44f4c-116">-Name</span></span>
<span data-ttu-id="44f4c-117">Gibt einen Namen für das geschützte ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="44f4c-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-118">-OS</span><span class="sxs-lookup"><span data-stu-id="44f4c-118">-OS</span></span>
<span data-ttu-id="44f4c-119">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="44f4c-119">Specifies the operating system family.</span></span>
<span data-ttu-id="44f4c-120">Die akzeptablen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="44f4c-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="44f4c-121">-OSDiskName</span></span>
<span data-ttu-id="44f4c-122">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="44f4c-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-123">-ProtectableItem</span></span>
<span data-ttu-id="44f4c-124">Gibt das zu schützende ASR-Element Objekt an, für das die Replikation aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="44f4c-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="44f4c-126">Gibt das Container Zuordnungsobjekt für ASR-Schutz an, das der für die Replikation zu verwendenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="44f4c-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="44f4c-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="44f4c-128">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44f4c-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="44f4c-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="44f4c-130">Gibt den Arm-Bezeichner der Ressourcengruppe an, in der der virtuelle Computer im Fall eines Failovers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f4c-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="44f4c-131">-WaitForCompletion</span></span>
<span data-ttu-id="44f4c-132">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs warten soll, bevor er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="44f4c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44f4c-133">-Confirm</span></span>
<span data-ttu-id="44f4c-134">Fordert zur Bestätigung auf, bevor der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-134">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="44f4c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f4c-135">-WhatIf</span></span>
<span data-ttu-id="44f4c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44f4c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44f4c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44f4c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44f4c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f4c-138">CommonParameters</span></span>
<span data-ttu-id="44f4c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f4c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f4c-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f4c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f4c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44f4c-141">INPUTS</span></span>

### <span data-ttu-id="44f4c-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="44f4c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44f4c-143">OUTPUTS</span></span>

### <span data-ttu-id="44f4c-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="44f4c-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="44f4c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="44f4c-145">NOTES</span></span>

## <span data-ttu-id="44f4c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44f4c-146">RELATED LINKS</span></span>

[<span data-ttu-id="44f4c-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="44f4c-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="44f4c-149">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="44f4c-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
