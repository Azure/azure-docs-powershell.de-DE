---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160204"
---
# <span data-ttu-id="9833d-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9833d-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="9833d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9833d-102">SYNOPSIS</span></span>

<span data-ttu-id="9833d-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="9833d-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="9833d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9833d-104">SYNTAX</span></span>

### <span data-ttu-id="9833d-105">NoFilterParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9833d-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9833d-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="9833d-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9833d-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9833d-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9833d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9833d-108">DESCRIPTION</span></span>

<span data-ttu-id="9833d-109">Das **Get-AzRecoveryServicesBackupRecoveryPoint-Cmdlet** ruft die Wiederherstellungspunkte für ein gesichertes Azure Backup-Element ab.</span><span class="sxs-lookup"><span data-stu-id="9833d-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9833d-110">Nachdem ein Element gesichert wurde, weist ein **AzureRmRecoveryServicesBackupRecoveryPoint-Objekt** einen oder mehrere Wiederherstellungspunkte auf.</span><span class="sxs-lookup"><span data-stu-id="9833d-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="9833d-111">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="9833d-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="9833d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9833d-112">EXAMPLES</span></span>

### <span data-ttu-id="9833d-113">Beispiel 1: Erhalten von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="9833d-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="9833d-114">Der erste Befehl ruft das Tresorobjekt basierend auf "vaultName" ab.</span><span class="sxs-lookup"><span data-stu-id="9833d-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="9833d-115">Der zweite Befehl ruft das Datum von vor sieben Tagen ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="9833d-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9833d-116">Der dritte Befehl ruft das aktuelle Datum ab und speichert ihn dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="9833d-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9833d-117">Der vierte Befehl ruft die AzureVM-Sicherungscontainer ab und speichert sie in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="9833d-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="9833d-118">Der fünfte Befehl ruft das Sicherungselement basierend auf workloadType, vaultId und speichert es dann in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="9833d-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9833d-119">Der letzte Befehl ruft ein Array mit Wiederherstellungspunkten für das Element in $BackupItem ab und speichert sie dann in $RP Variable.</span><span class="sxs-lookup"><span data-stu-id="9833d-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="9833d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9833d-120">PARAMETERS</span></span>

### <span data-ttu-id="9833d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9833d-121">-DefaultProfile</span></span>

<span data-ttu-id="9833d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9833d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9833d-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9833d-123">-EndDate</span></span>

<span data-ttu-id="9833d-124">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9833d-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="9833d-125">-Item</span><span class="sxs-lookup"><span data-stu-id="9833d-125">-Item</span></span>

<span data-ttu-id="9833d-126">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="9833d-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9833d-127">Verwenden Sie zum Abrufen **eines AzureRmRecoveryServicesBackupItem-Objekts** **das Cmdlet "Get-AzRecoveryServicesBackupItem".**</span><span class="sxs-lookup"><span data-stu-id="9833d-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="9833d-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="9833d-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="9833d-129">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den KeyVault Key für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9833d-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="9833d-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9833d-130">-RecoveryPointId</span></span>

<span data-ttu-id="9833d-131">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="9833d-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="9833d-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9833d-132">-StartDate</span></span>

<span data-ttu-id="9833d-133">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9833d-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="9833d-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9833d-134">-VaultId</span></span>

<span data-ttu-id="9833d-135">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="9833d-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9833d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9833d-136">CommonParameters</span></span>
<span data-ttu-id="9833d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9833d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9833d-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9833d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9833d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9833d-139">INPUTS</span></span>

### <span data-ttu-id="9833d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="9833d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="9833d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9833d-141">System.String</span></span>

## <span data-ttu-id="9833d-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9833d-142">OUTPUTS</span></span>

### <span data-ttu-id="9833d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9833d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="9833d-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9833d-144">NOTES</span></span>

## <span data-ttu-id="9833d-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9833d-145">RELATED LINKS</span></span>

[<span data-ttu-id="9833d-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9833d-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9833d-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9833d-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
