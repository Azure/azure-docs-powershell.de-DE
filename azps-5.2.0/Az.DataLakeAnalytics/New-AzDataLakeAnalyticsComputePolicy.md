---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297563"
---
# <span data-ttu-id="91ce3-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="91ce3-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="91ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="91ce3-103">Erstellt eine Data Lake Analytics-Rechenrichtlinienregel für eine bestimmte AAD-Entität.</span><span class="sxs-lookup"><span data-stu-id="91ce3-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="91ce3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91ce3-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ce3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="91ce3-106">Die **New-AzDataLakeAnalyticsComputePolicy** erstellt die angegebene Berechnungsrichtlinienregel für eine bestimmte AAD-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="91ce3-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="91ce3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="91ce3-108">Beispiel 1: Erstellen einer Berechnungsrichtlinie mit nur einer Regel</span><span class="sxs-lookup"><span data-stu-id="91ce3-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="91ce3-109">Mit diesem Befehl wird eine Richtlinie namens "myPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass er keinen Auftrag mit mehr als 5 Analyseeinheiten übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="91ce3-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="91ce3-110">Beispiel 2: Erstellen einer Berechnungsrichtlinie mit beiden festgelegten Regeln</span><span class="sxs-lookup"><span data-stu-id="91ce3-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="91ce3-111">Mit diesem Befehl wird eine Richtlinie namens "myPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass keine Aufgaben mit mehr als 5 Analyseeinheiten oder einer Priorität kleiner als 100 übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="91ce3-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="91ce3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91ce3-112">PARAMETERS</span></span>

### <span data-ttu-id="91ce3-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="91ce3-113">-Account</span></span>
<span data-ttu-id="91ce3-114">Name des Kontos, dem die Berechnungsrichtlinie hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91ce3-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="91ce3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ce3-115">-DefaultProfile</span></span>
<span data-ttu-id="91ce3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="91ce3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91ce3-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="91ce3-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="91ce3-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="91ce3-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="91ce3-119">Entweder dieser, "MinPriorityPerJob" oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="91ce3-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="91ce3-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="91ce3-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="91ce3-121">Die unterstützte Mindestpriorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="91ce3-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="91ce3-122">Entweder diese, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="91ce3-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="91ce3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="91ce3-123">-Name</span></span>
<span data-ttu-id="91ce3-124">Name der zu erstellende Berechnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="91ce3-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="91ce3-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="91ce3-125">-ObjectId</span></span>
<span data-ttu-id="91ce3-126">Die Azure Active Directory-Objekt-ID, auf die der Benutzer oder die Gruppe die Richtlinie anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="91ce3-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ce3-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="91ce3-127">-ObjectType</span></span>
<span data-ttu-id="91ce3-128">Der Azure Active Directory-Objekttyp für die übergebene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="91ce3-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ce3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ce3-129">-ResourceGroupName</span></span>
<span data-ttu-id="91ce3-130">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="91ce3-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="91ce3-131">Optional und wird versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="91ce3-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="91ce3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91ce3-132">-Confirm</span></span>
<span data-ttu-id="91ce3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91ce3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ce3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="91ce3-134">-WhatIf</span></span>
<span data-ttu-id="91ce3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91ce3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91ce3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91ce3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ce3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ce3-137">CommonParameters</span></span>
<span data-ttu-id="91ce3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ce3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ce3-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ce3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ce3-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91ce3-140">INPUTS</span></span>

### <span data-ttu-id="91ce3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="91ce3-141">System.String</span></span>

### <span data-ttu-id="91ce3-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="91ce3-142">System.Guid</span></span>

### <span data-ttu-id="91ce3-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91ce3-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="91ce3-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91ce3-144">OUTPUTS</span></span>

### <span data-ttu-id="91ce3-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="91ce3-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="91ce3-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91ce3-146">NOTES</span></span>

## <span data-ttu-id="91ce3-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91ce3-147">RELATED LINKS</span></span>
