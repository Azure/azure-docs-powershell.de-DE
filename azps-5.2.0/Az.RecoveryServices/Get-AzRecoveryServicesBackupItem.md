---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308704"
---
# <span data-ttu-id="2cb93-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cb93-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2cb93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb93-102">SYNOPSIS</span></span>

<span data-ttu-id="2cb93-103">Ruft die Elemente aus einem Container in "Sicherung" ab.</span><span class="sxs-lookup"><span data-stu-id="2cb93-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="2cb93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cb93-104">SYNTAX</span></span>

### <span data-ttu-id="2cb93-105">GetItemsForContainer (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cb93-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb93-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="2cb93-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb93-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="2cb93-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb93-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cb93-108">DESCRIPTION</span></span>

<span data-ttu-id="2cb93-109">Das **Cmdlet "Get-AzRecoveryServicesBackupItem"** ruft die Liste der geschützten Elemente in einem Container und den Schutzstatus der Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="2cb93-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="2cb93-110">Ein Container, der in einem Azure Recovery Services-Tresor registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="2cb93-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="2cb93-111">Für virtuelle Azure-Computer kann nur ein Sicherungselement im Container des virtuellen Computers vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2cb93-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="2cb93-112">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="2cb93-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="2cb93-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cb93-113">EXAMPLES</span></span>

### <span data-ttu-id="2cb93-114">Beispiel 1: Erhalten eines Elements aus einem Sicherungscontainer</span><span class="sxs-lookup"><span data-stu-id="2cb93-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="2cb93-115">Der erste Befehl ruft den Container vom Typ "AzureVM" ab und speichert ihn dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="2cb93-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cb93-116">Der zweite Befehl ruft das Sicherungselement "V2VM" in $Container und speichert es dann in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="2cb93-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="2cb93-117">Beispiel 2: Herunterladen eines Azure-Dateifreigabeelements von FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2cb93-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="2cb93-118">Der erste Befehl ruft den Container vom Typ "AzureStorage" ab und speichert ihn dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="2cb93-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cb93-119">Der zweite Befehl ruft das Sicherungselement ab, dessen friendlyName dem in "FriendlyName Parameter" übergebenen Wert entspricht, und speichert es dann in $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="2cb93-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2cb93-120">Die Verwendung des Parameters "FriendlyName" kann dazu führen, dass mehr als eine Azure-Dateifreigabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2cb93-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="2cb93-121">Führen Sie in solchen Fällen das Cmdlet aus, indem Sie den Wert für den Parameter "-Name" als die Eigenschaft "Name" übergeben, die im Ergebnissatz der $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="2cb93-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="2cb93-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cb93-122">PARAMETERS</span></span>

### <span data-ttu-id="2cb93-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2cb93-123">-BackupManagementType</span></span>

<span data-ttu-id="2cb93-124">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2cb93-124">The class of resources being protected.</span></span> <span data-ttu-id="2cb93-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2cb93-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cb93-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2cb93-126">AzureVM</span></span>
- <span data-ttu-id="2cb93-127">MAB</span><span class="sxs-lookup"><span data-stu-id="2cb93-127">MAB</span></span>
- <span data-ttu-id="2cb93-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="2cb93-128">AzureStorage</span></span>
- <span data-ttu-id="2cb93-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="2cb93-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb93-130">-Container</span><span class="sxs-lookup"><span data-stu-id="2cb93-130">-Container</span></span>

<span data-ttu-id="2cb93-131">Gibt ein Containerobjekt an, aus dem dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="2cb93-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="2cb93-132">Verwenden Sie zum **Abrufen eines AzureRmRecoveryServicesBackupContainers** das **Cmdlet "Get-AzRecoveryServicesBackupContainer".**</span><span class="sxs-lookup"><span data-stu-id="2cb93-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="2cb93-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb93-133">-DefaultProfile</span></span>

<span data-ttu-id="2cb93-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cb93-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb93-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="2cb93-135">-DeleteState</span></span>
<span data-ttu-id="2cb93-136">Gibt den Löschzustand des Elements an. Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2cb93-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cb93-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="2cb93-137">ToBeDeleted</span></span>
- <span data-ttu-id="2cb93-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="2cb93-138">NotDeleted</span></span>

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

