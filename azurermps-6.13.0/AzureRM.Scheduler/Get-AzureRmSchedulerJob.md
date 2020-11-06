---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 89c4a6bd9d009456c97aa246f608c1920c27c823
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503377"
---
# <span data-ttu-id="71ce8-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="71ce8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="71ce8-103">Ruft Scheduler-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="71ce8-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ce8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ce8-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71ce8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="71ce8-106">Das Cmdlet " **Get-AzureRmSchedulerJob** " ruft Azure Scheduler-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="71ce8-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="71ce8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71ce8-107">EXAMPLES</span></span>

## <span data-ttu-id="71ce8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="71ce8-108">PARAMETERS</span></span>

### <span data-ttu-id="71ce8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ce8-109">-DefaultProfile</span></span>
<span data-ttu-id="71ce8-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71ce8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ce8-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="71ce8-111">-JobCollectionName</span></span>
<span data-ttu-id="71ce8-112">Gibt den Namen einer Auftrags Sammlung an, die abzurufende Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="71ce8-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ce8-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="71ce8-113">-JobName</span></span>
<span data-ttu-id="71ce8-114">Gibt den Namen des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="71ce8-114">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ce8-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="71ce8-115">-JobState</span></span>
<span data-ttu-id="71ce8-116">Gibt den Auftragsstatus der abzurufenden Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="71ce8-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="71ce8-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71ce8-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71ce8-118">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="71ce8-118">Enabled</span></span> 
- <span data-ttu-id="71ce8-119">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="71ce8-119">Disabled</span></span> 
- <span data-ttu-id="71ce8-120">Faulted</span><span class="sxs-lookup"><span data-stu-id="71ce8-120">Faulted</span></span> 
- <span data-ttu-id="71ce8-121">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="71ce8-121">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ce8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ce8-122">-ResourceGroupName</span></span>
<span data-ttu-id="71ce8-123">Gibt die Ressourcengruppe der Aufträge an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71ce8-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ce8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ce8-124">CommonParameters</span></span>
<span data-ttu-id="71ce8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ce8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ce8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ce8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ce8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71ce8-127">INPUTS</span></span>

### <span data-ttu-id="71ce8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="71ce8-128">System.String</span></span>

## <span data-ttu-id="71ce8-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71ce8-129">OUTPUTS</span></span>

### <span data-ttu-id="71ce8-130">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="71ce8-130">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="71ce8-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="71ce8-131">NOTES</span></span>

## <span data-ttu-id="71ce8-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71ce8-132">RELATED LINKS</span></span>

[<span data-ttu-id="71ce8-133">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-133">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="71ce8-134">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71ce8-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="71ce8-135">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-135">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="71ce8-136">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-136">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="71ce8-137">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-137">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="71ce8-138">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-138">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="71ce8-139">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-139">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="71ce8-140">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-140">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="71ce8-141">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-141">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="71ce8-142">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="71ce8-142">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


