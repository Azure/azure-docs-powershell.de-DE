---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304688"
---
# <span data-ttu-id="03065-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="03065-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="03065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03065-102">SYNOPSIS</span></span>
<span data-ttu-id="03065-103">Setzt einen angehaltenen Azure-Websitewiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="03065-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="03065-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03065-104">SYNTAX</span></span>

### <span data-ttu-id="03065-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="03065-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03065-106">ByName</span><span class="sxs-lookup"><span data-stu-id="03065-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03065-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03065-107">DESCRIPTION</span></span>
<span data-ttu-id="03065-108">Das **Cmdlet "Resume-AzRecoveryServicesAsrJob"** setzt einen angehaltenen Azure-Websitewiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="03065-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="03065-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03065-109">EXAMPLES</span></span>

### <span data-ttu-id="03065-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03065-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="03065-111">Setzen Sie den angegebenen Auftrag fort, wenn er sich in einem wartenden oder angehaltenen Zustand befindet, und geben Sie das aktualisierte ASR-Auftragsobjekt zurück, das dem ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="03065-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="03065-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03065-112">PARAMETERS</span></span>

### <span data-ttu-id="03065-113">-Comment</span><span class="sxs-lookup"><span data-stu-id="03065-113">-Comment</span></span>
<span data-ttu-id="03065-114">Kommentare für das Auftragsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="03065-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="03065-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03065-115">-DefaultProfile</span></span>
<span data-ttu-id="03065-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03065-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="03065-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03065-117">-InputObject</span></span>
<span data-ttu-id="03065-118">Das Eingabeobjekt für das Cmdlet: Das ASR-Auftragsobjekt, das dem Auftrag entspricht, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03065-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="03065-119">-Name</span><span class="sxs-lookup"><span data-stu-id="03065-119">-Name</span></span>
<span data-ttu-id="03065-120">Geben Sie den Asr-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="03065-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="03065-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03065-121">-Confirm</span></span>
<span data-ttu-id="03065-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03065-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03065-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03065-123">-WhatIf</span></span>
<span data-ttu-id="03065-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03065-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03065-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03065-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03065-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03065-126">CommonParameters</span></span>
<span data-ttu-id="03065-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03065-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03065-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03065-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03065-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03065-129">INPUTS</span></span>

### <span data-ttu-id="03065-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="03065-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="03065-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03065-131">OUTPUTS</span></span>

### <span data-ttu-id="03065-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="03065-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="03065-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03065-133">NOTES</span></span>

## <span data-ttu-id="03065-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03065-134">RELATED LINKS</span></span>

[<span data-ttu-id="03065-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="03065-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="03065-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="03065-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="03065-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="03065-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
