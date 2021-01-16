---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299851"
---
# <span data-ttu-id="5e17c-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="5e17c-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="5e17c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e17c-102">SYNOPSIS</span></span>

<span data-ttu-id="5e17c-103">Ruft Details für einen Sicherungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5e17c-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="5e17c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e17c-104">SYNTAX</span></span>

### <span data-ttu-id="5e17c-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e17c-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e17c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="5e17c-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e17c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e17c-107">DESCRIPTION</span></span>

<span data-ttu-id="5e17c-108">Das **Cmdlet "Get-AzRecoveryServicesBackupJobDetail"** ruft Details zum Azure -Sicherungsauftrag für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5e17c-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="5e17c-109">Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.</span><span class="sxs-lookup"><span data-stu-id="5e17c-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="5e17c-110">Warnung: **Der Alias "Get-AzRecoveryServicesBackupJobDetails"** wird in einer zukünftigen Änderungsversion entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e17c-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="5e17c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e17c-111">EXAMPLES</span></span>

### <span data-ttu-id="5e17c-112">Beispiel 1: Erhalten von Sicherungsauftragsdetails für fehlgeschlagene Aufträge</span><span class="sxs-lookup"><span data-stu-id="5e17c-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="5e17c-113">Der erste Befehl ruft den relevanten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="5e17c-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="5e17c-114">Der zweite Befehl ruft ein Array mit fehlgeschlagenen Aufträgen im Tresor ab und speichert sie dann im $Jobs Array.</span><span class="sxs-lookup"><span data-stu-id="5e17c-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="5e17c-115">Der dritte Befehl ruft die Auftragsdetails für den ersten fehlgeschlagenen Auftrag in $Jobs ab und speichert sie dann in der $JobDetails Variable.</span><span class="sxs-lookup"><span data-stu-id="5e17c-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="5e17c-116">Der letzte Befehl zeigt Fehlerdetails für die fehlgeschlagenen Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="5e17c-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="5e17c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e17c-117">PARAMETERS</span></span>

### <span data-ttu-id="5e17c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e17c-118">-DefaultProfile</span></span>

<span data-ttu-id="5e17c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e17c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e17c-120">-Job</span><span class="sxs-lookup"><span data-stu-id="5e17c-120">-Job</span></span>

<span data-ttu-id="5e17c-121">Gibt den zu erhaltenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="5e17c-121">Specifies the job to get.</span></span>
<span data-ttu-id="5e17c-122">Verwenden Sie das Cmdlet **"Get-AzRecoveryServicesBackupJob",** um ein **"BackupJob"-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e17c-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="5e17c-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="5e17c-123">-JobId</span></span>

<span data-ttu-id="5e17c-124">Gibt die ID eines Sicherungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="5e17c-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="5e17c-125">Die ID ist die "JobId"-Eigenschaft eines **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="5e17c-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="5e17c-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5e17c-126">-VaultId</span></span>

<span data-ttu-id="5e17c-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="5e17c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5e17c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e17c-128">CommonParameters</span></span>
<span data-ttu-id="5e17c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e17c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e17c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e17c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e17c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e17c-131">INPUTS</span></span>

### <span data-ttu-id="5e17c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5e17c-132">System.String</span></span>

## <span data-ttu-id="5e17c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e17c-133">OUTPUTS</span></span>

### <span data-ttu-id="5e17c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="5e17c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5e17c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e17c-135">NOTES</span></span>

## <span data-ttu-id="5e17c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e17c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e17c-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5e17c-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
