---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659920"
---
# <span data-ttu-id="e5e7e-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e5e7e-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="e5e7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e7e-103">Ruft Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-103">Gets Backup containers.</span></span>

## <span data-ttu-id="e5e7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e7e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e7e-106">Das Cmdlet " **Get-AzRecoveryServicesBackupContainer** " Ruft einen Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="e5e7e-107">Ein Sicherungs Container kapselt Datenquellen, die als Sicherungselemente modelliert sind.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="e5e7e-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e5e7e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5e7e-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e7e-110">Beispiel 1: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="e5e7e-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="e5e7e-111">Dieser Befehl ruft den Container mit dem Namen V2VM vom Typ AzureVM ab.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="e5e7e-112">Beispiel 2: Abrufen aller Container eines bestimmten Typs</span><span class="sxs-lookup"><span data-stu-id="e5e7e-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="e5e7e-113">Dieser Befehl ruft alle Windows-Container ab, die durch den Azure Backup-Agent geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="e5e7e-114">Der *BackupManagementType* -Parameter ist nur für Windows-Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="e5e7e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5e7e-115">PARAMETERS</span></span>

### <span data-ttu-id="e5e7e-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e5e7e-116">-BackupManagementType</span></span>
<span data-ttu-id="e5e7e-117">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-117">Specifies the backup management type.</span></span>
<span data-ttu-id="e5e7e-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5e7e-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5e7e-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5e7e-119">AzureVM</span></span>
- <span data-ttu-id="e5e7e-120">Mars</span><span class="sxs-lookup"><span data-stu-id="e5e7e-120">MARS</span></span>
- <span data-ttu-id="e5e7e-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="e5e7e-121">AzureSQL</span></span>
- <span data-ttu-id="e5e7e-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e5e7e-122">AzureStorage</span></span>

<span data-ttu-id="e5e7e-123">Dieser Parameter wird verwendet, um Windows-Computer zu unterscheiden, die mithilfe von Mars Agent oder anderen Sicherungsmodulen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e7e-124">-Containertyp</span><span class="sxs-lookup"><span data-stu-id="e5e7e-124">-ContainerType</span></span>
<span data-ttu-id="e5e7e-125">Gibt den Typ des Sicherungs Containers an.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-125">Specifies the backup container type.</span></span>
<span data-ttu-id="e5e7e-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5e7e-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5e7e-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5e7e-127">AzureVM</span></span> 
- <span data-ttu-id="e5e7e-128">Windows</span><span class="sxs-lookup"><span data-stu-id="e5e7e-128">Windows</span></span>
- <span data-ttu-id="e5e7e-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="e5e7e-129">AzureSQL</span></span>
- <span data-ttu-id="e5e7e-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e5e7e-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e7e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e7e-131">-DefaultProfile</span></span>
<span data-ttu-id="e5e7e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e7e-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5e7e-133">-FriendlyName</span></span>
<span data-ttu-id="e5e7e-134">Gibt den Anzeigenamen des abzurufenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="e5e7e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e7e-135">-ResourceGroupName</span></span>
<span data-ttu-id="e5e7e-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e5e7e-137">Dieser Parameter ist nur für Azure Virtual Machines vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="e5e7e-138">-Status</span><span class="sxs-lookup"><span data-stu-id="e5e7e-138">-Status</span></span>
<span data-ttu-id="e5e7e-139">Gibt den Container Registrierungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-139">Specifies the container registration status.</span></span>
<span data-ttu-id="e5e7e-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5e7e-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5e7e-141">Registriert</span><span class="sxs-lookup"><span data-stu-id="e5e7e-141">Registered</span></span>

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

### <span data-ttu-id="e5e7e-142">-Tresor</span><span class="sxs-lookup"><span data-stu-id="e5e7e-142">-VaultId</span></span>
<span data-ttu-id="e5e7e-143">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="e5e7e-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e5e7e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e7e-144">CommonParameters</span></span>
<span data-ttu-id="e5e7e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e7e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e7e-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e7e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e7e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5e7e-147">INPUTS</span></span>

### <span data-ttu-id="e5e7e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e7e-148">System.String</span></span>

## <span data-ttu-id="e5e7e-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5e7e-149">OUTPUTS</span></span>

### <span data-ttu-id="e5e7e-150">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e5e7e-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="e5e7e-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5e7e-151">NOTES</span></span>

## <span data-ttu-id="e5e7e-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5e7e-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5e7e-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5e7e-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e5e7e-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e5e7e-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="e5e7e-155">Registrierung aufheben-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e5e7e-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

