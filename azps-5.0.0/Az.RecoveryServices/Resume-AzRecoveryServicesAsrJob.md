---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177417"
---
# <span data-ttu-id="0b3c3-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0b3c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3c3-103">Setzt einen angehenden Azure Site Recovery-Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0b3c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b3c3-104">SYNTAX</span></span>

### <span data-ttu-id="0b3c3-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b3c3-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3c3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0b3c3-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b3c3-107">DESCRIPTION</span></span>
<span data-ttu-id="0b3c3-108">Mit dem Cmdlet **Resume-AzRecoveryServicesAsrJob** wird ein angehaltene Azure Site Recovery-Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0b3c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b3c3-109">EXAMPLES</span></span>

### <span data-ttu-id="0b3c3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b3c3-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0b3c3-111">Fortsetzen des angegebenen Auftrags, wenn er sich in einem warte-oder angehalten-Zustand befindet und das aktualisierte ASR-Auftragsobjekt zurückgibt, das dem ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="0b3c3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b3c3-112">PARAMETERS</span></span>

### <span data-ttu-id="0b3c3-113">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="0b3c3-113">-Comment</span></span>
<span data-ttu-id="0b3c3-114">Kommentare für das Auftragsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="0b3c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c3-115">-DefaultProfile</span></span>
<span data-ttu-id="0b3c3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0b3c3-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b3c3-117">-InputObject</span></span>
<span data-ttu-id="0b3c3-118">Das Eingabeobjekt für das Cmdlet: das ASR-Auftragsobjekt, das dem Auftrag entspricht, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="0b3c3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b3c3-119">-Name</span></span>
<span data-ttu-id="0b3c3-120">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="0b3c3-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b3c3-121">-Confirm</span></span>
<span data-ttu-id="0b3c3-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3c3-123">-WhatIf</span></span>
<span data-ttu-id="0b3c3-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b3c3-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3c3-126">CommonParameters</span></span>
<span data-ttu-id="0b3c3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3c3-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b3c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3c3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b3c3-129">INPUTS</span></span>

### <span data-ttu-id="0b3c3-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b3c3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b3c3-131">OUTPUTS</span></span>

### <span data-ttu-id="0b3c3-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b3c3-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b3c3-133">NOTES</span></span>

## <span data-ttu-id="0b3c3-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b3c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b3c3-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0b3c3-136">Neustart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0b3c3-137">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b3c3-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
