---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166902"
---
# <span data-ttu-id="9e3dd-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e3dd-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="9e3dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e3dd-102">SYNOPSIS</span></span>

<span data-ttu-id="9e3dd-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="9e3dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e3dd-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e3dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e3dd-105">DESCRIPTION</span></span>

<span data-ttu-id="9e3dd-106">Das Cmdlet **Backup-AzRecoveryServicesBackupItem** übernimmt eine Adhoc-Sicherung des geschützten Azure-sicherungselements.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="9e3dd-107">Mithilfe dieses Cmdlets können Sie unmittelbar nach der Aktivierung des Schutzes eine erste Sicherung durchführen oder eine Sicherung starten, wenn eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="9e3dd-108">Dieses Cmdlet kann auch für die benutzerdefinierte Aufbewahrung mit oder ohne Ablaufdatum verwendet werden, um weitere Details zu finden.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="9e3dd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e3dd-109">EXAMPLES</span></span>

### <span data-ttu-id="9e3dd-110">Beispiel 1: Starten einer Sicherung für ein Sicherungselement</span><span class="sxs-lookup"><span data-stu-id="9e3dd-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="9e3dd-111">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM mit dem Namen pstestv2vm1 ab und speichert ihn dann in der $NamedContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="9e3dd-112">Der zweite Befehl ruft das Sicherungselement ab, das dem Container in $NamedContainer entspricht, und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="9e3dd-113">Der letzte Befehl löst den Sicherungsauftrag für das Sicherungselement in $Item aus.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="9e3dd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9e3dd-114">Example 2</span></span>

<span data-ttu-id="9e3dd-115">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="9e3dd-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="9e3dd-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="9e3dd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e3dd-117">PARAMETERS</span></span>

### <span data-ttu-id="9e3dd-118">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="9e3dd-118">-BackupType</span></span>

<span data-ttu-id="9e3dd-119">Art der durchzuführenden Sicherung</span><span class="sxs-lookup"><span data-stu-id="9e3dd-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="9e3dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3dd-120">-DefaultProfile</span></span>

<span data-ttu-id="9e3dd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3dd-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="9e3dd-122">-EnableCompression</span></span>

<span data-ttu-id="9e3dd-123">Wenn die Aktivierung der Komprimierung erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="9e3dd-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="9e3dd-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="9e3dd-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="9e3dd-125">Gibt eine Ablaufzeit für den Wiederherstellungspunkt als DateTime-Objekt an, wenn kein Wert angegeben wird, der den Standardwert 30 Tage hat.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="9e3dd-126">Anwendbar auf VM, SQL (nur Copy-Full-Backup-Typ), AFS-Backup-Elemente.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="9e3dd-127">-Item</span><span class="sxs-lookup"><span data-stu-id="9e3dd-127">-Item</span></span>

<span data-ttu-id="9e3dd-128">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="9e3dd-129">-Tresor</span><span class="sxs-lookup"><span data-stu-id="9e3dd-129">-VaultId</span></span>

<span data-ttu-id="9e3dd-130">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="9e3dd-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9e3dd-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e3dd-131">-Confirm</span></span>

<span data-ttu-id="9e3dd-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3dd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3dd-133">-WhatIf</span></span>

<span data-ttu-id="9e3dd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="9e3dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3dd-135">CommonParameters</span></span>
<span data-ttu-id="9e3dd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3dd-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3dd-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e3dd-138">INPUTS</span></span>

### <span data-ttu-id="9e3dd-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="9e3dd-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="9e3dd-140">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e3dd-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e3dd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3dd-141">System.String</span></span>

## <span data-ttu-id="9e3dd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e3dd-142">OUTPUTS</span></span>

### <span data-ttu-id="9e3dd-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9e3dd-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9e3dd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e3dd-144">NOTES</span></span>

## <span data-ttu-id="9e3dd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e3dd-145">RELATED LINKS</span></span>

[<span data-ttu-id="9e3dd-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9e3dd-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9e3dd-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e3dd-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="9e3dd-148">Wiederherstellen – AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e3dd-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
