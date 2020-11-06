---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: c4678cfb29d366c5ad855ea86313ea36be35e10b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496942"
---
# <span data-ttu-id="58087-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="58087-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="58087-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58087-102">SYNOPSIS</span></span>
<span data-ttu-id="58087-103">Wartet, bis ein Backup-Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="58087-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58087-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58087-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58087-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58087-105">DESCRIPTION</span></span>
<span data-ttu-id="58087-106">Das **Wait-AzureRmRecoveryServicesBackupJob-** Cmdlet wartet darauf, dass ein Azure Backup-Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="58087-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="58087-107">Backup-Aufträge können viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="58087-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="58087-108">Wenn Sie einen Sicherungsauftrag als Teil eines Skripts ausführen, möchten Sie möglicherweise erzwingen, dass das Skript auf den Abschluss des Auftrags wartet, bevor es mit anderen Aufgaben fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="58087-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="58087-109">Ein Skript, das dieses Cmdlet enthält, kann einfacher als eins sein, das den Sicherungsdienst für den Auftragsstatus abruft.</span><span class="sxs-lookup"><span data-stu-id="58087-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="58087-110">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="58087-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="58087-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58087-111">EXAMPLES</span></span>

### <span data-ttu-id="58087-112">Beispiel 1: warten Sie, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="58087-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="58087-113">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="58087-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="58087-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="58087-114">PARAMETERS</span></span>

### <span data-ttu-id="58087-115">-Job</span><span class="sxs-lookup"><span data-stu-id="58087-115">-Job</span></span>
<span data-ttu-id="58087-116">Gibt den Auftrag an, auf den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58087-116">Specifies the job to wait for.</span></span>
<span data-ttu-id="58087-117">Verwenden Sie das Get-AzureRmRecoveryServicesBackupJob-Cmdlet, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="58087-117">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58087-118">-Timeout</span><span class="sxs-lookup"><span data-stu-id="58087-118">-Timeout</span></span>
<span data-ttu-id="58087-119">Gibt die maximale Zeitdauer in Sekunden an, die dieses Cmdlet auf den Abschluss des Auftrags wartet.</span><span class="sxs-lookup"><span data-stu-id="58087-119">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="58087-120">Es wird empfohlen, einen Timeoutwert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="58087-120">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58087-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58087-121">-DefaultProfile</span></span>
<span data-ttu-id="58087-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58087-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58087-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58087-123">CommonParameters</span></span>
<span data-ttu-id="58087-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58087-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58087-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58087-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58087-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58087-126">INPUTS</span></span>

### <span data-ttu-id="58087-127">Objekt</span><span class="sxs-lookup"><span data-stu-id="58087-127">Object</span></span>
<span data-ttu-id="58087-128">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' Object ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58087-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="58087-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58087-129">OUTPUTS</span></span>

### <span data-ttu-id="58087-130">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="58087-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="58087-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="58087-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="58087-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="58087-132">NOTES</span></span>

## <span data-ttu-id="58087-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58087-133">RELATED LINKS</span></span>

[<span data-ttu-id="58087-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="58087-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


