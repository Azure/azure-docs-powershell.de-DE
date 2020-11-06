---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480557"
---
# <span data-ttu-id="234b2-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="234b2-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="234b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="234b2-102">SYNOPSIS</span></span>
<span data-ttu-id="234b2-103">Bricht einen vorhandenen Backup-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="234b2-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="234b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="234b2-104">SYNTAX</span></span>

### <span data-ttu-id="234b2-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="234b2-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="234b2-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="234b2-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234b2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="234b2-107">DESCRIPTION</span></span>
<span data-ttu-id="234b2-108">Mit dem Cmdlet " **Stop-AzureRmBackupJob** " wird ein vorhandener Azure Backup-Auftrag abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="234b2-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="234b2-109">Verwenden Sie diesen Parameter, um einen Auftrag zu beenden, der zu lange dauert und andere Aktivitäten blockiert.</span><span class="sxs-lookup"><span data-stu-id="234b2-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="234b2-110">Sie können nur die folgenden Arten von Aufträgen stornieren:</span><span class="sxs-lookup"><span data-stu-id="234b2-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="234b2-111">Backup</span><span class="sxs-lookup"><span data-stu-id="234b2-111">Backup</span></span>
- <span data-ttu-id="234b2-112">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="234b2-112">Restore</span></span>

## <span data-ttu-id="234b2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="234b2-113">EXAMPLES</span></span>

### <span data-ttu-id="234b2-114">Beispiel 1: Beenden eines Sicherungsauftrags mithilfe einer Auftrags-ID</span><span class="sxs-lookup"><span data-stu-id="234b2-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="234b2-115">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="234b2-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="234b2-116">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="234b2-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="234b2-117">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupJob** einen Sicherungsauftrag aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="234b2-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="234b2-118">Der Befehl speichert den Auftrag in der $Job-Variablen.</span><span class="sxs-lookup"><span data-stu-id="234b2-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="234b2-119">In diesem Beispiel ist nur ein Sicherungsvorgang im angegebenen Tresor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="234b2-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="234b2-120">Der endgültige Befehl beendet den Auftrag mit der angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="234b2-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="234b2-121">Beispiel 2: Beenden aller Wiederherstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="234b2-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="234b2-122">Dieser Befehl ruft alle Wiederherstellungsvorgänge im Tresor in $Vault ab und übergibt diese dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="234b2-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="234b2-123">Das aktuelle Cmdlet beendet die einzelnen Aufträge.</span><span class="sxs-lookup"><span data-stu-id="234b2-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="234b2-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="234b2-124">PARAMETERS</span></span>

### <span data-ttu-id="234b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234b2-125">-DefaultProfile</span></span>
<span data-ttu-id="234b2-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="234b2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="234b2-127">-Job</span><span class="sxs-lookup"><span data-stu-id="234b2-127">-Job</span></span>
<span data-ttu-id="234b2-128">Gibt einen Auftrag an, den dieses Cmdlet abbricht.</span><span class="sxs-lookup"><span data-stu-id="234b2-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="234b2-129">Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="234b2-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="234b2-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="234b2-130">-JobID</span></span>
<span data-ttu-id="234b2-131">Gibt einen Auftrag an, den dieses Cmdlet abbricht.</span><span class="sxs-lookup"><span data-stu-id="234b2-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="234b2-132">Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="234b2-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234b2-133">-Vault</span><span class="sxs-lookup"><span data-stu-id="234b2-133">-Vault</span></span>
<span data-ttu-id="234b2-134">Gibt den sicherungstresor an, in dem dieses Cmdlet einen Auftrag abbricht.</span><span class="sxs-lookup"><span data-stu-id="234b2-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="234b2-135">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="234b2-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234b2-136">CommonParameters</span></span>
<span data-ttu-id="234b2-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="234b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234b2-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="234b2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234b2-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="234b2-139">INPUTS</span></span>

### <span data-ttu-id="234b2-140">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="234b2-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="234b2-141">Parameter: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="234b2-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="234b2-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="234b2-142">OUTPUTS</span></span>

### <span data-ttu-id="234b2-143">System. void</span><span class="sxs-lookup"><span data-stu-id="234b2-143">System.Void</span></span>

## <span data-ttu-id="234b2-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="234b2-144">NOTES</span></span>

## <span data-ttu-id="234b2-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="234b2-145">RELATED LINKS</span></span>

[<span data-ttu-id="234b2-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="234b2-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="234b2-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="234b2-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="234b2-148">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="234b2-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


