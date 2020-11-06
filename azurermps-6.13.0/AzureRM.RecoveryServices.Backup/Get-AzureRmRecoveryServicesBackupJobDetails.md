---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477813"
---
# <span data-ttu-id="96476-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="96476-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="96476-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96476-102">SYNOPSIS</span></span>
<span data-ttu-id="96476-103">Ruft Details für einen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96476-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96476-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96476-104">SYNTAX</span></span>

### <span data-ttu-id="96476-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="96476-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96476-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="96476-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96476-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96476-107">DESCRIPTION</span></span>
<span data-ttu-id="96476-108">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupJobDetails** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96476-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="96476-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="96476-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="96476-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96476-110">EXAMPLES</span></span>

### <span data-ttu-id="96476-111">Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge</span><span class="sxs-lookup"><span data-stu-id="96476-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="96476-112">Der erste Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.</span><span class="sxs-lookup"><span data-stu-id="96476-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="96476-113">Der zweite Befehl ruft die Auftragsdetails für die fehlgeschlagenen Aufträge in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="96476-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="96476-114">Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="96476-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="96476-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="96476-115">PARAMETERS</span></span>

### <span data-ttu-id="96476-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96476-116">-DefaultProfile</span></span>
<span data-ttu-id="96476-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96476-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96476-118">-Job</span><span class="sxs-lookup"><span data-stu-id="96476-118">-Job</span></span>
<span data-ttu-id="96476-119">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="96476-119">Specifies the job to get.</span></span>
<span data-ttu-id="96476-120">Verwenden Sie das Get-AzureRmRecoveryServicesBackupJob-Cmdlet, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="96476-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="96476-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="96476-121">-JobId</span></span>
<span data-ttu-id="96476-122">Gibt die ID eines Backup-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="96476-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="96476-123">Die ID ist die InstanceId-Eigenschaft eines **BackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="96476-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="96476-124">-Tresor</span><span class="sxs-lookup"><span data-stu-id="96476-124">-VaultId</span></span>
<span data-ttu-id="96476-125">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="96476-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="96476-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96476-126">CommonParameters</span></span>
<span data-ttu-id="96476-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96476-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96476-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96476-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96476-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96476-129">INPUTS</span></span>

### <span data-ttu-id="96476-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96476-130">System.String</span></span>
<span data-ttu-id="96476-131">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="96476-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="96476-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96476-132">OUTPUTS</span></span>

### <span data-ttu-id="96476-133">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="96476-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="96476-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="96476-134">NOTES</span></span>

## <span data-ttu-id="96476-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96476-135">RELATED LINKS</span></span>

[<span data-ttu-id="96476-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="96476-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


