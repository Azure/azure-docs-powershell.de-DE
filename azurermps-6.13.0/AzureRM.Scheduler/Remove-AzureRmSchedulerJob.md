---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480085"
---
# <span data-ttu-id="92b4d-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="92b4d-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="92b4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="92b4d-103">Entfernt einen Scheduler-Job.</span><span class="sxs-lookup"><span data-stu-id="92b4d-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92b4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92b4d-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b4d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="92b4d-106">Mit dem Cmdlet **Remove-AzureRmSchedulerJob** wird ein Azure Scheduler-Auftrag entfernt.</span><span class="sxs-lookup"><span data-stu-id="92b4d-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="92b4d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92b4d-107">EXAMPLES</span></span>

## <span data-ttu-id="92b4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="92b4d-108">PARAMETERS</span></span>

### <span data-ttu-id="92b4d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b4d-109">-DefaultProfile</span></span>
<span data-ttu-id="92b4d-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92b4d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b4d-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="92b4d-111">-JobCollectionName</span></span>
<span data-ttu-id="92b4d-112">Gibt den Namen einer Auftrags Sammlung an, die den zu entfernenden Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="92b4d-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="92b4d-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="92b4d-113">-JobName</span></span>
<span data-ttu-id="92b4d-114">Gibt den Namen des zu entfernenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="92b4d-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="92b4d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b4d-115">-PassThru</span></span>
<span data-ttu-id="92b4d-116">Gibt an, dass dieses Cmdlet den Wert Success für Success zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="92b4d-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="92b4d-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="92b4d-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b4d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b4d-118">-ResourceGroupName</span></span>
<span data-ttu-id="92b4d-119">Gibt die Ressourcengruppe des Auftrags an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92b4d-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="92b4d-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92b4d-120">-Confirm</span></span>
<span data-ttu-id="92b4d-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92b4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b4d-122">-WhatIf</span></span>
<span data-ttu-id="92b4d-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92b4d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b4d-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92b4d-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b4d-125">CommonParameters</span></span>
<span data-ttu-id="92b4d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b4d-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b4d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b4d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92b4d-128">INPUTS</span></span>

### <span data-ttu-id="92b4d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="92b4d-129">System.String</span></span>

## <span data-ttu-id="92b4d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92b4d-130">OUTPUTS</span></span>

### <span data-ttu-id="92b4d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92b4d-131">System.String</span></span>

## <span data-ttu-id="92b4d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="92b4d-132">NOTES</span></span>

## <span data-ttu-id="92b4d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92b4d-133">RELATED LINKS</span></span>

[<span data-ttu-id="92b4d-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="92b4d-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


