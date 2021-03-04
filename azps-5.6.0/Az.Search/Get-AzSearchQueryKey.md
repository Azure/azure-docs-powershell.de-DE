---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937360"
---
# <span data-ttu-id="d0c5e-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d0c5e-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="d0c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c5e-103">Ruft Abfrageschlüssel des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d0c5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0c5e-104">SYNTAX</span></span>

### <span data-ttu-id="d0c5e-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0c5e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c5e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0c5e-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0c5e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0c5e-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c5e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0c5e-108">DESCRIPTION</span></span>
<span data-ttu-id="d0c5e-109">Das **Get-AzSearchQueryKey-Cmdlet** ruft Abfrageschlüssel des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d0c5e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0c5e-110">EXAMPLES</span></span>

### <span data-ttu-id="d0c5e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0c5e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="d0c5e-112">Das Beispiel ruft alle Abfrageschlüssel des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d0c5e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d0c5e-113">PARAMETERS</span></span>

### <span data-ttu-id="d0c5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c5e-114">-DefaultProfile</span></span>
<span data-ttu-id="d0c5e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c5e-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0c5e-116">-ParentObject</span></span>
<span data-ttu-id="d0c5e-117">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c5e-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0c5e-118">-ParentResourceId</span></span>
<span data-ttu-id="d0c5e-119">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-119">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0c5e-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-121">Resource Group name.</span></span>

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

### <span data-ttu-id="d0c5e-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d0c5e-122">-ServiceName</span></span>
<span data-ttu-id="d0c5e-123">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d0c5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c5e-124">CommonParameters</span></span>
<span data-ttu-id="d0c5e-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c5e-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0c5e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c5e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0c5e-127">INPUTS</span></span>

### <span data-ttu-id="d0c5e-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d0c5e-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d0c5e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d0c5e-129">System.String</span></span>

## <span data-ttu-id="d0c5e-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0c5e-130">OUTPUTS</span></span>

### <span data-ttu-id="d0c5e-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d0c5e-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="d0c5e-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d0c5e-132">NOTES</span></span>

## <span data-ttu-id="d0c5e-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d0c5e-133">RELATED LINKS</span></span>

[<span data-ttu-id="d0c5e-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d0c5e-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="d0c5e-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d0c5e-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)