---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 5f76c9a1adabf69872b4d529df7e3289e4d6745b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942299"
---
# <span data-ttu-id="37b22-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37b22-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="37b22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b22-102">SYNOPSIS</span></span>
<span data-ttu-id="37b22-103">Setzt einen angehaltenen Azure-Websitewiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="37b22-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="37b22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37b22-104">SYNTAX</span></span>

### <span data-ttu-id="37b22-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="37b22-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b22-106">ByName</span><span class="sxs-lookup"><span data-stu-id="37b22-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b22-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37b22-107">DESCRIPTION</span></span>
<span data-ttu-id="37b22-108">Das **Cmdlet Resume-AzRecoveryServicesAsrJob** setzt einen angehaltenen Azure-Websitewiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="37b22-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="37b22-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37b22-109">EXAMPLES</span></span>

### <span data-ttu-id="37b22-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37b22-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="37b22-111">Setzen Sie den angegebenen Auftrag fort, wenn er sich in einem wartenden oder angehaltenen Zustand befindet, und geben Sie das aktualisierte ASR-Auftragsobjekt zurück, das dem ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="37b22-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="37b22-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37b22-112">PARAMETERS</span></span>

### <span data-ttu-id="37b22-113">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="37b22-113">-Comment</span></span>
<span data-ttu-id="37b22-114">Kommentare für das Auftragsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="37b22-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b22-115">-DefaultProfile</span></span>
<span data-ttu-id="37b22-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37b22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="37b22-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b22-117">-InputObject</span></span>
<span data-ttu-id="37b22-118">Das Eingabeobjekt für das Cmdlet: Das ASR-Auftragsobjekt, das dem Auftrag entspricht, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b22-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b22-119">-Name</span><span class="sxs-lookup"><span data-stu-id="37b22-119">-Name</span></span>
<span data-ttu-id="37b22-120">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="37b22-120">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b22-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37b22-121">-Confirm</span></span>
<span data-ttu-id="37b22-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37b22-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b22-123">-WhatIf</span></span>
<span data-ttu-id="37b22-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b22-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37b22-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37b22-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b22-126">CommonParameters</span></span>
<span data-ttu-id="37b22-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b22-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37b22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b22-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37b22-129">INPUTS</span></span>

### <span data-ttu-id="37b22-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="37b22-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="37b22-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37b22-131">OUTPUTS</span></span>

### <span data-ttu-id="37b22-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="37b22-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="37b22-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37b22-133">NOTES</span></span>

## <span data-ttu-id="37b22-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37b22-134">RELATED LINKS</span></span>

[<span data-ttu-id="37b22-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37b22-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="37b22-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37b22-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="37b22-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37b22-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
