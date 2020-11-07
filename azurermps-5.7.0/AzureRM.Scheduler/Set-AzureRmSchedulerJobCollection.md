---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: fc2375e66dbc47ccadf11d0f7dd9dd66e42470de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663749"
---
# <span data-ttu-id="ea140-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="ea140-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea140-102">SYNOPSIS</span></span>
<span data-ttu-id="ea140-103">Ändert eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ea140-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea140-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea140-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea140-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea140-105">DESCRIPTION</span></span>
<span data-ttu-id="ea140-106">Das Cmdlet " **Satz-AzureRmSchedulerJobCollection** " ändert eine Auftrags Sammlung in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="ea140-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="ea140-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea140-107">EXAMPLES</span></span>

## <span data-ttu-id="ea140-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea140-108">PARAMETERS</span></span>

### <span data-ttu-id="ea140-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea140-109">-DefaultProfile</span></span>
<span data-ttu-id="ea140-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea140-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea140-111">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="ea140-111">-Frequency</span></span>
<span data-ttu-id="ea140-112">Gibt die maximale Häufigkeit an, die Sie für einen beliebigen Job in der Auftrags Sammlung angeben können.</span><span class="sxs-lookup"><span data-stu-id="ea140-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="ea140-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea140-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea140-114">Minuten</span><span class="sxs-lookup"><span data-stu-id="ea140-114">Minute</span></span> 
- <span data-ttu-id="ea140-115">Stunde</span><span class="sxs-lookup"><span data-stu-id="ea140-115">Hour</span></span> 
- <span data-ttu-id="ea140-116">Tag</span><span class="sxs-lookup"><span data-stu-id="ea140-116">Day</span></span> 
- <span data-ttu-id="ea140-117">Woche</span><span class="sxs-lookup"><span data-stu-id="ea140-117">Week</span></span> 
- <span data-ttu-id="ea140-118">Monat</span><span class="sxs-lookup"><span data-stu-id="ea140-118">Month</span></span>

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

### <span data-ttu-id="ea140-119">-Intervall</span><span class="sxs-lookup"><span data-stu-id="ea140-119">-Interval</span></span>
<span data-ttu-id="ea140-120">Gibt ein Wiederholungsintervall an.</span><span class="sxs-lookup"><span data-stu-id="ea140-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="ea140-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ea140-121">-JobCollectionName</span></span>
<span data-ttu-id="ea140-122">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="ea140-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="ea140-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="ea140-123">-Location</span></span>
<span data-ttu-id="ea140-124">Gibt den Azure-Bereich an, in dem die Auftrags Sammlung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ea140-124">Specifies the Azure region in which the job collection exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea140-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="ea140-125">-MaxJobCount</span></span>
<span data-ttu-id="ea140-126">Gibt die maximale Anzahl von Aufträgen an, die Sie in der Auftrags Sammlung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="ea140-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="ea140-127">Der Höchstbetrag hängt vom Plan ab, der vom *Plan* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea140-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="ea140-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="ea140-128">-Plan</span></span>
<span data-ttu-id="ea140-129">Gibt den Plan für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="ea140-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="ea140-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea140-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea140-131">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ea140-131">Free</span></span> 
- <span data-ttu-id="ea140-132">Standard</span><span class="sxs-lookup"><span data-stu-id="ea140-132">Standard</span></span> 
- <span data-ttu-id="ea140-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="ea140-133">P10Premium</span></span> 
- <span data-ttu-id="ea140-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="ea140-134">P20Premium</span></span>

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

### <span data-ttu-id="ea140-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea140-135">-ResourceGroupName</span></span>
<span data-ttu-id="ea140-136">Gibt die Ressourcengruppe der Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="ea140-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="ea140-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea140-137">-Confirm</span></span>
<span data-ttu-id="ea140-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea140-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea140-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea140-139">-WhatIf</span></span>
<span data-ttu-id="ea140-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea140-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea140-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea140-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea140-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea140-142">CommonParameters</span></span>
<span data-ttu-id="ea140-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea140-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea140-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea140-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea140-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea140-145">INPUTS</span></span>

### <span data-ttu-id="ea140-146">Keine</span><span class="sxs-lookup"><span data-stu-id="ea140-146">None</span></span>
<span data-ttu-id="ea140-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ea140-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea140-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea140-148">OUTPUTS</span></span>

### <span data-ttu-id="ea140-149">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="ea140-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="ea140-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea140-150">NOTES</span></span>

## <span data-ttu-id="ea140-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea140-151">RELATED LINKS</span></span>

[<span data-ttu-id="ea140-152">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ea140-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ea140-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ea140-155">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-155">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ea140-156">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ea140-156">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


