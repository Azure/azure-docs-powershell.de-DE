---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995592"
---
# <span data-ttu-id="4241c-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4241c-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4241c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4241c-102">SYNOPSIS</span></span>

<span data-ttu-id="4241c-103">Ruft die Elemente aus einem Container in Backup ab.</span><span class="sxs-lookup"><span data-stu-id="4241c-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="4241c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4241c-104">SYNTAX</span></span>

### <span data-ttu-id="4241c-105">GetItemsForContainer (Standard)</span><span class="sxs-lookup"><span data-stu-id="4241c-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4241c-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="4241c-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4241c-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="4241c-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4241c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4241c-108">DESCRIPTION</span></span>

<span data-ttu-id="4241c-109">Mit dem Cmdlet **Get-AzRecoveryServicesBackupItem werden** die Elemente in einem Container oder ein Wert in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4241c-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="4241c-110">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="4241c-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="4241c-111">Für Azure Virtual Machines kann nur ein Sicherungselement im Container für virtuelle Maschinen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4241c-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="4241c-112">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="4241c-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="4241c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4241c-113">EXAMPLES</span></span>

### <span data-ttu-id="4241c-114">Beispiel 1: Abrufen eines Elements aus einem Sicherungs Container</span><span class="sxs-lookup"><span data-stu-id="4241c-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="4241c-115">Der erste Befehl ruft den Container vom Typ AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="4241c-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4241c-116">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM in $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4241c-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="4241c-117">Beispiel 2: Abrufen eines Azure File Share-Elements aus FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4241c-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="4241c-118">Der erste Befehl ruft den Container vom Typ AzureStorage ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="4241c-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4241c-119">Der zweite Befehl ruft das Sicherungselement ab, dessen FriendlyName mit dem im Parameter FriendlyName übergebenen Wert übereinstimmt, und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4241c-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4241c-120">Die Verwendung des Parameters FriendlyName kann dazu führen, dass mehr als eine Azure-Dateifreigabe zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4241c-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="4241c-121">Verwenden Sie in solchen Fällen-Name-Parameter mit dem Parameterwert als die Name-Eigenschaft, die in $BackupItem Variablen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4241c-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="4241c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="4241c-122">PARAMETERS</span></span>

### <span data-ttu-id="4241c-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4241c-123">-BackupManagementType</span></span>

<span data-ttu-id="4241c-124">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="4241c-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="4241c-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4241c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4241c-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4241c-126">AzureVM</span></span>
- <span data-ttu-id="4241c-127">Mars</span><span class="sxs-lookup"><span data-stu-id="4241c-127">MARS</span></span>
- <span data-ttu-id="4241c-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="4241c-128">SCDPM</span></span>
- <span data-ttu-id="4241c-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="4241c-129">AzureBackupServer</span></span>
- <span data-ttu-id="4241c-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="4241c-130">AzureSQL</span></span>
- <span data-ttu-id="4241c-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4241c-131">AzureStorage</span></span>
- <span data-ttu-id="4241c-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="4241c-132">AzureWorkload</span></span>

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

### <span data-ttu-id="4241c-133">-Container</span><span class="sxs-lookup"><span data-stu-id="4241c-133">-Container</span></span>

<span data-ttu-id="4241c-134">Gibt ein Containerobjekt an, aus dem dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="4241c-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="4241c-135">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupContainer** das Cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="4241c-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="4241c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4241c-136">-DefaultProfile</span></span>

<span data-ttu-id="4241c-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4241c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4241c-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="4241c-138">-DeleteState</span></span>
<span data-ttu-id="4241c-139">Gibt den deletestate des Elements an. die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4241c-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4241c-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="4241c-140">ToBeDeleted</span></span>
- <span data-ttu-id="4241c-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="4241c-141">NotDeleted</span></span>

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

### <span data-ttu-id="4241c-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4241c-142">-FriendlyName</span></span>
<span data-ttu-id="4241c-143">FriendlyName des gesicherten Elements</span><span class="sxs-lookup"><span data-stu-id="4241c-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="4241c-144">-Name</span><span class="sxs-lookup"><span data-stu-id="4241c-144">-Name</span></span>

<span data-ttu-id="4241c-145">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="4241c-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4241c-146">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4241c-146">-Policy</span></span>

<span data-ttu-id="4241c-147">Schutzrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="4241c-147">Protection policy object.</span></span>

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

### <span data-ttu-id="4241c-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="4241c-148">-ProtectionState</span></span>

<span data-ttu-id="4241c-149">Gibt den Schutzstatus an.</span><span class="sxs-lookup"><span data-stu-id="4241c-149">Specifies the state of protection.</span></span>
<span data-ttu-id="4241c-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4241c-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4241c-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="4241c-151">IRPending.</span></span>
<span data-ttu-id="4241c-152">Die Erstsynchronisierung wurde nicht gestartet, und es gibt noch keinen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="4241c-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="4241c-153">Geschützten.</span><span class="sxs-lookup"><span data-stu-id="4241c-153">Protected.</span></span>
<span data-ttu-id="4241c-154">Der Schutz läuft.</span><span class="sxs-lookup"><span data-stu-id="4241c-154">Protection is ongoing.</span></span>
- <span data-ttu-id="4241c-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="4241c-155">ProtectionError.</span></span>
<span data-ttu-id="4241c-156">Es liegt ein Schutz Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="4241c-156">There is a protection error.</span></span>
- <span data-ttu-id="4241c-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="4241c-157">ProtectionStopped.</span></span>
<span data-ttu-id="4241c-158">Der Schutz ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4241c-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="4241c-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="4241c-159">-ProtectionStatus</span></span>

<span data-ttu-id="4241c-160">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="4241c-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="4241c-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4241c-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4241c-162">Gesunde</span><span class="sxs-lookup"><span data-stu-id="4241c-162">Healthy</span></span>
- <span data-ttu-id="4241c-163">Ungesunde</span><span class="sxs-lookup"><span data-stu-id="4241c-163">Unhealthy</span></span>

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

### <span data-ttu-id="4241c-164">-Tresor</span><span class="sxs-lookup"><span data-stu-id="4241c-164">-VaultId</span></span>

<span data-ttu-id="4241c-165">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="4241c-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4241c-166">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="4241c-166">-WorkloadType</span></span>

<span data-ttu-id="4241c-167">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="4241c-167">Specifies the workload type.</span></span>
<span data-ttu-id="4241c-168">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4241c-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4241c-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4241c-169">AzureVM</span></span>
- <span data-ttu-id="4241c-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="4241c-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="4241c-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="4241c-171">AzureFiles</span></span>
- <span data-ttu-id="4241c-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="4241c-172">MSSQL</span></span>

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

### <span data-ttu-id="4241c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4241c-173">CommonParameters</span></span>
<span data-ttu-id="4241c-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4241c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4241c-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4241c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4241c-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4241c-176">INPUTS</span></span>

### <span data-ttu-id="4241c-177">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="4241c-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="4241c-178">System. String</span><span class="sxs-lookup"><span data-stu-id="4241c-178">System.String</span></span>

## <span data-ttu-id="4241c-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4241c-179">OUTPUTS</span></span>

### <span data-ttu-id="4241c-180">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="4241c-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="4241c-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="4241c-181">NOTES</span></span>

## <span data-ttu-id="4241c-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4241c-182">RELATED LINKS</span></span>

[<span data-ttu-id="4241c-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4241c-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4241c-184">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4241c-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4241c-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4241c-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="4241c-186">Wiederherstellen – AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4241c-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
