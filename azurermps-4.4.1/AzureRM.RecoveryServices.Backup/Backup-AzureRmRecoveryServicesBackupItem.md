---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663870"
---
# <span data-ttu-id="5247c-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5247c-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5247c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5247c-102">SYNOPSIS</span></span>
<span data-ttu-id="5247c-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="5247c-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5247c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5247c-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5247c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5247c-105">DESCRIPTION</span></span>
<span data-ttu-id="5247c-106">Das Cmdlet **Backup-AzureRmRecoveryServicesBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="5247c-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="5247c-107">Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5247c-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="5247c-108">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5247c-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5247c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5247c-109">EXAMPLES</span></span>

### <span data-ttu-id="5247c-110">Beispiel 1: Starten einer Sicherung für ein Sicherungselement</span><span class="sxs-lookup"><span data-stu-id="5247c-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="5247c-111">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM mit dem Namen pstestv2vm1 ab und speichert ihn dann in der $NamedContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="5247c-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="5247c-112">Der zweite Befehl ruft das Sicherungselement ab, das dem Container in $NamedContainer entspricht, und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="5247c-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="5247c-113">Der letzte Befehl löst den Sicherungsauftrag für das Sicherungselement in $Item aus.</span><span class="sxs-lookup"><span data-stu-id="5247c-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="5247c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5247c-114">PARAMETERS</span></span>

### <span data-ttu-id="5247c-115">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="5247c-115">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="5247c-116">Gibt eine Ablaufzeit als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5247c-116">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="5247c-117">-Item</span><span class="sxs-lookup"><span data-stu-id="5247c-117">-Item</span></span>
<span data-ttu-id="5247c-118">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="5247c-118">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="5247c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5247c-119">-DefaultProfile</span></span>
<span data-ttu-id="5247c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5247c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5247c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5247c-121">CommonParameters</span></span>
<span data-ttu-id="5247c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5247c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5247c-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5247c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5247c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5247c-124">INPUTS</span></span>

### <span data-ttu-id="5247c-125">DateTime</span><span class="sxs-lookup"><span data-stu-id="5247c-125">DateTime</span></span>
<span data-ttu-id="5247c-126">Der Parameter "ExpiryDateTimeUTC" akzeptiert den Wert vom Typ "DateTime" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5247c-126">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="5247c-127">ItemBase</span><span class="sxs-lookup"><span data-stu-id="5247c-127">ItemBase</span></span>
<span data-ttu-id="5247c-128">Der Parameter "Item" akzeptiert den Wert vom Typ "ItemBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5247c-128">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="5247c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5247c-129">OUTPUTS</span></span>

### <span data-ttu-id="5247c-130">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5247c-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5247c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5247c-131">NOTES</span></span>

## <span data-ttu-id="5247c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5247c-132">RELATED LINKS</span></span>

[<span data-ttu-id="5247c-133">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5247c-133">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="5247c-134">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5247c-134">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5247c-135">Wiederherstellen – AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5247c-135">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


