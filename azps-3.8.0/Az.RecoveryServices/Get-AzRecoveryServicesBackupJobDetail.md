---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995589"
---
# <span data-ttu-id="0b1dd-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="0b1dd-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="0b1dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b1dd-102">SYNOPSIS</span></span>

<span data-ttu-id="0b1dd-103">Ruft Details für einen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="0b1dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b1dd-104">SYNTAX</span></span>

### <span data-ttu-id="0b1dd-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b1dd-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1dd-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="0b1dd-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b1dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b1dd-107">DESCRIPTION</span></span>

<span data-ttu-id="0b1dd-108">Das Cmdlet " **Get-AzRecoveryServicesBackupJobDetail** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="0b1dd-109">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="0b1dd-110">Warnung: **Get-AzRecoveryServicesBackupJobDetails-** Alias wird in einer zukünftigen Version von Breaking Change entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="0b1dd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b1dd-111">EXAMPLES</span></span>

### <span data-ttu-id="0b1dd-112">Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge</span><span class="sxs-lookup"><span data-stu-id="0b1dd-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="0b1dd-113">Der erste Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="0b1dd-114">Der zweite Befehl ruft die Auftragsdetails für die fehlgeschlagenen Aufträge in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="0b1dd-115">Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="0b1dd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b1dd-116">PARAMETERS</span></span>

### <span data-ttu-id="0b1dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1dd-117">-DefaultProfile</span></span>

<span data-ttu-id="0b1dd-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b1dd-119">-Job</span><span class="sxs-lookup"><span data-stu-id="0b1dd-119">-Job</span></span>

<span data-ttu-id="0b1dd-120">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-120">Specifies the job to get.</span></span>
<span data-ttu-id="0b1dd-121">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupJob** , um ein **BackupJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="0b1dd-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="0b1dd-122">-JobId</span></span>

<span data-ttu-id="0b1dd-123">Gibt die ID eines Backup-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="0b1dd-124">Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="0b1dd-125">-Tresor</span><span class="sxs-lookup"><span data-stu-id="0b1dd-125">-VaultId</span></span>

<span data-ttu-id="0b1dd-126">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="0b1dd-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0b1dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1dd-127">CommonParameters</span></span>
<span data-ttu-id="0b1dd-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b1dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1dd-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b1dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1dd-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b1dd-130">INPUTS</span></span>

### <span data-ttu-id="0b1dd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0b1dd-131">System.String</span></span>

## <span data-ttu-id="0b1dd-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b1dd-132">OUTPUTS</span></span>

### <span data-ttu-id="0b1dd-133">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0b1dd-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0b1dd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b1dd-134">NOTES</span></span>

## <span data-ttu-id="0b1dd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b1dd-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b1dd-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0b1dd-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
