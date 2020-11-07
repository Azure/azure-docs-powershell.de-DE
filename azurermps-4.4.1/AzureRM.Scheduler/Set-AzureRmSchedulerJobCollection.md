---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663825"
---
# <span data-ttu-id="69c25-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="69c25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69c25-102">SYNOPSIS</span></span>
<span data-ttu-id="69c25-103">Ändert eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="69c25-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69c25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69c25-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69c25-105">DESCRIPTION</span></span>
<span data-ttu-id="69c25-106">Das Cmdlet " **Satz-AzureRmSchedulerJobCollection** " ändert eine Auftrags Sammlung in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="69c25-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="69c25-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69c25-107">EXAMPLES</span></span>

## <span data-ttu-id="69c25-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69c25-108">PARAMETERS</span></span>

### <span data-ttu-id="69c25-109">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="69c25-109">-Frequency</span></span>
<span data-ttu-id="69c25-110">Gibt die maximale Häufigkeit an, die Sie für einen beliebigen Job in der Auftrags Sammlung angeben können.</span><span class="sxs-lookup"><span data-stu-id="69c25-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="69c25-111">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="69c25-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69c25-112">Minuten</span><span class="sxs-lookup"><span data-stu-id="69c25-112">Minute</span></span> 
- <span data-ttu-id="69c25-113">Stunde</span><span class="sxs-lookup"><span data-stu-id="69c25-113">Hour</span></span> 
- <span data-ttu-id="69c25-114">Tag</span><span class="sxs-lookup"><span data-stu-id="69c25-114">Day</span></span> 
- <span data-ttu-id="69c25-115">Woche</span><span class="sxs-lookup"><span data-stu-id="69c25-115">Week</span></span> 
- <span data-ttu-id="69c25-116">Monat</span><span class="sxs-lookup"><span data-stu-id="69c25-116">Month</span></span>

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

### <span data-ttu-id="69c25-117">-Intervall</span><span class="sxs-lookup"><span data-stu-id="69c25-117">-Interval</span></span>
<span data-ttu-id="69c25-118">Gibt ein Wiederholungsintervall an.</span><span class="sxs-lookup"><span data-stu-id="69c25-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="69c25-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="69c25-119">-JobCollectionName</span></span>
<span data-ttu-id="69c25-120">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="69c25-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="69c25-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="69c25-121">-Location</span></span>
<span data-ttu-id="69c25-122">Gibt den Azure-Bereich an, in dem die Auftrags Sammlung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="69c25-122">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="69c25-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="69c25-123">-MaxJobCount</span></span>
<span data-ttu-id="69c25-124">Gibt die maximale Anzahl von Aufträgen an, die Sie in der Auftrags Sammlung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="69c25-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="69c25-125">Der Höchstbetrag hängt vom Plan ab, der vom *Plan* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69c25-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="69c25-126">-Plan</span><span class="sxs-lookup"><span data-stu-id="69c25-126">-Plan</span></span>
<span data-ttu-id="69c25-127">Gibt den Plan für die Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="69c25-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="69c25-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="69c25-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69c25-129">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="69c25-129">Free</span></span> 
- <span data-ttu-id="69c25-130">Standard</span><span class="sxs-lookup"><span data-stu-id="69c25-130">Standard</span></span> 
- <span data-ttu-id="69c25-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="69c25-131">P10Premium</span></span> 
- <span data-ttu-id="69c25-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="69c25-132">P20Premium</span></span>

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

### <span data-ttu-id="69c25-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c25-133">-ResourceGroupName</span></span>
<span data-ttu-id="69c25-134">Gibt die Ressourcengruppe der Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="69c25-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="69c25-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69c25-135">-Confirm</span></span>
<span data-ttu-id="69c25-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69c25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c25-137">-WhatIf</span></span>
<span data-ttu-id="69c25-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69c25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c25-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69c25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c25-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c25-140">-DefaultProfile</span></span>
<span data-ttu-id="69c25-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69c25-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c25-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c25-142">CommonParameters</span></span>
<span data-ttu-id="69c25-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c25-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c25-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c25-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c25-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69c25-145">INPUTS</span></span>

## <span data-ttu-id="69c25-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69c25-146">OUTPUTS</span></span>

### <span data-ttu-id="69c25-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="69c25-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="69c25-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="69c25-148">NOTES</span></span>

## <span data-ttu-id="69c25-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69c25-149">RELATED LINKS</span></span>

[<span data-ttu-id="69c25-150">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="69c25-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="69c25-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="69c25-153">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="69c25-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="69c25-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


