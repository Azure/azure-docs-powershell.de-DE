---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502510"
---
# <span data-ttu-id="bfdbc-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bfdbc-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="bfdbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdbc-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfdbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfdbc-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfdbc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfdbc-105">DESCRIPTION</span></span>
<span data-ttu-id="bfdbc-106">Das Cmdlet **Backup-AzureRmRecoveryServicesBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="bfdbc-107">Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="bfdbc-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bfdbc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfdbc-109">EXAMPLES</span></span>

### <span data-ttu-id="bfdbc-110">Beispiel 1: Starten einer Sicherung für ein Sicherungselement</span><span class="sxs-lookup"><span data-stu-id="bfdbc-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="bfdbc-111">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM mit dem Namen pstestv2vm1 ab und speichert ihn dann in der $NamedContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="bfdbc-112">Der zweite Befehl ruft das Sicherungselement ab, das dem Container in $NamedContainer entspricht, und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="bfdbc-113">Der letzte Befehl löst den Sicherungsauftrag für das Sicherungselement in $Item aus.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="bfdbc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfdbc-114">PARAMETERS</span></span>

### <span data-ttu-id="bfdbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdbc-115">-DefaultProfile</span></span>
<span data-ttu-id="bfdbc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfdbc-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="bfdbc-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="bfdbc-118">Gibt eine Ablaufzeit als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdbc-119">-Item</span><span class="sxs-lookup"><span data-stu-id="bfdbc-119">-Item</span></span>
<span data-ttu-id="bfdbc-120">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdbc-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bfdbc-121">-Confirm</span></span>
<span data-ttu-id="bfdbc-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfdbc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfdbc-123">-WhatIf</span></span>
<span data-ttu-id="bfdbc-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfdbc-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfdbc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdbc-126">CommonParameters</span></span>
<span data-ttu-id="bfdbc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdbc-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfdbc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdbc-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfdbc-129">INPUTS</span></span>

### <span data-ttu-id="bfdbc-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="bfdbc-130">DateTime</span></span>
<span data-ttu-id="bfdbc-131">Der Parameter "ExpiryDateTimeUTC" akzeptiert den Wert vom Typ "DateTime" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-131">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="bfdbc-132">ItemBase</span><span class="sxs-lookup"><span data-stu-id="bfdbc-132">ItemBase</span></span>
<span data-ttu-id="bfdbc-133">Der Parameter "Item" akzeptiert den Wert vom Typ "ItemBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-133">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="bfdbc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfdbc-134">OUTPUTS</span></span>

### <span data-ttu-id="bfdbc-135">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="bfdbc-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bfdbc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfdbc-136">NOTES</span></span>

## <span data-ttu-id="bfdbc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfdbc-137">RELATED LINKS</span></span>

[<span data-ttu-id="bfdbc-138">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bfdbc-138">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="bfdbc-139">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bfdbc-139">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="bfdbc-140">Wiederherstellen – AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bfdbc-140">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


