---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664740"
---
# <span data-ttu-id="c7706-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c7706-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="c7706-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7706-102">SYNOPSIS</span></span>
<span data-ttu-id="c7706-103">Ruft die Elemente aus einem Container in Backup ab.</span><span class="sxs-lookup"><span data-stu-id="c7706-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7706-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7706-104">SYNTAX</span></span>

### <span data-ttu-id="c7706-105">GetItemsForContainer (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7706-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7706-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="c7706-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7706-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7706-107">DESCRIPTION</span></span>
<span data-ttu-id="c7706-108">Mit dem Cmdlet **Get-AzureRmRecoveryServicesBackupItem werden** die Elemente in einem Container oder ein Wert in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c7706-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="c7706-109">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="c7706-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="c7706-110">Für Azure Virtual Machines kann nur ein Sicherungselement im Container für virtuelle Maschinen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c7706-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="c7706-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7706-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c7706-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7706-112">EXAMPLES</span></span>

### <span data-ttu-id="c7706-113">Beispiel 1: Abrufen eines Elements aus einem Sicherungs Container</span><span class="sxs-lookup"><span data-stu-id="c7706-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="c7706-114">Der erste Befehl ruft den Container vom Typ AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7706-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="c7706-115">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM in $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7706-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="c7706-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7706-116">PARAMETERS</span></span>

### <span data-ttu-id="c7706-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c7706-117">-BackupManagementType</span></span>
<span data-ttu-id="c7706-118">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="c7706-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="c7706-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7706-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7706-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c7706-120">AzureVM</span></span> 
- <span data-ttu-id="c7706-121">Mars</span><span class="sxs-lookup"><span data-stu-id="c7706-121">MARS</span></span> 
- <span data-ttu-id="c7706-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="c7706-122">SCDPM</span></span> 
- <span data-ttu-id="c7706-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="c7706-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-124">-Container</span><span class="sxs-lookup"><span data-stu-id="c7706-124">-Container</span></span>
<span data-ttu-id="c7706-125">Gibt ein Containerobjekt an, aus dem dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="c7706-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="c7706-126">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupContainer** das Get-AzureRmRecoveryServicesBackupContainer-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7706-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c7706-127">-Name</span></span>
<span data-ttu-id="c7706-128">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="c7706-128">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="c7706-129">-ProtectionState</span></span>
<span data-ttu-id="c7706-130">Gibt den Schutzstatus an.</span><span class="sxs-lookup"><span data-stu-id="c7706-130">Specifies the state of protection.</span></span>
<span data-ttu-id="c7706-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7706-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7706-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="c7706-132">IRPending.</span></span>
<span data-ttu-id="c7706-133">Die Erstsynchronisierung wurde nicht gestartet, und es gibt noch keinen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="c7706-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="c7706-134">Geschützten.</span><span class="sxs-lookup"><span data-stu-id="c7706-134">Protected.</span></span>
<span data-ttu-id="c7706-135">Der Schutz läuft.</span><span class="sxs-lookup"><span data-stu-id="c7706-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="c7706-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="c7706-136">ProtectionError.</span></span>
<span data-ttu-id="c7706-137">Es liegt ein Schutz Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="c7706-137">There is a protection error.</span></span>
- <span data-ttu-id="c7706-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="c7706-138">ProtectionStopped.</span></span>
<span data-ttu-id="c7706-139">Der Schutz ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7706-139">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="c7706-140">-ProtectionStatus</span></span>
<span data-ttu-id="c7706-141">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="c7706-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="c7706-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7706-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7706-143">Gesunde</span><span class="sxs-lookup"><span data-stu-id="c7706-143">Healthy</span></span>
- <span data-ttu-id="c7706-144">Ungesunde</span><span class="sxs-lookup"><span data-stu-id="c7706-144">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-145">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="c7706-145">-WorkloadType</span></span>
<span data-ttu-id="c7706-146">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="c7706-146">Specifies the workload type.</span></span> <span data-ttu-id="c7706-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7706-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7706-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c7706-148">AzureVM</span></span> 
- <span data-ttu-id="c7706-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c7706-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7706-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7706-150">-DefaultProfile</span></span>
<span data-ttu-id="c7706-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7706-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7706-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7706-152">CommonParameters</span></span>
<span data-ttu-id="c7706-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7706-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7706-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7706-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7706-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7706-155">INPUTS</span></span>

## <span data-ttu-id="c7706-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7706-156">OUTPUTS</span></span>

### <span data-ttu-id="c7706-157">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="c7706-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="c7706-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="c7706-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="c7706-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7706-159">NOTES</span></span>

## <span data-ttu-id="c7706-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7706-160">RELATED LINKS</span></span>

[<span data-ttu-id="c7706-161">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c7706-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="c7706-162">Deaktivieren-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c7706-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c7706-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c7706-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="c7706-164">Wiederherstellen – AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c7706-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


