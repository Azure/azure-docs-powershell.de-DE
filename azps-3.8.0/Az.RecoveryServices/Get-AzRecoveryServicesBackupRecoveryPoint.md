---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 2703ca4684d3bf59f5b3fd47415897a2c80f6c3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004936"
---
# <span data-ttu-id="1040f-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1040f-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="1040f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1040f-102">SYNOPSIS</span></span>

<span data-ttu-id="1040f-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="1040f-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="1040f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1040f-104">SYNTAX</span></span>

### <span data-ttu-id="1040f-105">Nofilterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="1040f-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1040f-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="1040f-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1040f-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="1040f-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1040f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1040f-108">DESCRIPTION</span></span>

<span data-ttu-id="1040f-109">Das Cmdlet " **Get-AzRecoveryServicesBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="1040f-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="1040f-110">Nachdem ein Element gesichert wurde, verfügt ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt über einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="1040f-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="1040f-111">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="1040f-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="1040f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1040f-112">EXAMPLES</span></span>

### <span data-ttu-id="1040f-113">Beispiel 1: Abrufen von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="1040f-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="1040f-114">Der erste Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1040f-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1040f-115">Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="1040f-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1040f-116">Der dritte Befehl ruft AzureVM-Sicherungs Container ab und speichert Sie in der $Containers-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1040f-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="1040f-117">Der vierte Befehl ruft das Sicherungselement mit dem Namen V2VM ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="1040f-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1040f-118">Der letzte Befehl ruft ein Array von Wiederherstellungspunkten für das Element in $BackupItem ab und speichert Sie dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="1040f-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="1040f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1040f-119">PARAMETERS</span></span>

### <span data-ttu-id="1040f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1040f-120">-DefaultProfile</span></span>

<span data-ttu-id="1040f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1040f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1040f-122">-Enddate</span><span class="sxs-lookup"><span data-stu-id="1040f-122">-EndDate</span></span>

<span data-ttu-id="1040f-123">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="1040f-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="1040f-124">-Item</span><span class="sxs-lookup"><span data-stu-id="1040f-124">-Item</span></span>

<span data-ttu-id="1040f-125">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="1040f-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="1040f-126">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupItem** , um ein **AzureRmRecoveryServicesBackupItem** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1040f-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="1040f-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="1040f-127">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="1040f-128">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den keyvault-Schlüssel für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1040f-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="1040f-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="1040f-129">-RecoveryPointId</span></span>

<span data-ttu-id="1040f-130">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="1040f-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="1040f-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1040f-131">-StartDate</span></span>

<span data-ttu-id="1040f-132">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="1040f-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="1040f-133">-Tresor</span><span class="sxs-lookup"><span data-stu-id="1040f-133">-VaultId</span></span>

<span data-ttu-id="1040f-134">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="1040f-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1040f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1040f-135">CommonParameters</span></span>
<span data-ttu-id="1040f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1040f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1040f-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1040f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1040f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1040f-138">INPUTS</span></span>

### <span data-ttu-id="1040f-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="1040f-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="1040f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1040f-140">System.String</span></span>

## <span data-ttu-id="1040f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1040f-141">OUTPUTS</span></span>

### <span data-ttu-id="1040f-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1040f-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="1040f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1040f-143">NOTES</span></span>

## <span data-ttu-id="1040f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1040f-144">RELATED LINKS</span></span>

[<span data-ttu-id="1040f-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1040f-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="1040f-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1040f-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
