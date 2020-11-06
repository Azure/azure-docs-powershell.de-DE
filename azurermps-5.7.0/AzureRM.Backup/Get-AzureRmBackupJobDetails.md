---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: 109a02ac04fe9926ef4510d295c978e01026ade2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505818"
---
# <span data-ttu-id="f3d5a-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="f3d5a-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="f3d5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d5a-103">Ruft die Details eines Backup-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d5a-104">SYNTAX</span></span>

### <span data-ttu-id="f3d5a-105">JobsFiltersSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3d5a-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3d5a-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="f3d5a-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d5a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d5a-108">Das Cmdlet " **Get-AzureRmBackupJobDetails** " Ruft die Details eines Azure Backup-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="f3d5a-109">Sie können dieses Cmdlet verwenden, um Informationen zu einem fehlerhaften Job zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="f3d5a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3d5a-110">EXAMPLES</span></span>

### <span data-ttu-id="f3d5a-111">Beispiel 1: Anzeigen der Details eines fehlerhaften Auftrags</span><span class="sxs-lookup"><span data-stu-id="f3d5a-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="f3d5a-112">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="f3d5a-113">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f3d5a-114">Der zweite Befehl ruft fehlerhafte Aufträge aus dem Tresor in $Vault ab und speichert Sie dann in der $Jobs-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="f3d5a-115">Der dritte Job ruft Details für den ersten Job in der $Jobs-Variablen ab und speichert diese Details dann in der $JobDetails-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="f3d5a-116">Der endgültige Befehl zeigt die **ErrorDetails** -Eigenschaft von $JobDetails mit der standardmäßigen Punktsyntax an.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="f3d5a-117">Beispiel 2: Anzeigen der empfohlenen Aktion für einen fehlerhaften Auftrag</span><span class="sxs-lookup"><span data-stu-id="f3d5a-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="f3d5a-118">Dieser Befehl zeigt die empfohlene Aktion aus der $JobDetails Variablen an, die im ersten Beispiel erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="f3d5a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3d5a-119">PARAMETERS</span></span>

### <span data-ttu-id="f3d5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d5a-120">-DefaultProfile</span></span>
<span data-ttu-id="f3d5a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3d5a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3d5a-122">-Job</span><span class="sxs-lookup"><span data-stu-id="f3d5a-122">-Job</span></span>
<span data-ttu-id="f3d5a-123">Gibt einen Auftrag an, für den dieses Cmdlet Details erhält.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="f3d5a-124">Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d5a-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="f3d5a-125">-JobId</span></span>
<span data-ttu-id="f3d5a-126">Gibt die ID eines Auftrags an, für den dieses Cmdlet Details erhält.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="f3d5a-127">Die ID ist die **InstanceId** -Eigenschaft eines **AzureRmBackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="f3d5a-128">Verwenden Sie Get-AzureRmBackupJob, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d5a-129">-Vault</span><span class="sxs-lookup"><span data-stu-id="f3d5a-129">-Vault</span></span>
<span data-ttu-id="f3d5a-130">Gibt den sicherungstresor an, für den dieses Cmdlet Auftragsdetails erhält.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="f3d5a-131">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d5a-132">CommonParameters</span></span>
<span data-ttu-id="f3d5a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d5a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d5a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d5a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3d5a-135">INPUTS</span></span>

### <span data-ttu-id="f3d5a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f3d5a-136">None</span></span>

## <span data-ttu-id="f3d5a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3d5a-137">OUTPUTS</span></span>

### <span data-ttu-id="f3d5a-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="f3d5a-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="f3d5a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3d5a-139">NOTES</span></span>
* <span data-ttu-id="f3d5a-140">Keine</span><span class="sxs-lookup"><span data-stu-id="f3d5a-140">None</span></span>

## <span data-ttu-id="f3d5a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3d5a-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3d5a-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f3d5a-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="f3d5a-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f3d5a-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


