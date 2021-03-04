---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c7b213fd041718de1f4f8a6c21979a6c0e7af964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934728"
---
# <span data-ttu-id="f502c-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="f502c-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="f502c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f502c-102">SYNOPSIS</span></span>

<span data-ttu-id="f502c-103">Ruft Details für einen Sicherungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="f502c-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="f502c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f502c-104">SYNTAX</span></span>

### <span data-ttu-id="f502c-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f502c-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f502c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="f502c-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f502c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f502c-107">DESCRIPTION</span></span>

<span data-ttu-id="f502c-108">Das **Get-AzRecoveryServicesBackupJobDetail-Cmdlet** ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="f502c-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="f502c-109">Legen Sie den Tresorkontext mithilfe des -VaultId-Parameters ein.</span><span class="sxs-lookup"><span data-stu-id="f502c-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="f502c-110">Warnung: **Der Alias "Get-AzRecoveryServicesBackupJobDetails"** wird in einer zukünftigen Änderungsversion entfernt.</span><span class="sxs-lookup"><span data-stu-id="f502c-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="f502c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f502c-111">EXAMPLES</span></span>

### <span data-ttu-id="f502c-112">Beispiel 1: Erhalten von Details zu Sicherungsaufträgen für fehlgeschlagene Aufträge</span><span class="sxs-lookup"><span data-stu-id="f502c-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="f502c-113">Der erste Befehl ruft den relevanten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="f502c-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="f502c-114">Der zweite Befehl ruft ein Array fehlgeschlagener Aufträge im Tresor ab und speichert sie dann im $Jobs Matrix.</span><span class="sxs-lookup"><span data-stu-id="f502c-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="f502c-115">Der dritte Befehl ruft die Auftragsdetails für den ersten fehlgeschlagenen Auftrag in $Jobs ab und speichert sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="f502c-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="f502c-116">Der letzte Befehl zeigt Fehlerdetails für die fehlgeschlagenen Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="f502c-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="f502c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f502c-117">PARAMETERS</span></span>

### <span data-ttu-id="f502c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f502c-118">-DefaultProfile</span></span>

<span data-ttu-id="f502c-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f502c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f502c-120">-Job</span><span class="sxs-lookup"><span data-stu-id="f502c-120">-Job</span></span>

<span data-ttu-id="f502c-121">Gibt den zu erhaltenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f502c-121">Specifies the job to get.</span></span>
<span data-ttu-id="f502c-122">Zum Abrufen eines **BackupJob-Objekts** verwenden Sie **das Get-AzRecoveryServicesBackupJob-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="f502c-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="f502c-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="f502c-123">-JobId</span></span>

<span data-ttu-id="f502c-124">Gibt die ID eines Sicherungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="f502c-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="f502c-125">Die ID ist die JobId-Eigenschaft eines **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="f502c-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="f502c-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f502c-126">-VaultId</span></span>

<span data-ttu-id="f502c-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="f502c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f502c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f502c-128">CommonParameters</span></span>
<span data-ttu-id="f502c-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f502c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f502c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f502c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f502c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f502c-131">INPUTS</span></span>

### <span data-ttu-id="f502c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f502c-132">System.String</span></span>

## <span data-ttu-id="f502c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f502c-133">OUTPUTS</span></span>

### <span data-ttu-id="f502c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="f502c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f502c-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f502c-135">NOTES</span></span>

## <span data-ttu-id="f502c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f502c-136">RELATED LINKS</span></span>

[<span data-ttu-id="f502c-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f502c-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
