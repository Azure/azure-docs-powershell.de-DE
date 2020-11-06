---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 860b58ce3be37eb2ef2277b627971adb301a02af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499594"
---
# <span data-ttu-id="a2674-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="a2674-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="a2674-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2674-102">SYNOPSIS</span></span>
<span data-ttu-id="a2674-103">Aktualisiert eine Data Lake Analytics-Compute-Richtlinienregel für eine bestimmte Aad-Entität.</span><span class="sxs-lookup"><span data-stu-id="a2674-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2674-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2674-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2674-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2674-105">DESCRIPTION</span></span>
<span data-ttu-id="a2674-106">Das **Update-AzureRmDataLakeAnalyticsComputePolicy** aktualisiert die angegebene Compute-Richtlinienregel für eine bestimmte Aad-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="a2674-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a2674-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2674-107">EXAMPLES</span></span>

### <span data-ttu-id="a2674-108">Beispiel 1: Aktualisieren einer Regel in einer COMPUTE-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a2674-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="a2674-109">Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" aktualisiert, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="a2674-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="a2674-110">Beispiel 2: Erstellen einer COMPUTE-Richtlinie mit beiden Regel Updates</span><span class="sxs-lookup"><span data-stu-id="a2674-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="a2674-111">Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" erstellt, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 senden kann.</span><span class="sxs-lookup"><span data-stu-id="a2674-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="a2674-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2674-112">PARAMETERS</span></span>

### <span data-ttu-id="a2674-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="a2674-113">-Account</span></span>
<span data-ttu-id="a2674-114">Der Name des Kontos, in dem die Compute-Richtlinie aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2674-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="a2674-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2674-115">-DefaultProfile</span></span>
<span data-ttu-id="a2674-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2674-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2674-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="a2674-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="a2674-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a2674-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="a2674-119">Entweder this, MinPriorityPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2674-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="a2674-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="a2674-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="a2674-121">Die minimale unterstützte Priorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a2674-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="a2674-122">Entweder this, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2674-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="a2674-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2674-123">-Name</span></span>
<span data-ttu-id="a2674-124">Der Name der zu aktualisierende Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a2674-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="a2674-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2674-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2674-126">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a2674-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="a2674-127">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2674-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="a2674-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2674-128">-Confirm</span></span>
<span data-ttu-id="a2674-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2674-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2674-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2674-130">-WhatIf</span></span>
<span data-ttu-id="a2674-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2674-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2674-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2674-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2674-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2674-133">CommonParameters</span></span>
<span data-ttu-id="a2674-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2674-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2674-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2674-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2674-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2674-136">INPUTS</span></span>

### <span data-ttu-id="a2674-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a2674-137">System.String</span></span>

### <span data-ttu-id="a2674-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2674-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a2674-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2674-139">OUTPUTS</span></span>

### <span data-ttu-id="a2674-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="a2674-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="a2674-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2674-141">NOTES</span></span>

## <span data-ttu-id="a2674-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2674-142">RELATED LINKS</span></span>
