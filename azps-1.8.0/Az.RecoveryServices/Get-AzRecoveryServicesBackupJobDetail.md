---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659910"
---
# <span data-ttu-id="5ab3a-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="5ab3a-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="5ab3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ab3a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab3a-103">Ruft Details für einen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="5ab3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab3a-104">SYNTAX</span></span>

### <span data-ttu-id="5ab3a-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ab3a-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ab3a-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="5ab3a-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ab3a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ab3a-107">DESCRIPTION</span></span>
<span data-ttu-id="5ab3a-108">Das Cmdlet " **Get-AzRecoveryServicesBackupJobDetail** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="5ab3a-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5ab3a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ab3a-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab3a-111">Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge</span><span class="sxs-lookup"><span data-stu-id="5ab3a-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="5ab3a-112">Der erste Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="5ab3a-113">Der zweite Befehl ruft die Auftragsdetails für die fehlgeschlagenen Aufträge in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="5ab3a-114">Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="5ab3a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab3a-115">PARAMETERS</span></span>

### <span data-ttu-id="5ab3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab3a-116">-DefaultProfile</span></span>
<span data-ttu-id="5ab3a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ab3a-118">-Job</span><span class="sxs-lookup"><span data-stu-id="5ab3a-118">-Job</span></span>
<span data-ttu-id="5ab3a-119">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-119">Specifies the job to get.</span></span>
<span data-ttu-id="5ab3a-120">Verwenden Sie das Get-AzRecoveryServicesBackupJob-Cmdlet, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="5ab3a-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="5ab3a-121">-JobId</span></span>
<span data-ttu-id="5ab3a-122">Gibt die ID eines Backup-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="5ab3a-123">Die ID ist die InstanceId-Eigenschaft eines **BackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="5ab3a-124">-Tresor</span><span class="sxs-lookup"><span data-stu-id="5ab3a-124">-VaultId</span></span>
<span data-ttu-id="5ab3a-125">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="5ab3a-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ab3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab3a-126">CommonParameters</span></span>
<span data-ttu-id="5ab3a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab3a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab3a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab3a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ab3a-129">INPUTS</span></span>

### <span data-ttu-id="5ab3a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab3a-130">System.String</span></span>

## <span data-ttu-id="5ab3a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ab3a-131">OUTPUTS</span></span>

### <span data-ttu-id="5ab3a-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5ab3a-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5ab3a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ab3a-133">NOTES</span></span>

## <span data-ttu-id="5ab3a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ab3a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ab3a-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5ab3a-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


