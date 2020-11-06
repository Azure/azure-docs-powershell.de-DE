---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478350"
---
# <span data-ttu-id="9fb90-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9fb90-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="9fb90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fb90-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb90-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="9fb90-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fb90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fb90-104">SYNTAX</span></span>

### <span data-ttu-id="9fb90-105">Nofilterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fb90-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb90-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="9fb90-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb90-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9fb90-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fb90-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fb90-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb90-109">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="9fb90-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9fb90-110">Nachdem ein Element gesichert wurde, verfügt ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt über einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="9fb90-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="9fb90-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fb90-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9fb90-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fb90-112">EXAMPLES</span></span>

### <span data-ttu-id="9fb90-113">Beispiel 1: Abrufen von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="9fb90-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="9fb90-114">Der erste Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="9fb90-115">Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="9fb90-116">Der dritte Befehl ruft AzureVM-Sicherungs Container ab und speichert Sie in der $Containers-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="9fb90-117">Der vierte Befehl ruft das Sicherungselement mit dem Namen V2VM ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="9fb90-118">Der letzte Befehl ruft ein Array von Wiederherstellungspunkten für das Element in $BackupItem ab und speichert Sie dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="9fb90-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fb90-119">PARAMETERS</span></span>

### <span data-ttu-id="9fb90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb90-120">-DefaultProfile</span></span>
<span data-ttu-id="9fb90-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fb90-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-122">-Enddate</span><span class="sxs-lookup"><span data-stu-id="9fb90-122">-EndDate</span></span>
<span data-ttu-id="9fb90-123">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9fb90-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-124">-Item</span><span class="sxs-lookup"><span data-stu-id="9fb90-124">-Item</span></span>
<span data-ttu-id="9fb90-125">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="9fb90-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9fb90-126">Verwenden Sie das Get-AzureRmRecoveryServicesBackupItem-Cmdlet, um ein **AzureRmRecoveryServicesBackupItem** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fb90-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="9fb90-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="9fb90-128">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den keyvault-Schlüssel für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9fb90-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9fb90-129">-RecoveryPointId</span></span>
<span data-ttu-id="9fb90-130">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="9fb90-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9fb90-131">-StartDate</span></span>
<span data-ttu-id="9fb90-132">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9fb90-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb90-133">CommonParameters</span></span>
<span data-ttu-id="9fb90-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb90-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb90-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb90-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fb90-136">INPUTS</span></span>

### <span data-ttu-id="9fb90-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="9fb90-137">ItemBase</span></span>
<span data-ttu-id="9fb90-138">Der Parameter "Item" akzeptiert den Wert vom Typ "ItemBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fb90-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="9fb90-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fb90-139">OUTPUTS</span></span>

### <span data-ttu-id="9fb90-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9fb90-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="9fb90-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="9fb90-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="9fb90-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fb90-142">NOTES</span></span>

## <span data-ttu-id="9fb90-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fb90-143">RELATED LINKS</span></span>

[<span data-ttu-id="9fb90-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9fb90-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9fb90-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9fb90-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


