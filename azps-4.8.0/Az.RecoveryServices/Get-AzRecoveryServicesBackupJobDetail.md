---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009583"
---
# <span data-ttu-id="d1367-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="d1367-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="d1367-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1367-102">SYNOPSIS</span></span>

<span data-ttu-id="d1367-103">Ruft Details für einen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="d1367-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="d1367-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1367-104">SYNTAX</span></span>

### <span data-ttu-id="d1367-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1367-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1367-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="d1367-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1367-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1367-107">DESCRIPTION</span></span>

<span data-ttu-id="d1367-108">Das Cmdlet " **Get-AzRecoveryServicesBackupJobDetail** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="d1367-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="d1367-109">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="d1367-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="d1367-110">Warnung: **Get-AzRecoveryServicesBackupJobDetails-** Alias wird in einer zukünftigen Version von Breaking Change entfernt.</span><span class="sxs-lookup"><span data-stu-id="d1367-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="d1367-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1367-111">EXAMPLES</span></span>

### <span data-ttu-id="d1367-112">Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge</span><span class="sxs-lookup"><span data-stu-id="d1367-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="d1367-113">Der erste Befehl ruft den entsprechenden Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="d1367-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="d1367-114">Der zweite Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.</span><span class="sxs-lookup"><span data-stu-id="d1367-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="d1367-115">Der dritte Befehl ruft die Auftragsdetails für den ersten fehlerhaften Auftrag in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="d1367-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="d1367-116">Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="d1367-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="d1367-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1367-117">PARAMETERS</span></span>

### <span data-ttu-id="d1367-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1367-118">-DefaultProfile</span></span>

<span data-ttu-id="d1367-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1367-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1367-120">-Job</span><span class="sxs-lookup"><span data-stu-id="d1367-120">-Job</span></span>

<span data-ttu-id="d1367-121">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d1367-121">Specifies the job to get.</span></span>
<span data-ttu-id="d1367-122">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupJob** , um ein **BackupJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1367-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="d1367-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="d1367-123">-JobId</span></span>

<span data-ttu-id="d1367-124">Gibt die ID eines Backup-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="d1367-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="d1367-125">Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d1367-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="d1367-126">-Tresor</span><span class="sxs-lookup"><span data-stu-id="d1367-126">-VaultId</span></span>

<span data-ttu-id="d1367-127">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="d1367-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d1367-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1367-128">CommonParameters</span></span>
<span data-ttu-id="d1367-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1367-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1367-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1367-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1367-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1367-131">INPUTS</span></span>

### <span data-ttu-id="d1367-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1367-132">System.String</span></span>

## <span data-ttu-id="d1367-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1367-133">OUTPUTS</span></span>

### <span data-ttu-id="d1367-134">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d1367-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d1367-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1367-135">NOTES</span></span>

## <span data-ttu-id="d1367-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1367-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1367-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d1367-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
