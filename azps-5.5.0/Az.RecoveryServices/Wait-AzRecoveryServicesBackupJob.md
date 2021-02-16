---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151049"
---
# <span data-ttu-id="d4cbd-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d4cbd-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d4cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4cbd-102">SYNOPSIS</span></span>

<span data-ttu-id="d4cbd-103">Wartet auf den Abschluss eines Sicherungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="d4cbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4cbd-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4cbd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4cbd-105">DESCRIPTION</span></span>

<span data-ttu-id="d4cbd-106">Das **Cmdlet "Wait-AzRecoveryServicesBackupJob"** wartet auf den Abschluss eines Azure-Sicherungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="d4cbd-107">Sicherungsaufträge können sehr lange dauern.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="d4cbd-108">Wenn Sie einen Sicherungsauftrag als Teil eines Skripts ausführen, möchten Sie möglicherweise erzwingen, dass das Skript auf den Abschluss des Auftrags wartet, bevor es mit anderen Aufgaben fortgeht.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="d4cbd-109">Ein Skript, das dieses Cmdlet enthält, kann einfacher als das Skript sein, das den Sicherungsdienst nach dem Auftragsstatus abruft.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="d4cbd-110">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="d4cbd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4cbd-111">EXAMPLES</span></span>

### <span data-ttu-id="d4cbd-112">Beispiel 1: Warten auf den Abschluss eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="d4cbd-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="d4cbd-113">Dieses Skript abruft den ersten Auftrag, der derzeit ausgeführt wird, bis der Auftrag abgeschlossen ist oder ein Timeoutzeitraum von einer Stunde abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="d4cbd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4cbd-114">PARAMETERS</span></span>

### <span data-ttu-id="d4cbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cbd-115">-DefaultProfile</span></span>

<span data-ttu-id="d4cbd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4cbd-117">-Job</span><span class="sxs-lookup"><span data-stu-id="d4cbd-117">-Job</span></span>

<span data-ttu-id="d4cbd-118">Gibt den Auftrag an, auf den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="d4cbd-119">Verwenden Sie das Cmdlet **"Get-AzRecoveryServicesBackupJob",** um ein **"BackupJob"-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="d4cbd-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="d4cbd-120">-Timeout</span></span>

<span data-ttu-id="d4cbd-121">Gibt die maximale Zeit (in Sekunden) an, für die dieses Cmdlet auf den Abschluss des Auftrags wartet.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="d4cbd-122">Es wird empfohlen, einen Zeit out-Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="d4cbd-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d4cbd-123">-VaultId</span></span>

<span data-ttu-id="d4cbd-124">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d4cbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cbd-125">CommonParameters</span></span>
<span data-ttu-id="d4cbd-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cbd-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4cbd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cbd-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4cbd-128">INPUTS</span></span>

### <span data-ttu-id="d4cbd-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="d4cbd-129">System.Object</span></span>

### <span data-ttu-id="d4cbd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d4cbd-130">System.String</span></span>

## <span data-ttu-id="d4cbd-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4cbd-131">OUTPUTS</span></span>

### <span data-ttu-id="d4cbd-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="d4cbd-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d4cbd-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d4cbd-133">NOTES</span></span>

## <span data-ttu-id="d4cbd-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d4cbd-134">RELATED LINKS</span></span>

[<span data-ttu-id="d4cbd-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d4cbd-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