### <span data-ttu-id="2cb93-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2cb93-139">-FriendlyName</span></span>
<span data-ttu-id="2cb93-140">FriendlyName des gesicherten Elements</span><span class="sxs-lookup"><span data-stu-id="2cb93-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="2cb93-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2cb93-141">-Name</span></span>

<span data-ttu-id="2cb93-142">Gibt den Namen des Sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="2cb93-142">Specifies the name of backup item.</span></span> <span data-ttu-id="2cb93-143">Geben Sie für die Dateifreigabe die eindeutige ID der geschützten Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="2cb93-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="2cb93-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="2cb93-144">-Policy</span></span>

<span data-ttu-id="2cb93-145">Schutzrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="2cb93-145">Protection policy object.</span></span>

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

### <span data-ttu-id="2cb93-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="2cb93-146">-ProtectionState</span></span>

<span data-ttu-id="2cb93-147">Gibt den Schutzstatus an.</span><span class="sxs-lookup"><span data-stu-id="2cb93-147">Specifies the state of protection.</span></span>
<span data-ttu-id="2cb93-148">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2cb93-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cb93-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="2cb93-149">IRPending.</span></span>
<span data-ttu-id="2cb93-150">Die Erstsynchronisierung wurde noch nicht gestartet, und es gibt noch keinen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="2cb93-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="2cb93-151">Geschützt.</span><span class="sxs-lookup"><span data-stu-id="2cb93-151">Protected.</span></span>
<span data-ttu-id="2cb93-152">Der Schutz ist noch nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2cb93-152">Protection is ongoing.</span></span>
- <span data-ttu-id="2cb93-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="2cb93-153">ProtectionError.</span></span>
<span data-ttu-id="2cb93-154">Es liegt ein Schutzfehler vor.</span><span class="sxs-lookup"><span data-stu-id="2cb93-154">There is a protection error.</span></span>
- <span data-ttu-id="2cb93-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="2cb93-155">ProtectionStopped.</span></span>
<span data-ttu-id="2cb93-156">Der Schutz ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2cb93-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="2cb93-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="2cb93-157">-ProtectionStatus</span></span>

<span data-ttu-id="2cb93-158">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="2cb93-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="2cb93-159">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2cb93-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cb93-160">Fehlerfrei</span><span class="sxs-lookup"><span data-stu-id="2cb93-160">Healthy</span></span>
- <span data-ttu-id="2cb93-161">Fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="2cb93-161">Unhealthy</span></span>

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

### <span data-ttu-id="2cb93-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2cb93-162">-VaultId</span></span>

<span data-ttu-id="2cb93-163">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="2cb93-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2cb93-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="2cb93-164">-WorkloadType</span></span>

<span data-ttu-id="2cb93-165">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2cb93-165">Workload type of the resource.</span></span> <span data-ttu-id="2cb93-166">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2cb93-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cb93-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2cb93-167">AzureVM</span></span>
- <span data-ttu-id="2cb93-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="2cb93-168">AzureFiles</span></span>
- <span data-ttu-id="2cb93-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="2cb93-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb93-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb93-170">CommonParameters</span></span>
<span data-ttu-id="2cb93-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb93-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb93-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cb93-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb93-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cb93-173">INPUTS</span></span>

### <span data-ttu-id="2cb93-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2cb93-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="2cb93-175">System.String</span><span class="sxs-lookup"><span data-stu-id="2cb93-175">System.String</span></span>

## <span data-ttu-id="2cb93-176">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cb93-176">OUTPUTS</span></span>

### <span data-ttu-id="2cb93-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="2cb93-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="2cb93-178">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cb93-178">NOTES</span></span>

## <span data-ttu-id="2cb93-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cb93-179">RELATED LINKS</span></span>

[<span data-ttu-id="2cb93-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cb93-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2cb93-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2cb93-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2cb93-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cb93-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="2cb93-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cb93-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
