---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659898"
---
# <span data-ttu-id="5c851-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5c851-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="5c851-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c851-102">SYNOPSIS</span></span>
<span data-ttu-id="5c851-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="5c851-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="5c851-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c851-104">SYNTAX</span></span>

### <span data-ttu-id="5c851-105">Nofilterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c851-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c851-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="5c851-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c851-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="5c851-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c851-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c851-108">DESCRIPTION</span></span>
<span data-ttu-id="5c851-109">Das Cmdlet " **Get-AzRecoveryServicesBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="5c851-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="5c851-110">Nachdem ein Element gesichert wurde, verfügt ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt über einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="5c851-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="5c851-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c851-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5c851-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c851-112">EXAMPLES</span></span>

### <span data-ttu-id="5c851-113">Beispiel 1: Abrufen von Wiederherstellungspunkten aus der letzten Woche für ein Element</span><span class="sxs-lookup"><span data-stu-id="5c851-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="5c851-114">Der erste Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c851-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5c851-115">Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c851-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5c851-116">Der dritte Befehl ruft AzureVM-Sicherungs Container ab und speichert Sie in der $Containers-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c851-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="5c851-117">Der vierte Befehl ruft das Sicherungselement mit dem Namen V2VM ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c851-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5c851-118">Der letzte Befehl ruft ein Array von Wiederherstellungspunkten für das Element in $BackupItem ab und speichert Sie dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c851-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="5c851-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c851-119">PARAMETERS</span></span>

### <span data-ttu-id="5c851-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c851-120">-DefaultProfile</span></span>
<span data-ttu-id="5c851-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c851-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c851-122">-Enddate</span><span class="sxs-lookup"><span data-stu-id="5c851-122">-EndDate</span></span>
<span data-ttu-id="5c851-123">Gibt das Ende des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="5c851-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="5c851-124">-Item</span><span class="sxs-lookup"><span data-stu-id="5c851-124">-Item</span></span>
<span data-ttu-id="5c851-125">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="5c851-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="5c851-126">Verwenden Sie das Get-AzRecoveryServicesBackupItem-Cmdlet, um ein **AzureRmRecoveryServicesBackupItem** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c851-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="5c851-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="5c851-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="5c851-128">Gibt den Speicherort an, an dem die Eingabedatei heruntergeladen werden soll, um den keyvault-Schlüssel für einen verschlüsselten virtuellen Computer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c851-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="5c851-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="5c851-129">-RecoveryPointId</span></span>
<span data-ttu-id="5c851-130">Gibt die Wiederherstellungspunkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="5c851-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="5c851-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5c851-131">-StartDate</span></span>
<span data-ttu-id="5c851-132">Gibt den Anfang des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="5c851-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="5c851-133">-Tresor</span><span class="sxs-lookup"><span data-stu-id="5c851-133">-VaultId</span></span>
<span data-ttu-id="5c851-134">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="5c851-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5c851-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c851-135">CommonParameters</span></span>
<span data-ttu-id="5c851-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c851-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c851-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c851-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c851-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c851-138">INPUTS</span></span>

### <span data-ttu-id="5c851-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="5c851-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="5c851-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5c851-140">System.String</span></span>

## <span data-ttu-id="5c851-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c851-141">OUTPUTS</span></span>

### <span data-ttu-id="5c851-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5c851-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="5c851-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c851-143">NOTES</span></span>

## <span data-ttu-id="5c851-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c851-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c851-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5c851-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="5c851-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5c851-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


