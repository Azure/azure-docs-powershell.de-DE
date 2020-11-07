---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659919"
---
# <span data-ttu-id="16720-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="16720-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="16720-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16720-102">SYNOPSIS</span></span>
<span data-ttu-id="16720-103">Ruft die Elemente aus einem Container in Backup ab.</span><span class="sxs-lookup"><span data-stu-id="16720-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="16720-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16720-104">SYNTAX</span></span>

### <span data-ttu-id="16720-105">GetItemsForContainer (Standard)</span><span class="sxs-lookup"><span data-stu-id="16720-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16720-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="16720-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16720-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="16720-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16720-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16720-108">DESCRIPTION</span></span>
<span data-ttu-id="16720-109">Mit dem Cmdlet **Get-AzRecoveryServicesBackupItem werden** die Elemente in einem Container oder ein Wert in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="16720-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="16720-110">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="16720-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="16720-111">Für Azure Virtual Machines kann nur ein Sicherungselement im Container für virtuelle Maschinen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="16720-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="16720-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="16720-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="16720-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16720-113">EXAMPLES</span></span>

### <span data-ttu-id="16720-114">Beispiel 1: Abrufen eines Elements aus einem Sicherungs Container</span><span class="sxs-lookup"><span data-stu-id="16720-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="16720-115">Der erste Befehl ruft den Container vom Typ AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="16720-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="16720-116">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM in $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16720-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="16720-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="16720-117">PARAMETERS</span></span>

### <span data-ttu-id="16720-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="16720-118">-BackupManagementType</span></span>
<span data-ttu-id="16720-119">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="16720-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="16720-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16720-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16720-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="16720-121">AzureVM</span></span> 
- <span data-ttu-id="16720-122">Mars</span><span class="sxs-lookup"><span data-stu-id="16720-122">MARS</span></span> 
- <span data-ttu-id="16720-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="16720-123">SCDPM</span></span> 
- <span data-ttu-id="16720-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="16720-124">AzureBackupServer</span></span> 
- <span data-ttu-id="16720-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="16720-125">AzureSQL</span></span>
- <span data-ttu-id="16720-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="16720-126">AzureStorage</span></span>

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

### <span data-ttu-id="16720-127">-Container</span><span class="sxs-lookup"><span data-stu-id="16720-127">-Container</span></span>
<span data-ttu-id="16720-128">Gibt ein Containerobjekt an, aus dem dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="16720-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="16720-129">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupContainer** das Get-AzRecoveryServicesBackupContainer-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16720-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="16720-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16720-130">-DefaultProfile</span></span>
<span data-ttu-id="16720-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16720-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16720-132">-Name</span><span class="sxs-lookup"><span data-stu-id="16720-132">-Name</span></span>
<span data-ttu-id="16720-133">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="16720-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="16720-134">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="16720-134">-Policy</span></span>
<span data-ttu-id="16720-135">Schutzrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="16720-135">Protection policy object.</span></span>

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

### <span data-ttu-id="16720-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="16720-136">-ProtectionState</span></span>
<span data-ttu-id="16720-137">Gibt den Schutzstatus an.</span><span class="sxs-lookup"><span data-stu-id="16720-137">Specifies the state of protection.</span></span>
<span data-ttu-id="16720-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16720-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16720-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="16720-139">IRPending.</span></span>
<span data-ttu-id="16720-140">Die Erstsynchronisierung wurde nicht gestartet, und es gibt noch keinen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="16720-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="16720-141">Geschützten.</span><span class="sxs-lookup"><span data-stu-id="16720-141">Protected.</span></span>
<span data-ttu-id="16720-142">Der Schutz läuft.</span><span class="sxs-lookup"><span data-stu-id="16720-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="16720-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="16720-143">ProtectionError.</span></span>
<span data-ttu-id="16720-144">Es liegt ein Schutz Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="16720-144">There is a protection error.</span></span>
- <span data-ttu-id="16720-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="16720-145">ProtectionStopped.</span></span>
<span data-ttu-id="16720-146">Der Schutz ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="16720-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="16720-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="16720-147">-ProtectionStatus</span></span>
<span data-ttu-id="16720-148">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="16720-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="16720-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16720-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16720-150">Gesunde</span><span class="sxs-lookup"><span data-stu-id="16720-150">Healthy</span></span>
- <span data-ttu-id="16720-151">Ungesunde</span><span class="sxs-lookup"><span data-stu-id="16720-151">Unhealthy</span></span>

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

### <span data-ttu-id="16720-152">-Tresor</span><span class="sxs-lookup"><span data-stu-id="16720-152">-VaultId</span></span>
<span data-ttu-id="16720-153">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="16720-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="16720-154">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="16720-154">-WorkloadType</span></span>
<span data-ttu-id="16720-155">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="16720-155">Specifies the workload type.</span></span> <span data-ttu-id="16720-156">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16720-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16720-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="16720-157">AzureVM</span></span> 
- <span data-ttu-id="16720-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="16720-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="16720-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="16720-159">AzureFiles</span></span>

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

### <span data-ttu-id="16720-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16720-160">CommonParameters</span></span>
<span data-ttu-id="16720-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16720-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16720-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16720-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16720-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16720-163">INPUTS</span></span>

### <span data-ttu-id="16720-164">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="16720-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="16720-165">System. String</span><span class="sxs-lookup"><span data-stu-id="16720-165">System.String</span></span>

## <span data-ttu-id="16720-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16720-166">OUTPUTS</span></span>

### <span data-ttu-id="16720-167">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="16720-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="16720-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="16720-168">NOTES</span></span>

## <span data-ttu-id="16720-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16720-169">RELATED LINKS</span></span>

[<span data-ttu-id="16720-170">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="16720-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="16720-171">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="16720-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="16720-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="16720-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="16720-173">Wiederherstellen – AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="16720-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


