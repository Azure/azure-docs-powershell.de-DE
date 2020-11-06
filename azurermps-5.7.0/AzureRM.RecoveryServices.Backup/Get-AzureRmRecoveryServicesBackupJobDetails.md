---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478366"
---
# <span data-ttu-id="05844-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="05844-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="05844-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05844-102">SYNOPSIS</span></span>
<span data-ttu-id="05844-103">Ruft Details für einen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="05844-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05844-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05844-104">SYNTAX</span></span>

### <span data-ttu-id="05844-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05844-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05844-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="05844-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05844-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05844-107">DESCRIPTION</span></span>
<span data-ttu-id="05844-108">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupJobDetails** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="05844-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="05844-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="05844-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="05844-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05844-110">EXAMPLES</span></span>

### <span data-ttu-id="05844-111">Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge</span><span class="sxs-lookup"><span data-stu-id="05844-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="05844-112">Der erste Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.</span><span class="sxs-lookup"><span data-stu-id="05844-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="05844-113">Der zweite Befehl ruft die Auftragsdetails für die fehlgeschlagenen Aufträge in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.</span><span class="sxs-lookup"><span data-stu-id="05844-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="05844-114">Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="05844-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="05844-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="05844-115">PARAMETERS</span></span>

### <span data-ttu-id="05844-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05844-116">-DefaultProfile</span></span>
<span data-ttu-id="05844-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05844-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05844-118">-Job</span><span class="sxs-lookup"><span data-stu-id="05844-118">-Job</span></span>
<span data-ttu-id="05844-119">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="05844-119">Specifies the job to get.</span></span>
<span data-ttu-id="05844-120">Verwenden Sie das Get-AzureRmRecoveryServicesBackupJob-Cmdlet, um ein **BackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="05844-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05844-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="05844-121">-JobId</span></span>
<span data-ttu-id="05844-122">Gibt die ID eines Backup-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="05844-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="05844-123">Die ID ist die InstanceId-Eigenschaft eines **BackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="05844-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05844-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05844-124">CommonParameters</span></span>
<span data-ttu-id="05844-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05844-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05844-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05844-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05844-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05844-127">INPUTS</span></span>

### <span data-ttu-id="05844-128">Keine</span><span class="sxs-lookup"><span data-stu-id="05844-128">None</span></span>
<span data-ttu-id="05844-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="05844-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05844-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05844-130">OUTPUTS</span></span>

### <span data-ttu-id="05844-131">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="05844-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="05844-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="05844-132">NOTES</span></span>

## <span data-ttu-id="05844-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05844-133">RELATED LINKS</span></span>

[<span data-ttu-id="05844-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="05844-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


