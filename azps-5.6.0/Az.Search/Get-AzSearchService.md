---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: f4f360cc7fd9151735f131878565a09933f1be54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924456"
---
# <span data-ttu-id="b004e-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b004e-101">Get-AzSearchService</span></span>

## <span data-ttu-id="b004e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b004e-102">SYNOPSIS</span></span>
<span data-ttu-id="b004e-103">Ruft einen Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="b004e-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b004e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b004e-104">SYNTAX</span></span>

### <span data-ttu-id="b004e-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b004e-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b004e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b004e-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b004e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b004e-107">DESCRIPTION</span></span>
<span data-ttu-id="b004e-108">Das **Get-AzSearchService-Cmdlet** ruft den angegebenen Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="b004e-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b004e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b004e-109">EXAMPLES</span></span>

### <span data-ttu-id="b004e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b004e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="b004e-111">Holen Sie sich einen Azure Cognitive Search-Dienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="b004e-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="b004e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b004e-112">PARAMETERS</span></span>

### <span data-ttu-id="b004e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b004e-113">-DefaultProfile</span></span>
<span data-ttu-id="b004e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b004e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b004e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b004e-115">-Name</span></span>
<span data-ttu-id="b004e-116">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="b004e-116">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b004e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b004e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b004e-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b004e-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b004e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b004e-119">-ResourceId</span></span>
<span data-ttu-id="b004e-120">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="b004e-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b004e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b004e-121">CommonParameters</span></span>
<span data-ttu-id="b004e-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b004e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b004e-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b004e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b004e-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b004e-124">INPUTS</span></span>

### <span data-ttu-id="b004e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b004e-125">System.String</span></span>

## <span data-ttu-id="b004e-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b004e-126">OUTPUTS</span></span>

### <span data-ttu-id="b004e-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b004e-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b004e-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b004e-128">NOTES</span></span>

## <span data-ttu-id="b004e-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b004e-129">RELATED LINKS</span></span>

[<span data-ttu-id="b004e-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b004e-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="b004e-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b004e-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="b004e-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b004e-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)