---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178128"
---
# <span data-ttu-id="04fc4-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="04fc4-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="04fc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04fc4-102">SYNOPSIS</span></span>

<span data-ttu-id="04fc4-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="04fc4-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="04fc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04fc4-104">SYNTAX</span></span>

### <span data-ttu-id="04fc4-105">Nofilterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="04fc4-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04fc4-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="04fc4-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04fc4-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="04fc4-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04fc4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04fc4-108">DESCRIPTION</span></span>

<span data-ttu-id="04fc4-109">Das Cmdlet " **Get-AzRecoveryServicesBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="04fc4-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="04fc4-110">Nachdem ein Element gesichert wurde, verfügt ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt über einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="04fc4-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="04fc4-111">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="04fc4-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="04fc4-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04fc4-112">EXAMPLES</span></span>

### <span data-ttu-id="04fc4-113">Beispiel 1: Abrufen von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="04fc4-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="04fc4-114">Mit dem ersten Befehl wird Vault-Objekt auf Grundlage von vaultname abgerufen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="04fc4-115">Der zweite Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="04fc4-116">Der dritte Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="04fc4-117">Der vierte Befehl ruft AzureVM-Sicherungs Container ab und speichert Sie in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="04fc4-118">Der fünfte Befehl ruft das Sicherungselement auf Grundlage von workloadtype, Vault-Funktion ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="04fc4-119">Der letzte Befehl ruft ein Array von Wiederherstellungspunkten für das Element in $BackupItem ab und speichert Sie dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="04fc4-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="04fc4-120">PARAMETERS</span></span>

### <span data-ttu-id="04fc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fc4-121">-DefaultProfile</span></span>

<span data-ttu-id="04fc4-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04fc4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04fc4-123">-Enddate</span><span class="sxs-lookup"><span data-stu-id="04fc4-123">-EndDate</span></span>

<span data-ttu-id="04fc4-124">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="04fc4-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="04fc4-125">-Item</span><span class="sxs-lookup"><span data-stu-id="04fc4-125">-Item</span></span>

<span data-ttu-id="04fc4-126">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="04fc4-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="04fc4-127">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupItem** , um ein **AzureRmRecoveryServicesBackupItem** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="04fc4-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="04fc4-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="04fc4-129">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den keyvault-Schlüssel für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="04fc4-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="04fc4-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="04fc4-130">-RecoveryPointId</span></span>

<span data-ttu-id="04fc4-131">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="04fc4-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="04fc4-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="04fc4-132">-StartDate</span></span>

<span data-ttu-id="04fc4-133">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="04fc4-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="04fc4-134">-Tresor</span><span class="sxs-lookup"><span data-stu-id="04fc4-134">-VaultId</span></span>

<span data-ttu-id="04fc4-135">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="04fc4-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="04fc4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fc4-136">CommonParameters</span></span>
<span data-ttu-id="04fc4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04fc4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fc4-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04fc4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fc4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04fc4-139">INPUTS</span></span>

### <span data-ttu-id="04fc4-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="04fc4-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="04fc4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="04fc4-141">System.String</span></span>

## <span data-ttu-id="04fc4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04fc4-142">OUTPUTS</span></span>

### <span data-ttu-id="04fc4-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="04fc4-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="04fc4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="04fc4-144">NOTES</span></span>

## <span data-ttu-id="04fc4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04fc4-145">RELATED LINKS</span></span>

[<span data-ttu-id="04fc4-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="04fc4-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="04fc4-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="04fc4-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
