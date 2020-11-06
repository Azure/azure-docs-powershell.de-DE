---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479285"
---
# <span data-ttu-id="80a50-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="80a50-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="80a50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80a50-102">SYNOPSIS</span></span>
<span data-ttu-id="80a50-103">Erstellt eine Data Lake Analytics-Berechnungs Richtlinienregel für eine bestimmte Aad-Entität.</span><span class="sxs-lookup"><span data-stu-id="80a50-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80a50-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80a50-105">DESCRIPTION</span></span>
<span data-ttu-id="80a50-106">Das **New-AzureRmDataLakeAnalyticsComputePolicy-** Objekt erstellt die angegebene Compute-Richtlinienregel für eine bestimmte Aad-Entität in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="80a50-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="80a50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80a50-107">EXAMPLES</span></span>

### <span data-ttu-id="80a50-108">Beispiel 1: Erstellen einer COMPUTE-Richtlinie mit nur einer Regel</span><span class="sxs-lookup"><span data-stu-id="80a50-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="80a50-109">Mit diesem Befehl wird eine Richtlinie namens "MyPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" erstellt, die sicherstellt, dass Sie keine Aufgabe mit mehr als 5 Parallelität übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="80a50-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="80a50-110">Beispiel 2: Erstellen einer COMPUTE-Richtlinie mit beiden Regelsätzen</span><span class="sxs-lookup"><span data-stu-id="80a50-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="80a50-111">Dieser Befehl erstellt eine Richtlinie mit dem Namen "MyPolicy" im Konto "contosoadla" für den Benutzer mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3", die sicherstellt, dass Sie keine Aufträge mit mehr als 5 Parallelität oder mit einer Priorität unter 100 übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="80a50-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="80a50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="80a50-112">PARAMETERS</span></span>

### <span data-ttu-id="80a50-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="80a50-113">-Account</span></span>
<span data-ttu-id="80a50-114">Der Name des Kontos, dem die Compute-Richtlinie hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80a50-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="80a50-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="80a50-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="80a50-116">Der maximal unterstützte Grad an Parallelität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="80a50-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="80a50-117">Entweder this, MinPriorityPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80a50-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="80a50-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="80a50-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="80a50-119">Die minimale unterstützte Priorität pro Auftrag für diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="80a50-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="80a50-120">Entweder this, MaxDegreeOfParallelismPerJob oder beide Parameter müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80a50-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="80a50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80a50-121">-Name</span></span>
<span data-ttu-id="80a50-122">Der Name der zu erstellende Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="80a50-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="80a50-123">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="80a50-123">-ObjectId</span></span>
<span data-ttu-id="80a50-124">Die Azure Active Directory-Objekt-ID des Benutzers oder der Gruppe, auf die die Richtlinie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="80a50-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="80a50-125">-Objekttyp</span><span class="sxs-lookup"><span data-stu-id="80a50-125">-ObjectType</span></span>
<span data-ttu-id="80a50-126">Der Azure Active Directory-Objekttyp für die übergebene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="80a50-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="80a50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a50-127">-ResourceGroupName</span></span>
<span data-ttu-id="80a50-128">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="80a50-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="80a50-129">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="80a50-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="80a50-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80a50-130">-Confirm</span></span>
<span data-ttu-id="80a50-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80a50-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a50-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a50-132">-WhatIf</span></span>
<span data-ttu-id="80a50-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80a50-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80a50-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80a50-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a50-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a50-135">-DefaultProfile</span></span>
<span data-ttu-id="80a50-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80a50-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a50-137">CommonParameters</span></span>
<span data-ttu-id="80a50-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a50-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a50-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a50-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80a50-140">INPUTS</span></span>

### <span data-ttu-id="80a50-141">System. String</span><span class="sxs-lookup"><span data-stu-id="80a50-141">System.String</span></span>
<span data-ttu-id="80a50-142">System. GUID System. Int32</span><span class="sxs-lookup"><span data-stu-id="80a50-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="80a50-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80a50-143">OUTPUTS</span></span>

### <span data-ttu-id="80a50-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="80a50-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="80a50-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="80a50-145">NOTES</span></span>

## <span data-ttu-id="80a50-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80a50-146">RELATED LINKS</span></span>

