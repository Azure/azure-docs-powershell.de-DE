---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501625"
---
# <span data-ttu-id="7051f-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="7051f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7051f-102">SYNOPSIS</span></span>
<span data-ttu-id="7051f-103">Erstellt eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7051f-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7051f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7051f-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7051f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7051f-105">DESCRIPTION</span></span>
<span data-ttu-id="7051f-106">Das Cmdlet **New-AzureRmSchedulerJobCollection** erstellt eine Auftrags Sammlung im Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="7051f-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="7051f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7051f-107">EXAMPLES</span></span>

## <span data-ttu-id="7051f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7051f-108">PARAMETERS</span></span>

### <span data-ttu-id="7051f-109">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="7051f-109">-Frequency</span></span>
<span data-ttu-id="7051f-110">Gibt die maximale Häufigkeit an, die Sie für einen beliebigen Job in der Auftrags Sammlung angeben können.</span><span class="sxs-lookup"><span data-stu-id="7051f-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="7051f-111">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7051f-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7051f-112">Minuten</span><span class="sxs-lookup"><span data-stu-id="7051f-112">Minute</span></span> 
- <span data-ttu-id="7051f-113">Stunde</span><span class="sxs-lookup"><span data-stu-id="7051f-113">Hour</span></span> 
- <span data-ttu-id="7051f-114">Tag</span><span class="sxs-lookup"><span data-stu-id="7051f-114">Day</span></span> 
- <span data-ttu-id="7051f-115">Woche</span><span class="sxs-lookup"><span data-stu-id="7051f-115">Week</span></span> 
- <span data-ttu-id="7051f-116">Monat</span><span class="sxs-lookup"><span data-stu-id="7051f-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7051f-117">-Intervall</span><span class="sxs-lookup"><span data-stu-id="7051f-117">-Interval</span></span>
<span data-ttu-id="7051f-118">Gibt ein Wiederholungsintervall an.</span><span class="sxs-lookup"><span data-stu-id="7051f-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7051f-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7051f-119">-JobCollectionName</span></span>
<span data-ttu-id="7051f-120">Gibt einen Namen für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="7051f-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="7051f-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="7051f-121">-Location</span></span>
<span data-ttu-id="7051f-122">Gibt den Azure-Bereich an, in dem dieses Cmdlet die Auftrags Sammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7051f-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="7051f-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="7051f-123">-MaxJobCount</span></span>
<span data-ttu-id="7051f-124">Gibt die maximale Anzahl von Aufträgen an, die Sie in der Auftrags Sammlung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="7051f-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="7051f-125">Der Höchstbetrag hängt vom Plan ab, der vom *Plan* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7051f-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7051f-126">-Plan</span><span class="sxs-lookup"><span data-stu-id="7051f-126">-Plan</span></span>
<span data-ttu-id="7051f-127">Gibt den Plan für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="7051f-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="7051f-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7051f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7051f-129">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="7051f-129">Free</span></span> 
- <span data-ttu-id="7051f-130">Standard</span><span class="sxs-lookup"><span data-stu-id="7051f-130">Standard</span></span> 
- <span data-ttu-id="7051f-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="7051f-131">P10Premium</span></span> 
- <span data-ttu-id="7051f-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="7051f-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7051f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7051f-133">-ResourceGroupName</span></span>
<span data-ttu-id="7051f-134">Gibt die Ressourcengruppe für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="7051f-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="7051f-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7051f-135">-Confirm</span></span>
<span data-ttu-id="7051f-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7051f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7051f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7051f-137">-WhatIf</span></span>
<span data-ttu-id="7051f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7051f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7051f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7051f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7051f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7051f-140">-DefaultProfile</span></span>
<span data-ttu-id="7051f-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7051f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7051f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7051f-142">CommonParameters</span></span>
<span data-ttu-id="7051f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7051f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7051f-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7051f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7051f-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7051f-145">INPUTS</span></span>

## <span data-ttu-id="7051f-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7051f-146">OUTPUTS</span></span>

### <span data-ttu-id="7051f-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="7051f-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="7051f-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="7051f-148">NOTES</span></span>

## <span data-ttu-id="7051f-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7051f-149">RELATED LINKS</span></span>

[<span data-ttu-id="7051f-150">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7051f-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7051f-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7051f-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7051f-154">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7051f-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


