---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: dfec2d79d092a5f119daa558b1d383f1a1d71df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482726"
---
# <span data-ttu-id="0391e-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="0391e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0391e-102">SYNOPSIS</span></span>
<span data-ttu-id="0391e-103">Erstellt eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0391e-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0391e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0391e-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0391e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0391e-105">DESCRIPTION</span></span>
<span data-ttu-id="0391e-106">Das Cmdlet **New-AzureRmSchedulerJobCollection** erstellt eine Auftrags Sammlung im Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="0391e-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="0391e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0391e-107">EXAMPLES</span></span>

## <span data-ttu-id="0391e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0391e-108">PARAMETERS</span></span>

### <span data-ttu-id="0391e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0391e-109">-DefaultProfile</span></span>
<span data-ttu-id="0391e-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0391e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0391e-111">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="0391e-111">-Frequency</span></span>
<span data-ttu-id="0391e-112">Gibt die maximale Häufigkeit an, die Sie für einen beliebigen Job in der Auftrags Sammlung angeben können.</span><span class="sxs-lookup"><span data-stu-id="0391e-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="0391e-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0391e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0391e-114">Minuten</span><span class="sxs-lookup"><span data-stu-id="0391e-114">Minute</span></span> 
- <span data-ttu-id="0391e-115">Stunde</span><span class="sxs-lookup"><span data-stu-id="0391e-115">Hour</span></span> 
- <span data-ttu-id="0391e-116">Tag</span><span class="sxs-lookup"><span data-stu-id="0391e-116">Day</span></span> 
- <span data-ttu-id="0391e-117">Woche</span><span class="sxs-lookup"><span data-stu-id="0391e-117">Week</span></span> 
- <span data-ttu-id="0391e-118">Monat</span><span class="sxs-lookup"><span data-stu-id="0391e-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-119">-Intervall</span><span class="sxs-lookup"><span data-stu-id="0391e-119">-Interval</span></span>
<span data-ttu-id="0391e-120">Gibt ein Wiederholungsintervall an.</span><span class="sxs-lookup"><span data-stu-id="0391e-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0391e-121">-JobCollectionName</span></span>
<span data-ttu-id="0391e-122">Gibt einen Namen für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="0391e-122">Specifies a name for the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="0391e-123">-Location</span></span>
<span data-ttu-id="0391e-124">Gibt den Azure-Bereich an, in dem dieses Cmdlet die Auftrags Sammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0391e-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="0391e-125">-MaxJobCount</span></span>
<span data-ttu-id="0391e-126">Gibt die maximale Anzahl von Aufträgen an, die Sie in der Auftrags Sammlung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="0391e-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="0391e-127">Der Höchstbetrag hängt vom Plan ab, der vom *Plan* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0391e-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="0391e-128">-Plan</span></span>
<span data-ttu-id="0391e-129">Gibt den Plan für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="0391e-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="0391e-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0391e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0391e-131">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="0391e-131">Free</span></span> 
- <span data-ttu-id="0391e-132">Standard</span><span class="sxs-lookup"><span data-stu-id="0391e-132">Standard</span></span> 
- <span data-ttu-id="0391e-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="0391e-133">P10Premium</span></span> 
- <span data-ttu-id="0391e-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="0391e-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0391e-135">-ResourceGroupName</span></span>
<span data-ttu-id="0391e-136">Gibt die Ressourcengruppe für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="0391e-136">Specifies the resource group for the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0391e-137">-Confirm</span></span>
<span data-ttu-id="0391e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0391e-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0391e-139">-WhatIf</span></span>
<span data-ttu-id="0391e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0391e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0391e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0391e-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0391e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0391e-142">CommonParameters</span></span>
<span data-ttu-id="0391e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0391e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0391e-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0391e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0391e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0391e-145">INPUTS</span></span>

### <span data-ttu-id="0391e-146">Keine</span><span class="sxs-lookup"><span data-stu-id="0391e-146">None</span></span>
<span data-ttu-id="0391e-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0391e-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0391e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0391e-148">OUTPUTS</span></span>

### <span data-ttu-id="0391e-149">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="0391e-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="0391e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="0391e-150">NOTES</span></span>

## <span data-ttu-id="0391e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0391e-151">RELATED LINKS</span></span>

[<span data-ttu-id="0391e-152">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0391e-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0391e-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0391e-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0391e-156">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0391e-156">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


