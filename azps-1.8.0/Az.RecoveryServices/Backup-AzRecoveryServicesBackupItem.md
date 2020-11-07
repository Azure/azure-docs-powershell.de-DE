---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 58a4ae793a221a693ffb91c03f024292d364666b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659969"
---
# <span data-ttu-id="65744-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65744-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="65744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65744-102">SYNOPSIS</span></span>
<span data-ttu-id="65744-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="65744-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="65744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65744-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65744-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65744-105">DESCRIPTION</span></span>
<span data-ttu-id="65744-106">Das Cmdlet **Backup-AzRecoveryServicesBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="65744-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="65744-107">Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="65744-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="65744-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="65744-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="65744-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65744-109">EXAMPLES</span></span>

### <span data-ttu-id="65744-110">Beispiel 1: Starten einer Sicherung für ein Sicherungselement</span><span class="sxs-lookup"><span data-stu-id="65744-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="65744-111">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM mit dem Namen pstestv2vm1 ab und speichert ihn dann in der $NamedContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="65744-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="65744-112">Der zweite Befehl ruft das Sicherungselement ab, das dem Container in $NamedContainer entspricht, und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="65744-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="65744-113">Der letzte Befehl löst den Sicherungsauftrag für das Sicherungselement in $Item aus.</span><span class="sxs-lookup"><span data-stu-id="65744-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="65744-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="65744-114">PARAMETERS</span></span>

### <span data-ttu-id="65744-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="65744-115">-BackupType</span></span>
<span data-ttu-id="65744-116">Art der durchzuführenden Sicherung</span><span class="sxs-lookup"><span data-stu-id="65744-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65744-117">-DefaultProfile</span></span>
<span data-ttu-id="65744-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65744-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65744-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="65744-119">-EnableCompression</span></span>
<span data-ttu-id="65744-120">Wenn die Aktivierung der Komprimierung erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="65744-120">If enabling compression is required</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65744-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="65744-121">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="65744-122">Gibt eine Ablaufzeit als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="65744-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65744-123">-Item</span><span class="sxs-lookup"><span data-stu-id="65744-123">-Item</span></span>
<span data-ttu-id="65744-124">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="65744-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65744-125">-Tresor</span><span class="sxs-lookup"><span data-stu-id="65744-125">-VaultId</span></span>
<span data-ttu-id="65744-126">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="65744-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="65744-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65744-127">-Confirm</span></span>
<span data-ttu-id="65744-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65744-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65744-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65744-129">-WhatIf</span></span>
<span data-ttu-id="65744-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65744-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65744-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65744-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65744-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65744-132">CommonParameters</span></span>
<span data-ttu-id="65744-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65744-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65744-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65744-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65744-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65744-135">INPUTS</span></span>

### <span data-ttu-id="65744-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="65744-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="65744-137">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65744-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65744-138">System. String</span><span class="sxs-lookup"><span data-stu-id="65744-138">System.String</span></span>

## <span data-ttu-id="65744-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65744-139">OUTPUTS</span></span>

### <span data-ttu-id="65744-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="65744-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="65744-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="65744-141">NOTES</span></span>

## <span data-ttu-id="65744-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65744-142">RELATED LINKS</span></span>

[<span data-ttu-id="65744-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="65744-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="65744-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65744-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="65744-145">Wiederherstellen – AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65744-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


