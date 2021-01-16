---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298099"
---
# <span data-ttu-id="52825-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-101">Set-AzSearchService</span></span>

## <span data-ttu-id="52825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52825-102">SYNOPSIS</span></span>
<span data-ttu-id="52825-103">Aktualisieren Sie einen Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="52825-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="52825-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52825-104">SYNTAX</span></span>

### <span data-ttu-id="52825-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52825-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52825-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52825-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52825-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52825-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52825-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52825-108">DESCRIPTION</span></span>
<span data-ttu-id="52825-109">Das **Cmdlet Set-AzSearchService** ändert einen Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="52825-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="52825-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52825-110">EXAMPLES</span></span>

### <span data-ttu-id="52825-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52825-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="52825-112">Im Beispiel werden die Partitions- und Replikatanzahl des Azure Search-Diensts in "2" geändert.</span><span class="sxs-lookup"><span data-stu-id="52825-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="52825-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52825-113">PARAMETERS</span></span>

### <span data-ttu-id="52825-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52825-114">-DefaultProfile</span></span>
<span data-ttu-id="52825-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52825-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52825-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52825-116">-InputObject</span></span>
<span data-ttu-id="52825-117">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="52825-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52825-118">-Name</span><span class="sxs-lookup"><span data-stu-id="52825-118">-Name</span></span>
<span data-ttu-id="52825-119">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="52825-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52825-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="52825-120">-PartitionCount</span></span>
<span data-ttu-id="52825-121">Anzahl der Suchdienstpartitionen.</span><span class="sxs-lookup"><span data-stu-id="52825-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="52825-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="52825-122">-ReplicaCount</span></span>
<span data-ttu-id="52825-123">Anzahl der Suchdienstreplikate.</span><span class="sxs-lookup"><span data-stu-id="52825-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="52825-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52825-124">-ResourceGroupName</span></span>
<span data-ttu-id="52825-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="52825-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52825-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52825-126">-ResourceId</span></span>
<span data-ttu-id="52825-127">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="52825-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52825-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52825-128">-Confirm</span></span>
<span data-ttu-id="52825-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52825-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52825-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="52825-130">-WhatIf</span></span>
<span data-ttu-id="52825-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52825-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52825-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52825-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52825-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52825-133">CommonParameters</span></span>
<span data-ttu-id="52825-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52825-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52825-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52825-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52825-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52825-136">INPUTS</span></span>

### <span data-ttu-id="52825-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="52825-138">System.String</span><span class="sxs-lookup"><span data-stu-id="52825-138">System.String</span></span>

## <span data-ttu-id="52825-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52825-139">OUTPUTS</span></span>

### <span data-ttu-id="52825-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="52825-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52825-141">NOTES</span></span>

## <span data-ttu-id="52825-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52825-142">RELATED LINKS</span></span>

[<span data-ttu-id="52825-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="52825-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="52825-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="52825-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)