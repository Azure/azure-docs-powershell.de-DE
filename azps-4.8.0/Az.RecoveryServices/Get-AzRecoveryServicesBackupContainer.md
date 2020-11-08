---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007901"
---
# <span data-ttu-id="0b7b5-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0b7b5-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0b7b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b7b5-102">SYNOPSIS</span></span>

<span data-ttu-id="0b7b5-103">Ruft Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-103">Gets Backup containers.</span></span>

## <span data-ttu-id="0b7b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b7b5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b7b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b7b5-105">DESCRIPTION</span></span>

<span data-ttu-id="0b7b5-106">Das Cmdlet " **Get-AzRecoveryServicesBackupContainer** " Ruft einen Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="0b7b5-107">Ein Sicherungs Container kapselt Datenquellen, die als Sicherungselemente modelliert sind.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="0b7b5-108">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0b7b5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b7b5-109">EXAMPLES</span></span>

### <span data-ttu-id="0b7b5-110">Beispiel 1: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="0b7b5-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="0b7b5-111">Dieser Befehl ruft den Container mit dem Namen V2VM vom Typ AzureVM ab.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="0b7b5-112">Beispiel 2: Abrufen aller Container eines bestimmten Typs</span><span class="sxs-lookup"><span data-stu-id="0b7b5-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="0b7b5-113">Dieser Befehl ruft alle Windows-Container ab, die durch den Azure Backup-Agent geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="0b7b5-114">Der **BackupManagementType** -Parameter ist nur für Windows-Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="0b7b5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b7b5-115">PARAMETERS</span></span>

### <span data-ttu-id="0b7b5-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0b7b5-116">-BackupManagementType</span></span>

<span data-ttu-id="0b7b5-117">Die Klasse der Ressourcen, die geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-117">The class of resources being protected.</span></span> <span data-ttu-id="0b7b5-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b7b5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b7b5-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0b7b5-119">AzureVM</span></span>
- <span data-ttu-id="0b7b5-120">Mars</span><span class="sxs-lookup"><span data-stu-id="0b7b5-120">MARS</span></span>
- <span data-ttu-id="0b7b5-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="0b7b5-121">AzureWorkload</span></span>
- <span data-ttu-id="0b7b5-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0b7b5-122">AzureStorage</span></span>

<span data-ttu-id="0b7b5-123">Dieser Parameter wird verwendet, um Windows-Computer zu unterscheiden, die mithilfe von Mars Agent oder anderen Sicherungsmodulen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="0b7b5-124">-Containertyp</span><span class="sxs-lookup"><span data-stu-id="0b7b5-124">-ContainerType</span></span>

<span data-ttu-id="0b7b5-125">Gibt den Typ des Sicherungs Containers an.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-125">Specifies the backup container type.</span></span>
<span data-ttu-id="0b7b5-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b7b5-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b7b5-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0b7b5-127">AzureVM</span></span>
- <span data-ttu-id="0b7b5-128">Windows</span><span class="sxs-lookup"><span data-stu-id="0b7b5-128">Windows</span></span>
- <span data-ttu-id="0b7b5-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="0b7b5-129">AzureSQL</span></span>
- <span data-ttu-id="0b7b5-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0b7b5-130">AzureStorage</span></span>
- <span data-ttu-id="0b7b5-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="0b7b5-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7b5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7b5-132">-DefaultProfile</span></span>

<span data-ttu-id="0b7b5-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b7b5-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0b7b5-134">-FriendlyName</span></span>

<span data-ttu-id="0b7b5-135">Gibt den Anzeigenamen des abzurufenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="0b7b5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b7b5-136">-ResourceGroupName</span></span>

<span data-ttu-id="0b7b5-137">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0b7b5-138">Dieser Parameter ist nur für Azure Virtual Machines vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="0b7b5-139">-Status</span><span class="sxs-lookup"><span data-stu-id="0b7b5-139">-Status</span></span>

<span data-ttu-id="0b7b5-140">Gibt den Container Registrierungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-140">Specifies the container registration status.</span></span>
<span data-ttu-id="0b7b5-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b7b5-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b7b5-142">Registriert</span><span class="sxs-lookup"><span data-stu-id="0b7b5-142">Registered</span></span>

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

### <span data-ttu-id="0b7b5-143">-Tresor</span><span class="sxs-lookup"><span data-stu-id="0b7b5-143">-VaultId</span></span>

<span data-ttu-id="0b7b5-144">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="0b7b5-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0b7b5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7b5-145">CommonParameters</span></span>
<span data-ttu-id="0b7b5-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7b5-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b7b5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7b5-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b7b5-148">INPUTS</span></span>

### <span data-ttu-id="0b7b5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0b7b5-149">System.String</span></span>

## <span data-ttu-id="0b7b5-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b7b5-150">OUTPUTS</span></span>

### <span data-ttu-id="0b7b5-151">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="0b7b5-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="0b7b5-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b7b5-152">NOTES</span></span>

## <span data-ttu-id="0b7b5-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b7b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="0b7b5-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b7b5-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0b7b5-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0b7b5-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="0b7b5-156">Registrierung aufheben-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0b7b5-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
