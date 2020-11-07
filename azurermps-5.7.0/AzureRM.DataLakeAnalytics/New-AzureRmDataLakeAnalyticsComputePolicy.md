---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: fad4a56f9fb4d46ac1b9ab9878760e46f8a20746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662582"
---
# <span data-ttu-id="170f6-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="170f6-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="170f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="170f6-102">SYNOPSIS</span></span>
<span data-ttu-id="170f6-103">Erstellt eine Data Lake Analytics-Berechnungs Richtlinienregel für eine bestimmte Aad-Entität.</span><span class="sxs-lookup"><span data-stu-id="170f6-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="170f6-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="170f6-105">DESCRIPTION</span></span>
<span data-ttu-id="170f6-106">Das **New-AzureRmDataLakeAnalyticsComputePolicy-** Objekt erstellt die angegebene Compute-Richtlinienregel für eine bestimmte Aad-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="170f6-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="170f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="170f6-107">EXAMPLES</span></span>

### <span data-ttu-id="170f6-108">Beispiel 1: Erstellen einer COMPUTE-Richtlinie mit nur einer Regel</span><span class="sxs-lookup"><span data-stu-id="170f6-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="170f6-109">Mit diesem Befehl wird eine Richtlinie namens "MyPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass Sie keine Aufträge mit mehr als 5 Analyseeinheiten übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="170f6-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="170f6-110">Beispiel 2: Erstellen einer COMPUTE-Richtlinie mit beiden Regelsätzen</span><span class="sxs-lookup"><span data-stu-id="170f6-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="170f6-111">Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass Sie keine Aufträge mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 einreichen können.</span><span class="sxs-lookup"><span data-stu-id="170f6-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="170f6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="170f6-112">PARAMETERS</span></span>

### <span data-ttu-id="170f6-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="170f6-113">-Account</span></span>
<span data-ttu-id="170f6-114">Der Name des Kontos, dem die Compute-Richtlinie hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="170f6-114">Name of the account to add the compute policy to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170f6-115">-DefaultProfile</span></span>
<span data-ttu-id="170f6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="170f6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="170f6-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="170f6-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="170f6-118">Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="170f6-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="170f6-119">Entweder this, MinPriorityPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="170f6-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="170f6-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="170f6-121">Die minimale unterstützte Priorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="170f6-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="170f6-122">Entweder this, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="170f6-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="170f6-123">-Name</span></span>
<span data-ttu-id="170f6-124">Der Name der zu erstellende Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="170f6-124">Name of the compute policy to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-125">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="170f6-125">-ObjectId</span></span>
<span data-ttu-id="170f6-126">Die Azure Active Directory-Objekt-ID des Benutzers oder der Gruppe, auf die die Richtlinie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="170f6-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-127">-Objekttyp</span><span class="sxs-lookup"><span data-stu-id="170f6-127">-ObjectType</span></span>
<span data-ttu-id="170f6-128">Der Azure Active Directory-Objekttyp für die übergebene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="170f6-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170f6-129">-ResourceGroupName</span></span>
<span data-ttu-id="170f6-130">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="170f6-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="170f6-131">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="170f6-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="170f6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="170f6-132">-Confirm</span></span>
<span data-ttu-id="170f6-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="170f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170f6-134">-WhatIf</span></span>
<span data-ttu-id="170f6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170f6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="170f6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="170f6-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170f6-137">CommonParameters</span></span>
<span data-ttu-id="170f6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170f6-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170f6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="170f6-140">INPUTS</span></span>

### <span data-ttu-id="170f6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="170f6-141">System.String</span></span>
<span data-ttu-id="170f6-142">System. GUID System. Int32</span><span class="sxs-lookup"><span data-stu-id="170f6-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="170f6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="170f6-143">OUTPUTS</span></span>

### <span data-ttu-id="170f6-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="170f6-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="170f6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="170f6-145">NOTES</span></span>

## <span data-ttu-id="170f6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="170f6-146">RELATED LINKS</span></span>

