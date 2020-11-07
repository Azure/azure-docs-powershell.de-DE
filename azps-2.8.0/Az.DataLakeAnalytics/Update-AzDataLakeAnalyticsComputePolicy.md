---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 39c13bd7dd85f15edf1521ef372196b6c7472512
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651580"
---
# <span data-ttu-id="5e917-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5e917-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5e917-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e917-102">SYNOPSIS</span></span>
<span data-ttu-id="5e917-103">Aktualisiert eine Data Lake Analytics-Compute-Richtlinienregel für eine bestimmte Aad-Entität.</span><span class="sxs-lookup"><span data-stu-id="5e917-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="5e917-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e917-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e917-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e917-105">DESCRIPTION</span></span>
<span data-ttu-id="5e917-106">Das **Update-AzDataLakeAnalyticsComputePolicy** aktualisiert die angegebene Compute-Richtlinienregel für eine bestimmte Aad-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="5e917-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5e917-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e917-107">EXAMPLES</span></span>

### <span data-ttu-id="5e917-108">Beispiel 1: Aktualisieren einer Regel in einer COMPUTE-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5e917-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="5e917-109">Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" aktualisiert, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="5e917-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="5e917-110">Beispiel 2: Erstellen einer COMPUTE-Richtlinie mit beiden Regel Updates</span><span class="sxs-lookup"><span data-stu-id="5e917-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="5e917-111">Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" erstellt, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 senden kann.</span><span class="sxs-lookup"><span data-stu-id="5e917-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="5e917-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e917-112">PARAMETERS</span></span>

### <span data-ttu-id="5e917-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="5e917-113">-Account</span></span>
<span data-ttu-id="5e917-114">Der Name des Kontos, in dem die Compute-Richtlinie aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e917-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e917-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e917-115">-DefaultProfile</span></span>
<span data-ttu-id="5e917-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5e917-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e917-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="5e917-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="5e917-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5e917-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="5e917-119">Entweder this, MinPriorityPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e917-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e917-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="5e917-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="5e917-121">Die minimale unterstützte Priorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5e917-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="5e917-122">Entweder this, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e917-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e917-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5e917-123">-Name</span></span>
<span data-ttu-id="5e917-124">Der Name der zu aktualisierende Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5e917-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e917-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e917-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e917-126">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5e917-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="5e917-127">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e917-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="5e917-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e917-128">-Confirm</span></span>
<span data-ttu-id="5e917-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e917-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e917-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e917-130">-WhatIf</span></span>
<span data-ttu-id="5e917-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e917-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e917-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e917-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e917-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e917-133">CommonParameters</span></span>
<span data-ttu-id="5e917-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e917-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e917-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e917-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e917-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e917-136">INPUTS</span></span>

### <span data-ttu-id="5e917-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5e917-137">System.String</span></span>

### <span data-ttu-id="5e917-138">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e917-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5e917-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e917-139">OUTPUTS</span></span>

### <span data-ttu-id="5e917-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5e917-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5e917-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e917-141">NOTES</span></span>

## <span data-ttu-id="5e917-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e917-142">RELATED LINKS</span></span>
