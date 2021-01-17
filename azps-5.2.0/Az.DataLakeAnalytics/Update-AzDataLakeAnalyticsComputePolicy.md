---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372838"
---
# <span data-ttu-id="aac0d-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="aac0d-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="aac0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac0d-102">SYNOPSIS</span></span>
<span data-ttu-id="aac0d-103">Aktualisiert eine Data Lake Analytics-Rechenrichtlinienregel für eine bestimmte AAD-Entität.</span><span class="sxs-lookup"><span data-stu-id="aac0d-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="aac0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aac0d-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac0d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aac0d-105">DESCRIPTION</span></span>
<span data-ttu-id="aac0d-106">Das **Update-AzDataLakeAnalyticsComputePolicy** aktualisiert die angegebene Berechnungsrichtlinienregel für eine bestimmte AAD-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="aac0d-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="aac0d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aac0d-107">EXAMPLES</span></span>

### <span data-ttu-id="aac0d-108">Beispiel 1: Aktualisieren einer Regel in einer Berechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="aac0d-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="aac0d-109">Mit diesem Befehl wird die Richtlinie "myPolicy" im Konto "contosoadla" aktualisiert, um sicherzustellen, dass der Benutzer keinen Auftrag mit mehr als 5 Analyseeinheiten übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="aac0d-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="aac0d-110">Beispiel 2: Erstellen einer Berechnungsrichtlinie mit aktualisierung beider Regeln</span><span class="sxs-lookup"><span data-stu-id="aac0d-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="aac0d-111">Mit diesem Befehl wird eine Richtlinie namens "myPolicy" im Konto "contosoadla" erstellt, um sicherzustellen, dass der Benutzer keine Aufgaben mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="aac0d-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="aac0d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aac0d-112">PARAMETERS</span></span>

### <span data-ttu-id="aac0d-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="aac0d-113">-Account</span></span>
<span data-ttu-id="aac0d-114">Name des Kontos, in dem die Berechnungsrichtlinie aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aac0d-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="aac0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac0d-115">-DefaultProfile</span></span>
<span data-ttu-id="aac0d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aac0d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aac0d-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="aac0d-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="aac0d-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="aac0d-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="aac0d-119">Entweder dieser, "MinPriorityPerJob" oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aac0d-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="aac0d-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="aac0d-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="aac0d-121">Die unterstützte Mindestpriorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="aac0d-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="aac0d-122">Entweder diese, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aac0d-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="aac0d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aac0d-123">-Name</span></span>
<span data-ttu-id="aac0d-124">Name der zu aktualisierende Berechnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="aac0d-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="aac0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="aac0d-126">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="aac0d-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="aac0d-127">Optional und wird versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="aac0d-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="aac0d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aac0d-128">-Confirm</span></span>
<span data-ttu-id="aac0d-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aac0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac0d-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aac0d-130">-WhatIf</span></span>
<span data-ttu-id="aac0d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aac0d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aac0d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aac0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac0d-133">CommonParameters</span></span>
<span data-ttu-id="aac0d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac0d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac0d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac0d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aac0d-136">INPUTS</span></span>

### <span data-ttu-id="aac0d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aac0d-137">System.String</span></span>

### <span data-ttu-id="aac0d-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aac0d-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aac0d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aac0d-139">OUTPUTS</span></span>

### <span data-ttu-id="aac0d-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="aac0d-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="aac0d-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aac0d-141">NOTES</span></span>

## <span data-ttu-id="aac0d-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aac0d-142">RELATED LINKS</span></span>
