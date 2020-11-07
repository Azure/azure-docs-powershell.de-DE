---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664741"
---
# <span data-ttu-id="7a199-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7a199-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="7a199-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a199-102">SYNOPSIS</span></span>
<span data-ttu-id="7a199-103">Ruft Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="7a199-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a199-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a199-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a199-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a199-105">DESCRIPTION</span></span>
<span data-ttu-id="7a199-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupContainer** " Ruft einen Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="7a199-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="7a199-107">Ein Sicherungs Container kapselt Datenquellen, die als Sicherungselemente modelliert sind.</span><span class="sxs-lookup"><span data-stu-id="7a199-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="7a199-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a199-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7a199-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a199-109">EXAMPLES</span></span>

### <span data-ttu-id="7a199-110">Beispiel 1: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="7a199-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="7a199-111">Dieser Befehl ruft den Container mit dem Namen V2VM vom Typ AzureVM ab.</span><span class="sxs-lookup"><span data-stu-id="7a199-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="7a199-112">Beispiel 2: Abrufen aller Container eines bestimmten Typs</span><span class="sxs-lookup"><span data-stu-id="7a199-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="7a199-113">Dieser Befehl ruft alle Windows-Container ab, die durch den Azure Backup-Agent geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="7a199-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="7a199-114">Der *BackupManagementType* -Parameter ist nur für Windows-Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a199-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="7a199-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a199-115">PARAMETERS</span></span>

### <span data-ttu-id="7a199-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7a199-116">-BackupManagementType</span></span>
<span data-ttu-id="7a199-117">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="7a199-117">Specifies the backup management type.</span></span>
<span data-ttu-id="7a199-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7a199-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a199-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7a199-119">AzureVM</span></span>
- <span data-ttu-id="7a199-120">Mars</span><span class="sxs-lookup"><span data-stu-id="7a199-120">MARS</span></span>
- <span data-ttu-id="7a199-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="7a199-121">AzureSQL</span></span>

<span data-ttu-id="7a199-122">Dieser Parameter wird verwendet, um Windows-Computer zu unterscheiden, die mithilfe von Mars Agent oder anderen Sicherungsmodulen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="7a199-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-123">-Containertyp</span><span class="sxs-lookup"><span data-stu-id="7a199-123">-ContainerType</span></span>
<span data-ttu-id="7a199-124">Gibt den Typ des Sicherungs Containers an.</span><span class="sxs-lookup"><span data-stu-id="7a199-124">Specifies the backup container type.</span></span>
<span data-ttu-id="7a199-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7a199-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a199-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7a199-126">AzureVM</span></span> 
- <span data-ttu-id="7a199-127">Windows</span><span class="sxs-lookup"><span data-stu-id="7a199-127">Windows</span></span>
- <span data-ttu-id="7a199-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="7a199-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7a199-129">-FriendlyName</span></span>
<span data-ttu-id="7a199-130">Gibt den Anzeigenamen des abzurufenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="7a199-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="7a199-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7a199-131">-Name</span></span>
<span data-ttu-id="7a199-132">Gibt den Namen des abzurufenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="7a199-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="7a199-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a199-133">-ResourceGroupName</span></span>
<span data-ttu-id="7a199-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7a199-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7a199-135">Dieser Parameter ist nur für Azure Virtual Machines vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="7a199-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="7a199-136">-Status</span><span class="sxs-lookup"><span data-stu-id="7a199-136">-Status</span></span>
<span data-ttu-id="7a199-137">Gibt den Container Registrierungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="7a199-137">Specifies the container registration status.</span></span>
<span data-ttu-id="7a199-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7a199-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a199-139">Registriert</span><span class="sxs-lookup"><span data-stu-id="7a199-139">Registered</span></span>

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

### <span data-ttu-id="7a199-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a199-140">-DefaultProfile</span></span>
<span data-ttu-id="7a199-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a199-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a199-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a199-142">CommonParameters</span></span>
<span data-ttu-id="7a199-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a199-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a199-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a199-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a199-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a199-145">INPUTS</span></span>

## <span data-ttu-id="7a199-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a199-146">OUTPUTS</span></span>

### <span data-ttu-id="7a199-147">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7a199-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="7a199-148">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="7a199-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="7a199-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a199-149">NOTES</span></span>

## <span data-ttu-id="7a199-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a199-150">RELATED LINKS</span></span>

[<span data-ttu-id="7a199-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7a199-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="7a199-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7a199-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="7a199-153">Registrierung aufheben-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7a199-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


