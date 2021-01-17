---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470367"
---
# <span data-ttu-id="7f805-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7f805-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="7f805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f805-102">SYNOPSIS</span></span>

<span data-ttu-id="7f805-103">Ruft Sicherungscontainer ab.</span><span class="sxs-lookup"><span data-stu-id="7f805-103">Gets Backup containers.</span></span>

## <span data-ttu-id="7f805-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f805-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f805-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f805-105">DESCRIPTION</span></span>

<span data-ttu-id="7f805-106">Das **Cmdlet "Get-AzRecoveryServicesBackupContainer"** ruft einen Sicherungscontainer ab.</span><span class="sxs-lookup"><span data-stu-id="7f805-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="7f805-107">Ein Sicherungscontainer kapselt Datenquellen, die als Sicherungselemente modelliert sind.</span><span class="sxs-lookup"><span data-stu-id="7f805-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="7f805-108">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="7f805-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="7f805-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f805-109">EXAMPLES</span></span>

### <span data-ttu-id="7f805-110">Beispiel 1: Erhalten eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="7f805-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="7f805-111">Dieser Befehl ruft den Container "V2VM" vom Typ "AzureVM" ab.</span><span class="sxs-lookup"><span data-stu-id="7f805-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="7f805-112">Beispiel 2: Alle Container eines bestimmten Typs erhalten</span><span class="sxs-lookup"><span data-stu-id="7f805-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="7f805-113">Dieser Befehl ruft alle Windows-Container ab, die durch den Azure Backup-Agent geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="7f805-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="7f805-114">Der **Parameter "BackupManagementType"** ist nur für Windows-Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f805-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="7f805-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f805-115">PARAMETERS</span></span>

### <span data-ttu-id="7f805-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7f805-116">-BackupManagementType</span></span>

<span data-ttu-id="7f805-117">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7f805-117">The class of resources being protected.</span></span> <span data-ttu-id="7f805-118">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="7f805-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f805-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f805-119">AzureVM</span></span>
- <span data-ttu-id="7f805-120">MARS</span><span class="sxs-lookup"><span data-stu-id="7f805-120">MARS</span></span>
- <span data-ttu-id="7f805-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="7f805-121">AzureWorkload</span></span>
- <span data-ttu-id="7f805-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7f805-122">AzureStorage</span></span>

<span data-ttu-id="7f805-123">Dieser Parameter wird verwendet, um Windows-Computer, die mit dem MARS-Agent oder anderen Sicherungsmodule gesichert werden, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7f805-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f805-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="7f805-124">-ContainerType</span></span>

<span data-ttu-id="7f805-125">Gibt den Sicherungscontainertyp an.</span><span class="sxs-lookup"><span data-stu-id="7f805-125">Specifies the backup container type.</span></span>
<span data-ttu-id="7f805-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="7f805-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f805-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f805-127">AzureVM</span></span>
- <span data-ttu-id="7f805-128">Windows</span><span class="sxs-lookup"><span data-stu-id="7f805-128">Windows</span></span>
- <span data-ttu-id="7f805-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7f805-129">AzureStorage</span></span>
- <span data-ttu-id="7f805-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="7f805-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f805-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f805-131">-DefaultProfile</span></span>

<span data-ttu-id="7f805-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f805-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f805-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f805-133">-FriendlyName</span></span>

<span data-ttu-id="7f805-134">Gibt den Anzeigenamen des zu erhaltenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="7f805-134">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f805-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f805-135">-ResourceGroupName</span></span>

<span data-ttu-id="7f805-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7f805-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7f805-137">Dieser Parameter gilt nur für virtuelle Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="7f805-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f805-138">-Status</span><span class="sxs-lookup"><span data-stu-id="7f805-138">-Status</span></span>

<span data-ttu-id="7f805-139">Gibt den Containerregistrierungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="7f805-139">Specifies the container registration status.</span></span>
<span data-ttu-id="7f805-140">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="7f805-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f805-141">Registriert</span><span class="sxs-lookup"><span data-stu-id="7f805-141">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f805-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7f805-142">-VaultId</span></span>

<span data-ttu-id="7f805-143">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="7f805-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7f805-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f805-144">CommonParameters</span></span>
<span data-ttu-id="7f805-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f805-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f805-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f805-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f805-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f805-147">INPUTS</span></span>

### <span data-ttu-id="7f805-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7f805-148">System.String</span></span>

## <span data-ttu-id="7f805-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f805-149">OUTPUTS</span></span>

### <span data-ttu-id="7f805-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7f805-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="7f805-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f805-151">NOTES</span></span>

## <span data-ttu-id="7f805-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f805-152">RELATED LINKS</span></span>

[<span data-ttu-id="7f805-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7f805-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7f805-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7f805-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="7f805-155">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7f805-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
