---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0fb1df2d72259c6c0f427a9a66f4cf271cc0cbfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934760"
---
# <span data-ttu-id="b7730-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b7730-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="b7730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7730-102">SYNOPSIS</span></span>

<span data-ttu-id="b7730-103">Ruft Sicherungscontainer ab.</span><span class="sxs-lookup"><span data-stu-id="b7730-103">Gets Backup containers.</span></span>

## <span data-ttu-id="b7730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7730-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7730-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7730-105">DESCRIPTION</span></span>

<span data-ttu-id="b7730-106">Das **Get-AzRecoveryServicesBackupContainer-Cmdlet** erhält einen Sicherungscontainer.</span><span class="sxs-lookup"><span data-stu-id="b7730-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="b7730-107">Ein Sicherungscontainer kapselt Datenquellen, die als Sicherungselemente modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="b7730-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="b7730-108">Für den Containertyp "Azure VM" werden in der Ausgabe alle Container aufgeführt, deren Name genau mit dem Container entspricht, der als Wert für den Parameter "Anzeigename" übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b7730-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="b7730-109">Bei anderen Containertypen enthält die Ausgabe eine Liste von Containern, deren Name dem Wert ähnelt, der für den Parameter "Anzeigename" übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b7730-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="b7730-110">Legen Sie den Tresorkontext mithilfe des -VaultId-Parameters ein.</span><span class="sxs-lookup"><span data-stu-id="b7730-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b7730-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7730-111">EXAMPLES</span></span>

### <span data-ttu-id="b7730-112">Beispiel 1: Einen bestimmten Container erhalten</span><span class="sxs-lookup"><span data-stu-id="b7730-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="b7730-113">Dieser Befehl ruft den Container mit dem Namen V2VM vom Typ AzureVM ab.</span><span class="sxs-lookup"><span data-stu-id="b7730-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="b7730-114">Beispiel 2: Alle Container eines bestimmten Typs erhalten</span><span class="sxs-lookup"><span data-stu-id="b7730-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="b7730-115">Dieser Befehl ruft alle Windows-Container ab, die vom Azure Backup-Agent geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="b7730-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="b7730-116">Der **Parameter BackupManagementType** ist nur für Windows-Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7730-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="b7730-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7730-117">PARAMETERS</span></span>

### <span data-ttu-id="b7730-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b7730-118">-BackupManagementType</span></span>

<span data-ttu-id="b7730-119">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b7730-119">The class of resources being protected.</span></span> <span data-ttu-id="b7730-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7730-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7730-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b7730-121">AzureVM</span></span>
- <span data-ttu-id="b7730-122">MARS</span><span class="sxs-lookup"><span data-stu-id="b7730-122">MARS</span></span>
- <span data-ttu-id="b7730-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b7730-123">AzureWorkload</span></span>
- <span data-ttu-id="b7730-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b7730-124">AzureStorage</span></span>

<span data-ttu-id="b7730-125">Dieser Parameter wird verwendet, um Windows-Computer zu unterscheiden, die mit dem MARS-Agent oder anderen Sicherungsmodule gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="b7730-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="b7730-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="b7730-126">-ContainerType</span></span>

<span data-ttu-id="b7730-127">Gibt den Sicherungscontainertyp an.</span><span class="sxs-lookup"><span data-stu-id="b7730-127">Specifies the backup container type.</span></span>
<span data-ttu-id="b7730-128">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7730-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7730-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b7730-129">AzureVM</span></span>
- <span data-ttu-id="b7730-130">Windows</span><span class="sxs-lookup"><span data-stu-id="b7730-130">Windows</span></span>
- <span data-ttu-id="b7730-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b7730-131">AzureStorage</span></span>
- <span data-ttu-id="b7730-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="b7730-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="b7730-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7730-133">-DefaultProfile</span></span>

<span data-ttu-id="b7730-134">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7730-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7730-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b7730-135">-FriendlyName</span></span>

<span data-ttu-id="b7730-136">Gibt den Anzeigenamen des zu erhaltenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="b7730-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="b7730-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7730-137">-ResourceGroupName</span></span>

<span data-ttu-id="b7730-138">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b7730-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b7730-139">Dieser Parameter gilt nur für virtuelle Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="b7730-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="b7730-140">-Status</span><span class="sxs-lookup"><span data-stu-id="b7730-140">-Status</span></span>

<span data-ttu-id="b7730-141">Gibt den Containerregistrierungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="b7730-141">Specifies the container registration status.</span></span>
<span data-ttu-id="b7730-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7730-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7730-143">Registriert</span><span class="sxs-lookup"><span data-stu-id="b7730-143">Registered</span></span>

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

### <span data-ttu-id="b7730-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b7730-144">-VaultId</span></span>

<span data-ttu-id="b7730-145">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="b7730-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b7730-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7730-146">CommonParameters</span></span>
<span data-ttu-id="b7730-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7730-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7730-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7730-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7730-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7730-149">INPUTS</span></span>

### <span data-ttu-id="b7730-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b7730-150">System.String</span></span>

## <span data-ttu-id="b7730-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7730-151">OUTPUTS</span></span>

### <span data-ttu-id="b7730-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b7730-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="b7730-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7730-153">NOTES</span></span>

## <span data-ttu-id="b7730-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7730-154">RELATED LINKS</span></span>

[<span data-ttu-id="b7730-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7730-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b7730-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b7730-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="b7730-157">Aufheben der Registrierung-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b7730-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
