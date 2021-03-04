---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 7cd9231134b7b78d51a9a86777c54dd99e1ffa90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937024"
---
# <span data-ttu-id="0fca4-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0fca4-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0fca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fca4-102">SYNOPSIS</span></span>
<span data-ttu-id="0fca4-103">Erstellt eine Data Lake Analytics-Computerichtlinienregel für eine bestimmte AAD-Entität.</span><span class="sxs-lookup"><span data-stu-id="0fca4-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="0fca4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fca4-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fca4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fca4-105">DESCRIPTION</span></span>
<span data-ttu-id="0fca4-106">Die **New-AzDataLakeAnalyticsComputePolicy** erstellt die angegebene Computerichtlinienregel für eine bestimmte AAD-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="0fca4-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0fca4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fca4-107">EXAMPLES</span></span>

### <span data-ttu-id="0fca4-108">Beispiel 1: Erstellen einer Computerichtlinie mit nur einer Regel</span><span class="sxs-lookup"><span data-stu-id="0fca4-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="0fca4-109">Mit diesem Befehl wird eine Richtlinie mit dem Namen "myPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass er keinen Auftrag mit mehr als 5 Analyseeinheiten übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="0fca4-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="0fca4-110">Beispiel 2: Erstellen einer Computerichtlinie mit beiden Festgelegten Regeln</span><span class="sxs-lookup"><span data-stu-id="0fca4-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="0fca4-111">Mit diesem Befehl wird eine Richtlinie mit dem Namen "myPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass keine Aufgaben mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0fca4-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="0fca4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0fca4-112">PARAMETERS</span></span>

### <span data-ttu-id="0fca4-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="0fca4-113">-Account</span></span>
<span data-ttu-id="0fca4-114">Name des Kontos, dem die Datenverarbeitungsrichtlinie hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fca4-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="0fca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fca4-115">-DefaultProfile</span></span>
<span data-ttu-id="0fca4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0fca4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fca4-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="0fca4-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="0fca4-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0fca4-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="0fca4-119">Entweder dies, MinPriorityPerJob, oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0fca4-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0fca4-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="0fca4-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="0fca4-121">Die unterstützte Mindestpriorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0fca4-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="0fca4-122">Entweder dies ist MaxAnalyticsUnitsPerJob, oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0fca4-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0fca4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0fca4-123">-Name</span></span>
<span data-ttu-id="0fca4-124">Name der zu erstellende Datenverarbeitungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0fca4-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="0fca4-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0fca4-125">-ObjectId</span></span>
<span data-ttu-id="0fca4-126">Die Azure Active Directory-Objekt-ID für den Benutzer oder die Gruppe, auf die die Richtlinie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fca4-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="0fca4-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="0fca4-127">-ObjectType</span></span>
<span data-ttu-id="0fca4-128">Der Azure Active Directory-Objekttyp für die übergebene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="0fca4-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="0fca4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fca4-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fca4-130">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="0fca4-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="0fca4-131">Optional und versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fca4-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="0fca4-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fca4-132">-Confirm</span></span>
<span data-ttu-id="0fca4-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fca4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fca4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fca4-134">-WhatIf</span></span>
<span data-ttu-id="0fca4-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fca4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fca4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fca4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fca4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fca4-137">CommonParameters</span></span>
<span data-ttu-id="0fca4-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fca4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fca4-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fca4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fca4-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fca4-140">INPUTS</span></span>

### <span data-ttu-id="0fca4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0fca4-141">System.String</span></span>

### <span data-ttu-id="0fca4-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0fca4-142">System.Guid</span></span>

### <span data-ttu-id="0fca4-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0fca4-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0fca4-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fca4-144">OUTPUTS</span></span>

### <span data-ttu-id="0fca4-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0fca4-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0fca4-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0fca4-146">NOTES</span></span>

## <span data-ttu-id="0fca4-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0fca4-147">RELATED LINKS</span></span>
