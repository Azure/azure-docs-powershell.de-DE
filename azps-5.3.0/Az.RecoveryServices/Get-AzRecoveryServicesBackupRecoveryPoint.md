---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472091"
---
# <span data-ttu-id="6a14a-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6a14a-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="6a14a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a14a-102">SYNOPSIS</span></span>

<span data-ttu-id="6a14a-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="6a14a-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="6a14a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a14a-104">SYNTAX</span></span>

### <span data-ttu-id="6a14a-105">NoFilterParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a14a-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a14a-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="6a14a-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a14a-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="6a14a-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a14a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a14a-108">DESCRIPTION</span></span>

<span data-ttu-id="6a14a-109">Das **Get-AzRecoveryServicesBackupRecoveryPoint-Cmdlet** ruft die Wiederherstellungspunkte für ein gesichertes Azure Backup-Element ab.</span><span class="sxs-lookup"><span data-stu-id="6a14a-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="6a14a-110">Nachdem ein Element gesichert wurde, weist ein **AzureRmRecoveryServicesBackupRecoveryPoint-Objekt** einen oder mehrere Wiederherstellungspunkte auf.</span><span class="sxs-lookup"><span data-stu-id="6a14a-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="6a14a-111">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="6a14a-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="6a14a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a14a-112">EXAMPLES</span></span>

### <span data-ttu-id="6a14a-113">Beispiel 1: Erhalten von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="6a14a-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="6a14a-114">Der erste Befehl ruft das Tresorobjekt basierend auf "vaultName" ab.</span><span class="sxs-lookup"><span data-stu-id="6a14a-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="6a14a-115">Der zweite Befehl ruft das Datum aus sieben Tagen ab und speichert es dann in $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="6a14a-116">Der dritte Befehl ruft das aktuelle Datum ab und speichert ihn dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="6a14a-117">Der vierte Befehl ruft die AzureVM-Sicherungscontainer ab und speichert sie in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="6a14a-118">Der fünfte Befehl ruft das Sicherungselement auf Grundlage von workloadType, vaultId und speichert es dann in $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="6a14a-119">Der letzte Befehl ruft ein Array von Wiederherstellungspunkten für das Element in $BackupItem und speichert sie dann in $RP Variable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="6a14a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a14a-120">PARAMETERS</span></span>

### <span data-ttu-id="6a14a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a14a-121">-DefaultProfile</span></span>

<span data-ttu-id="6a14a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a14a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a14a-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6a14a-123">-EndDate</span></span>

<span data-ttu-id="6a14a-124">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="6a14a-124">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14a-125">-Item</span><span class="sxs-lookup"><span data-stu-id="6a14a-125">-Item</span></span>

<span data-ttu-id="6a14a-126">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="6a14a-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="6a14a-127">Verwenden Sie zum Abrufen **eines AzureRmRecoveryServicesBackupItem-Objekts** **das Cmdlet "Get-AzRecoveryServicesBackupItem".**</span><span class="sxs-lookup"><span data-stu-id="6a14a-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a14a-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="6a14a-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="6a14a-129">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den KeyVault Key für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="6a14a-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14a-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="6a14a-130">-RecoveryPointId</span></span>

<span data-ttu-id="6a14a-131">Gibt die Id des Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="6a14a-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14a-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="6a14a-132">-StartDate</span></span>

<span data-ttu-id="6a14a-133">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="6a14a-133">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14a-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6a14a-134">-VaultId</span></span>

<span data-ttu-id="6a14a-135">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6a14a-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6a14a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a14a-136">CommonParameters</span></span>
<span data-ttu-id="6a14a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a14a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a14a-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a14a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a14a-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a14a-139">INPUTS</span></span>

### <span data-ttu-id="6a14a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="6a14a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="6a14a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6a14a-141">System.String</span></span>

## <span data-ttu-id="6a14a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a14a-142">OUTPUTS</span></span>

### <span data-ttu-id="6a14a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6a14a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6a14a-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a14a-144">NOTES</span></span>

## <span data-ttu-id="6a14a-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a14a-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a14a-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6a14a-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="6a14a-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6a14a-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
