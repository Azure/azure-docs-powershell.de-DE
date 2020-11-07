---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824363"
---
# <span data-ttu-id="91527-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91527-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="91527-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91527-102">SYNOPSIS</span></span>

<span data-ttu-id="91527-103">Ruft die Elemente aus einem Container in Backup ab.</span><span class="sxs-lookup"><span data-stu-id="91527-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="91527-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91527-104">SYNTAX</span></span>

### <span data-ttu-id="91527-105">GetItemsForContainer (Standard)</span><span class="sxs-lookup"><span data-stu-id="91527-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91527-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="91527-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91527-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="91527-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91527-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91527-108">DESCRIPTION</span></span>

<span data-ttu-id="91527-109">Mit dem Cmdlet **Get-AzRecoveryServicesBackupItem werden** die Elemente in einem Container oder ein Wert in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91527-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="91527-110">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="91527-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="91527-111">Für Azure Virtual Machines kann nur ein Sicherungselement im Container für virtuelle Maschinen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="91527-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="91527-112">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="91527-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="91527-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91527-113">EXAMPLES</span></span>

### <span data-ttu-id="91527-114">Beispiel 1: Abrufen eines Elements aus einem Sicherungs Container</span><span class="sxs-lookup"><span data-stu-id="91527-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="91527-115">Der erste Befehl ruft den Container vom Typ AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="91527-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="91527-116">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM in $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="91527-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="91527-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="91527-117">PARAMETERS</span></span>

### <span data-ttu-id="91527-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="91527-118">-BackupManagementType</span></span>

<span data-ttu-id="91527-119">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="91527-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="91527-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91527-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91527-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="91527-121">AzureVM</span></span>
- <span data-ttu-id="91527-122">Mars</span><span class="sxs-lookup"><span data-stu-id="91527-122">MARS</span></span>
- <span data-ttu-id="91527-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="91527-123">SCDPM</span></span>
- <span data-ttu-id="91527-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="91527-124">AzureBackupServer</span></span>
- <span data-ttu-id="91527-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="91527-125">AzureSQL</span></span>
- <span data-ttu-id="91527-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="91527-126">AzureStorage</span></span>
- <span data-ttu-id="91527-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="91527-127">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91527-128">-Container</span><span class="sxs-lookup"><span data-stu-id="91527-128">-Container</span></span>

<span data-ttu-id="91527-129">Gibt ein Containerobjekt an, aus dem dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="91527-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="91527-130">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupContainer** das Cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="91527-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="91527-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91527-131">-DefaultProfile</span></span>

<span data-ttu-id="91527-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91527-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91527-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="91527-133">-DeleteState</span></span>
<span data-ttu-id="91527-134">Gibt den deletestate des Elements an. die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91527-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91527-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="91527-135">ToBeDeleted</span></span>
- <span data-ttu-id="91527-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="91527-136">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91527-137">-Name</span><span class="sxs-lookup"><span data-stu-id="91527-137">-Name</span></span>

<span data-ttu-id="91527-138">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="91527-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="91527-139">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="91527-139">-Policy</span></span>

<span data-ttu-id="91527-140">Schutzrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="91527-140">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91527-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="91527-141">-ProtectionState</span></span>

<span data-ttu-id="91527-142">Gibt den Schutzstatus an.</span><span class="sxs-lookup"><span data-stu-id="91527-142">Specifies the state of protection.</span></span>
<span data-ttu-id="91527-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91527-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91527-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="91527-144">IRPending.</span></span>
<span data-ttu-id="91527-145">Die Erstsynchronisierung wurde nicht gestartet, und es gibt noch keinen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="91527-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="91527-146">Geschützten.</span><span class="sxs-lookup"><span data-stu-id="91527-146">Protected.</span></span>
<span data-ttu-id="91527-147">Der Schutz läuft.</span><span class="sxs-lookup"><span data-stu-id="91527-147">Protection is ongoing.</span></span>
- <span data-ttu-id="91527-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="91527-148">ProtectionError.</span></span>
<span data-ttu-id="91527-149">Es liegt ein Schutz Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="91527-149">There is a protection error.</span></span>
- <span data-ttu-id="91527-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="91527-150">ProtectionStopped.</span></span>
<span data-ttu-id="91527-151">Der Schutz ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="91527-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="91527-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="91527-152">-ProtectionStatus</span></span>

<span data-ttu-id="91527-153">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="91527-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="91527-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91527-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91527-155">Gesunde</span><span class="sxs-lookup"><span data-stu-id="91527-155">Healthy</span></span>
- <span data-ttu-id="91527-156">Ungesunde</span><span class="sxs-lookup"><span data-stu-id="91527-156">Unhealthy</span></span>

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

### <span data-ttu-id="91527-157">-Tresor</span><span class="sxs-lookup"><span data-stu-id="91527-157">-VaultId</span></span>

<span data-ttu-id="91527-158">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="91527-158">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91527-159">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="91527-159">-WorkloadType</span></span>

<span data-ttu-id="91527-160">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="91527-160">Specifies the workload type.</span></span>
<span data-ttu-id="91527-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91527-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91527-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="91527-162">AzureVM</span></span>
- <span data-ttu-id="91527-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="91527-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="91527-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="91527-164">AzureFiles</span></span>
- <span data-ttu-id="91527-165">MSSQL</span><span class="sxs-lookup"><span data-stu-id="91527-165">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91527-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91527-166">-CommonParameters</span></span>

<span data-ttu-id="91527-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91527-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91527-168">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91527-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91527-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91527-169">INPUTS</span></span>

### <span data-ttu-id="91527-170">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="91527-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="91527-171">System. String</span><span class="sxs-lookup"><span data-stu-id="91527-171">System.String</span></span>

## <span data-ttu-id="91527-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91527-172">OUTPUTS</span></span>

### <span data-ttu-id="91527-173">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="91527-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="91527-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="91527-174">NOTES</span></span>

## <span data-ttu-id="91527-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91527-175">RELATED LINKS</span></span>

[<span data-ttu-id="91527-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91527-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="91527-177">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="91527-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="91527-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="91527-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="91527-179">Wiederherstellen – AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91527-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
