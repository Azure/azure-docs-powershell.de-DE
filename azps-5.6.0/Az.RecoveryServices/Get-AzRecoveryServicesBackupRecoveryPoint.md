---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9e9aab3a71e976d9c41694702dae7a8087da9a36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927803"
---
# <span data-ttu-id="91d5e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="91d5e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="91d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d5e-102">SYNOPSIS</span></span>

<span data-ttu-id="91d5e-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="91d5e-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="91d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91d5e-104">SYNTAX</span></span>

### <span data-ttu-id="91d5e-105">NoFilterParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91d5e-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91d5e-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="91d5e-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91d5e-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="91d5e-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91d5e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91d5e-108">DESCRIPTION</span></span>

<span data-ttu-id="91d5e-109">Das **Get-AzRecoveryServicesBackupRecoveryPoint-Cmdlet** ruft die Wiederherstellungspunkte für ein gesichertes Azure Backup-Element ab.</span><span class="sxs-lookup"><span data-stu-id="91d5e-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="91d5e-110">Nachdem ein Element gesichert wurde, weist ein **AzureRmRecoveryServicesBackupRecoveryPoint-Objekt** einen oder mehrere Wiederherstellungspunkte auf.</span><span class="sxs-lookup"><span data-stu-id="91d5e-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="91d5e-111">Legen Sie den Tresorkontext mithilfe des -VaultId-Parameters ein.</span><span class="sxs-lookup"><span data-stu-id="91d5e-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="91d5e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91d5e-112">EXAMPLES</span></span>

### <span data-ttu-id="91d5e-113">Beispiel 1: Erhalten von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="91d5e-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="91d5e-114">Der erste Befehl ruft das Tresorobjekt basierend auf VaultName ab.</span><span class="sxs-lookup"><span data-stu-id="91d5e-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="91d5e-115">Der zweite Befehl ruft das Datum von vor sieben Tagen ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="91d5e-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="91d5e-116">Der dritte Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="91d5e-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="91d5e-117">Der vierte Befehl ruft AzureVM-Sicherungscontainer ab und speichert sie in der $Container-Variable.</span><span class="sxs-lookup"><span data-stu-id="91d5e-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="91d5e-118">Mit dem fünften Befehl wird das Sicherungselement basierend auf workloadType, vaultId und dann in der $BackupItem gespeichert.</span><span class="sxs-lookup"><span data-stu-id="91d5e-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="91d5e-119">Der letzte Befehl ruft eine Matrix von Wiederherstellungspunkten für das Element in $BackupItem ab und speichert sie dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="91d5e-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="91d5e-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="91d5e-120">PARAMETERS</span></span>

### <span data-ttu-id="91d5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d5e-121">-DefaultProfile</span></span>

<span data-ttu-id="91d5e-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91d5e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91d5e-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="91d5e-123">-EndDate</span></span>

<span data-ttu-id="91d5e-124">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="91d5e-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="91d5e-125">-Item</span><span class="sxs-lookup"><span data-stu-id="91d5e-125">-Item</span></span>

<span data-ttu-id="91d5e-126">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="91d5e-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="91d5e-127">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem-Objekts** das **Get-AzRecoveryServicesBackupItem-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="91d5e-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="91d5e-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="91d5e-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="91d5e-129">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den KeyVault-Schlüssel für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="91d5e-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="91d5e-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="91d5e-130">-RecoveryPointId</span></span>

<span data-ttu-id="91d5e-131">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="91d5e-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="91d5e-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="91d5e-132">-StartDate</span></span>

<span data-ttu-id="91d5e-133">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="91d5e-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="91d5e-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="91d5e-134">-VaultId</span></span>

<span data-ttu-id="91d5e-135">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="91d5e-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="91d5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d5e-136">CommonParameters</span></span>
<span data-ttu-id="91d5e-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d5e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91d5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d5e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91d5e-139">INPUTS</span></span>

### <span data-ttu-id="91d5e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="91d5e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="91d5e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="91d5e-141">System.String</span></span>

## <span data-ttu-id="91d5e-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91d5e-142">OUTPUTS</span></span>

### <span data-ttu-id="91d5e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="91d5e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="91d5e-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="91d5e-144">NOTES</span></span>

## <span data-ttu-id="91d5e-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="91d5e-145">RELATED LINKS</span></span>

[<span data-ttu-id="91d5e-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="91d5e-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="91d5e-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91d5e-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
