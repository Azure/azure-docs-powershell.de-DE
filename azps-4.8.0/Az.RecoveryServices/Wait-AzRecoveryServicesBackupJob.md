---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174448"
---
# <span data-ttu-id="b62d1-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b62d1-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="b62d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b62d1-102">SYNOPSIS</span></span>

<span data-ttu-id="b62d1-103">Wartet, bis ein Backup-Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b62d1-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="b62d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62d1-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b62d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b62d1-105">DESCRIPTION</span></span>

<span data-ttu-id="b62d1-106">Das **Wait-AzRecoveryServicesBackupJob-** Cmdlet wartet darauf, dass ein Azure Backup-Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b62d1-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="b62d1-107">Backup-Aufträge können viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="b62d1-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="b62d1-108">Wenn Sie einen Sicherungsauftrag als Teil eines Skripts ausführen, möchten Sie möglicherweise erzwingen, dass das Skript auf den Abschluss des Auftrags wartet, bevor es mit anderen Aufgaben fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b62d1-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="b62d1-109">Ein Skript, das dieses Cmdlet enthält, kann einfacher als eins sein, das den Sicherungsdienst für den Auftragsstatus abruft.</span><span class="sxs-lookup"><span data-stu-id="b62d1-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="b62d1-110">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="b62d1-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b62d1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b62d1-111">EXAMPLES</span></span>

### <span data-ttu-id="b62d1-112">Beispiel 1: warten Sie, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b62d1-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="b62d1-113">Dieses Skript ruft den ersten Auftrag ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist oder ein Timeoutzeitraum von 1 Stunde abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b62d1-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="b62d1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62d1-114">PARAMETERS</span></span>

### <span data-ttu-id="b62d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62d1-115">-DefaultProfile</span></span>

<span data-ttu-id="b62d1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b62d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62d1-117">-Job</span><span class="sxs-lookup"><span data-stu-id="b62d1-117">-Job</span></span>

<span data-ttu-id="b62d1-118">Gibt den Auftrag an, auf den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b62d1-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="b62d1-119">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupJob** , um ein **BackupJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b62d1-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="b62d1-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="b62d1-120">-Timeout</span></span>

<span data-ttu-id="b62d1-121">Gibt die maximale Zeitdauer in Sekunden an, die dieses Cmdlet auf den Abschluss des Auftrags wartet.</span><span class="sxs-lookup"><span data-stu-id="b62d1-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="b62d1-122">Es wird empfohlen, einen Timeoutwert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b62d1-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="b62d1-123">-Tresor</span><span class="sxs-lookup"><span data-stu-id="b62d1-123">-VaultId</span></span>

<span data-ttu-id="b62d1-124">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="b62d1-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b62d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62d1-125">CommonParameters</span></span>
<span data-ttu-id="b62d1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62d1-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b62d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62d1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b62d1-128">INPUTS</span></span>

### <span data-ttu-id="b62d1-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="b62d1-129">System.Object</span></span>

### <span data-ttu-id="b62d1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b62d1-130">System.String</span></span>

## <span data-ttu-id="b62d1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b62d1-131">OUTPUTS</span></span>

### <span data-ttu-id="b62d1-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b62d1-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b62d1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b62d1-133">NOTES</span></span>

## <span data-ttu-id="b62d1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b62d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="b62d1-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b62d1-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
