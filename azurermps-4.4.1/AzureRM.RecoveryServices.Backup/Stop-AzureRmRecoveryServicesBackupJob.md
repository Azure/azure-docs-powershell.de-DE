---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503990"
---
# <span data-ttu-id="8c8ee-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c8ee-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="8c8ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8ee-103">Bricht einen ausgeführten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c8ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c8ee-104">SYNTAX</span></span>

### <span data-ttu-id="8c8ee-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c8ee-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="8c8ee-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c8ee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="8c8ee-108">Mit dem Cmdlet " **Stop-AzureRmRecoveryServicesBackupJob** " wird ein vorhandener Azure Backup-Auftrag abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="8c8ee-109">Verwenden Sie dieses Cmdlet, um einen Auftrag zu beenden, der zu lange dauert und andere Aktivitäten blockiert.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="8c8ee-110">Sie können nur Sicherungs-und Wiederherstellungsauftrags Typen stornieren.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="8c8ee-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8c8ee-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c8ee-112">EXAMPLES</span></span>

### <span data-ttu-id="8c8ee-113">Beispiel 1: Beenden eines Backup-Auftrags</span><span class="sxs-lookup"><span data-stu-id="8c8ee-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="8c8ee-114">Der erste Befehl ruft einen Sicherungsauftrag ab und speichert den Auftrag dann in der $Job Variablen.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="8c8ee-115">Mit dem letzten Befehl wird der Auftrag beendet, indem die Instanz-ID des Sicherungsauftrags in $Job angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="8c8ee-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8ee-116">PARAMETERS</span></span>

### <span data-ttu-id="8c8ee-117">-Job</span><span class="sxs-lookup"><span data-stu-id="8c8ee-117">-Job</span></span>
<span data-ttu-id="8c8ee-118">Gibt einen Auftrag an, den dieses Cmdlet abbricht.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="8c8ee-119">Verwenden Sie das Get-AzureRmRecoveryServicesBackupJob-Cmdlet, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8ee-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="8c8ee-120">-JobId</span></span>
<span data-ttu-id="8c8ee-121">Gibt die ID des Auftrags an, der abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="8c8ee-122">Die ID ist die InstanceId-Eigenschaft eines **BackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="8c8ee-123">Verwenden Sie Get-AzureRmRecoveryServicesBackupJob, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8ee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8ee-124">-DefaultProfile</span></span>
<span data-ttu-id="8c8ee-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c8ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8ee-126">CommonParameters</span></span>
<span data-ttu-id="8c8ee-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8ee-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8ee-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c8ee-129">INPUTS</span></span>

## <span data-ttu-id="8c8ee-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c8ee-130">OUTPUTS</span></span>

### <span data-ttu-id="8c8ee-131">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8c8ee-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8c8ee-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c8ee-132">NOTES</span></span>

## <span data-ttu-id="8c8ee-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c8ee-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c8ee-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c8ee-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="8c8ee-135">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c8ee-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


