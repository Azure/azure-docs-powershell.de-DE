---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663830"
---
# <span data-ttu-id="2d185-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2d185-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="2d185-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d185-102">SYNOPSIS</span></span>
<span data-ttu-id="2d185-103">Ruft Scheduler-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="2d185-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d185-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d185-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d185-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d185-105">DESCRIPTION</span></span>
<span data-ttu-id="2d185-106">Das Cmdlet " **Get-AzureRmSchedulerJob** " ruft Azure Scheduler-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="2d185-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="2d185-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d185-107">EXAMPLES</span></span>

## <span data-ttu-id="2d185-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d185-108">PARAMETERS</span></span>

### <span data-ttu-id="2d185-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2d185-109">-JobCollectionName</span></span>
<span data-ttu-id="2d185-110">Gibt den Namen einer Auftrags Sammlung an, die abzurufende Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="2d185-110">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="2d185-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2d185-111">-JobName</span></span>
<span data-ttu-id="2d185-112">Gibt den Namen des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2d185-112">Specifies the name of a job to get.</span></span>

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

### <span data-ttu-id="2d185-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="2d185-113">-JobState</span></span>
<span data-ttu-id="2d185-114">Gibt den Auftragsstatus der abzurufenden Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="2d185-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="2d185-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2d185-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d185-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2d185-116">Enabled</span></span> 
- <span data-ttu-id="2d185-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="2d185-117">Disabled</span></span> 
- <span data-ttu-id="2d185-118">Faulted</span><span class="sxs-lookup"><span data-stu-id="2d185-118">Faulted</span></span> 
- <span data-ttu-id="2d185-119">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="2d185-119">Completed</span></span>

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

### <span data-ttu-id="2d185-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d185-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d185-121">Gibt die Ressourcengruppe der Aufträge an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d185-121">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="2d185-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d185-122">-DefaultProfile</span></span>
<span data-ttu-id="2d185-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d185-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d185-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d185-124">CommonParameters</span></span>
<span data-ttu-id="2d185-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d185-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d185-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d185-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d185-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d185-127">INPUTS</span></span>

## <span data-ttu-id="2d185-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d185-128">OUTPUTS</span></span>

### <span data-ttu-id="2d185-129">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2d185-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="2d185-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d185-130">NOTES</span></span>

## <span data-ttu-id="2d185-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d185-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d185-132">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d185-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2d185-133">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2d185-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2d185-134">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d185-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2d185-135">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2d185-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="2d185-136">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d185-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="2d185-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2d185-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="2d185-138">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d185-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2d185-139">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d185-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2d185-140">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2d185-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="2d185-141">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d185-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


