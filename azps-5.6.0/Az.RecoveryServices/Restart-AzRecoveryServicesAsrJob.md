---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 2609ed7483499445dbdd093d0059b76b7e781ef8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919168"
---
# <span data-ttu-id="606e4-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="606e4-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="606e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606e4-102">SYNOPSIS</span></span>
<span data-ttu-id="606e4-103">Startet einen Azure-Websitewiederherstellungsauftrag neu.</span><span class="sxs-lookup"><span data-stu-id="606e4-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="606e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="606e4-104">SYNTAX</span></span>

### <span data-ttu-id="606e4-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="606e4-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606e4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="606e4-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="606e4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="606e4-107">DESCRIPTION</span></span>
<span data-ttu-id="606e4-108">Das **Cmdlet Restart-AzRecoveryServicesAsrJob** startet einen Azure-Websitewiederherstellungsauftrag neu.</span><span class="sxs-lookup"><span data-stu-id="606e4-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="606e4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="606e4-109">EXAMPLES</span></span>

### <span data-ttu-id="606e4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="606e4-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="606e4-111">Startet den angegebenen ASR-Auftrag neu und gibt das aktualisierte ASR-Auftragsobjekt des ASR-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="606e4-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="606e4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="606e4-112">PARAMETERS</span></span>

### <span data-ttu-id="606e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606e4-113">-DefaultProfile</span></span>
<span data-ttu-id="606e4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="606e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="606e4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="606e4-115">-InputObject</span></span>
<span data-ttu-id="606e4-116">Das Eingabeobjekt für das Cmdlet: Das ASR-Auftragsobjekt, das dem neu zu startende ASR-Auftrag entspricht</span><span class="sxs-lookup"><span data-stu-id="606e4-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="606e4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="606e4-117">-Name</span></span>
<span data-ttu-id="606e4-118">Geben Sie den Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="606e4-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="606e4-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="606e4-119">-Confirm</span></span>
<span data-ttu-id="606e4-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="606e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="606e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606e4-121">-WhatIf</span></span>
<span data-ttu-id="606e4-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="606e4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="606e4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="606e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="606e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606e4-124">CommonParameters</span></span>
<span data-ttu-id="606e4-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606e4-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="606e4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606e4-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="606e4-127">INPUTS</span></span>

### <span data-ttu-id="606e4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="606e4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="606e4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="606e4-129">OUTPUTS</span></span>

### <span data-ttu-id="606e4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="606e4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="606e4-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="606e4-131">NOTES</span></span>

## <span data-ttu-id="606e4-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="606e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="606e4-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="606e4-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="606e4-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="606e4-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="606e4-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="606e4-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
