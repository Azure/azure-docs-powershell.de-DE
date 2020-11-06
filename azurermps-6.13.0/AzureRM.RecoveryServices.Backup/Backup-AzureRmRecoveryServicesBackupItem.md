---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482158"
---
# <span data-ttu-id="793b4-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="793b4-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="793b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="793b4-102">SYNOPSIS</span></span>
<span data-ttu-id="793b4-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="793b4-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="793b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="793b4-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="793b4-105">DESCRIPTION</span></span>
<span data-ttu-id="793b4-106">Das Cmdlet **Backup-AzureRmRecoveryServicesBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="793b4-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="793b4-107">Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="793b4-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="793b4-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="793b4-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="793b4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="793b4-109">EXAMPLES</span></span>

### <span data-ttu-id="793b4-110">Beispiel 1: Starten einer Sicherung für ein Sicherungselement</span><span class="sxs-lookup"><span data-stu-id="793b4-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="793b4-111">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM mit dem Namen pstestv2vm1 ab und speichert ihn dann in der $NamedContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="793b4-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="793b4-112">Der zweite Befehl ruft das Sicherungselement ab, das dem Container in $NamedContainer entspricht, und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="793b4-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="793b4-113">Der letzte Befehl löst den Sicherungsauftrag für das Sicherungselement in $Item aus.</span><span class="sxs-lookup"><span data-stu-id="793b4-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="793b4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="793b4-114">PARAMETERS</span></span>

### <span data-ttu-id="793b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793b4-115">-DefaultProfile</span></span>
<span data-ttu-id="793b4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="793b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="793b4-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="793b4-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="793b4-118">Gibt eine Ablaufzeit als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="793b4-118">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="793b4-119">-Item</span><span class="sxs-lookup"><span data-stu-id="793b4-119">-Item</span></span>
<span data-ttu-id="793b4-120">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="793b4-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="793b4-121">-Tresor</span><span class="sxs-lookup"><span data-stu-id="793b4-121">-VaultId</span></span>
<span data-ttu-id="793b4-122">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="793b4-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="793b4-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="793b4-123">-Confirm</span></span>
<span data-ttu-id="793b4-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="793b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793b4-125">-WhatIf</span></span>
<span data-ttu-id="793b4-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="793b4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="793b4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="793b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793b4-128">CommonParameters</span></span>
<span data-ttu-id="793b4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793b4-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="793b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793b4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="793b4-131">INPUTS</span></span>

### <span data-ttu-id="793b4-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="793b4-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="793b4-133">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="793b4-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="793b4-134">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="793b4-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="793b4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="793b4-135">System.String</span></span>
<span data-ttu-id="793b4-136">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="793b4-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="793b4-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="793b4-137">OUTPUTS</span></span>

### <span data-ttu-id="793b4-138">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="793b4-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="793b4-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="793b4-139">NOTES</span></span>

## <span data-ttu-id="793b4-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="793b4-140">RELATED LINKS</span></span>

[<span data-ttu-id="793b4-141">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="793b4-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="793b4-142">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="793b4-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="793b4-143">Wiederherstellen – AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="793b4-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


