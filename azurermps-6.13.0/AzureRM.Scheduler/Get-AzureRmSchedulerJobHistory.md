---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 5bf5745270db8cea076ccac9cff2d4e9b7a4bc06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503366"
---
# <span data-ttu-id="7053b-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="7053b-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="7053b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7053b-102">SYNOPSIS</span></span>
<span data-ttu-id="7053b-103">Ruft den Auftragsverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="7053b-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7053b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7053b-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7053b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7053b-105">DESCRIPTION</span></span>
<span data-ttu-id="7053b-106">Das Cmdlet " **Get-AzureRmSchedulerJobHistory** " Ruft den Verlauf eines Azure Scheduler-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="7053b-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="7053b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7053b-107">EXAMPLES</span></span>

## <span data-ttu-id="7053b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7053b-108">PARAMETERS</span></span>

### <span data-ttu-id="7053b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7053b-109">-DefaultProfile</span></span>
<span data-ttu-id="7053b-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7053b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7053b-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7053b-111">-JobCollectionName</span></span>
<span data-ttu-id="7053b-112">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="7053b-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="7053b-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="7053b-113">-JobExecutionStatus</span></span>
<span data-ttu-id="7053b-114">Gibt den Status eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="7053b-114">Specifies the status of a job.</span></span>
<span data-ttu-id="7053b-115">Dieses Cmdlet ruft das Protokoll ab, das dem von Ihnen angegebenen Status entspricht.</span><span class="sxs-lookup"><span data-stu-id="7053b-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="7053b-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7053b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7053b-117">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="7053b-117">Completed</span></span> 
- <span data-ttu-id="7053b-118">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="7053b-118">Failed</span></span> 
- <span data-ttu-id="7053b-119">Verschoben</span><span class="sxs-lookup"><span data-stu-id="7053b-119">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7053b-120">-Jobname</span><span class="sxs-lookup"><span data-stu-id="7053b-120">-JobName</span></span>
<span data-ttu-id="7053b-121">Gibt den Namen eines Auftrags an, für den das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="7053b-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="7053b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7053b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7053b-123">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="7053b-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="7053b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7053b-124">CommonParameters</span></span>
<span data-ttu-id="7053b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7053b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7053b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7053b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7053b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7053b-127">INPUTS</span></span>

### <span data-ttu-id="7053b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7053b-128">System.String</span></span>

## <span data-ttu-id="7053b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7053b-129">OUTPUTS</span></span>

### <span data-ttu-id="7053b-130">Microsoft. Azure. Commands. Scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="7053b-130">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="7053b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7053b-131">NOTES</span></span>

## <span data-ttu-id="7053b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7053b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7053b-133">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="7053b-133">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


