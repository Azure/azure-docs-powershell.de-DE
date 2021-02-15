---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151108"
---
# <span data-ttu-id="285a4-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285a4-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="285a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285a4-102">SYNOPSIS</span></span>
<span data-ttu-id="285a4-103">Beendet einen Azure-Websitewiederherstellungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="285a4-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="285a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="285a4-104">SYNTAX</span></span>

### <span data-ttu-id="285a4-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="285a4-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285a4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="285a4-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="285a4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285a4-107">DESCRIPTION</span></span>
<span data-ttu-id="285a4-108">Das **Cmdlet "Stop-AzRecoveryServicesAsrJob"** beendet den angegebenen Azure-Websitewiederherstellungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="285a4-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="285a4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="285a4-109">EXAMPLES</span></span>

### <span data-ttu-id="285a4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="285a4-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="285a4-111">Versucht, den angegebenen Auftrag zu beenden, und gibt ein aktualisiertes Objekt für den ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="285a4-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="285a4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285a4-112">PARAMETERS</span></span>

### <span data-ttu-id="285a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285a4-113">-DefaultProfile</span></span>
<span data-ttu-id="285a4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="285a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="285a4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="285a4-115">-InputObject</span></span>
<span data-ttu-id="285a4-116">Eingabeobjekt: Angeben des ASR-Auftragsobjekts, das dem zu stoppende ASR-Auftrag entspricht</span><span class="sxs-lookup"><span data-stu-id="285a4-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="285a4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="285a4-117">-Name</span></span>
<span data-ttu-id="285a4-118">Geben Sie den ASR-Auftrag an, der vom Namen des ASR-Auftrags beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="285a4-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="285a4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285a4-119">-Confirm</span></span>
<span data-ttu-id="285a4-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="285a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285a4-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="285a4-121">-WhatIf</span></span>
<span data-ttu-id="285a4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="285a4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="285a4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="285a4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285a4-124">CommonParameters</span></span>
<span data-ttu-id="285a4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285a4-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="285a4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285a4-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="285a4-127">INPUTS</span></span>

### <span data-ttu-id="285a4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="285a4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="285a4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="285a4-129">OUTPUTS</span></span>

### <span data-ttu-id="285a4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="285a4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="285a4-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="285a4-131">NOTES</span></span>

## <span data-ttu-id="285a4-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="285a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="285a4-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285a4-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="285a4-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285a4-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="285a4-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285a4-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
