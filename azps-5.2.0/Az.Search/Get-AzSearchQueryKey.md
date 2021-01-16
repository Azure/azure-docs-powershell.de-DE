---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294688"
---
# <span data-ttu-id="59b49-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="59b49-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="59b49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b49-102">SYNOPSIS</span></span>
<span data-ttu-id="59b49-103">Ruft Abfrageschlüssel des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="59b49-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="59b49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59b49-104">SYNTAX</span></span>

### <span data-ttu-id="59b49-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59b49-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b49-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b49-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59b49-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b49-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59b49-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59b49-108">DESCRIPTION</span></span>
<span data-ttu-id="59b49-109">Das **Cmdlet "Get-AzSearchQueryKey"** ruft die Abfrageschlüssel des Azure -Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="59b49-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="59b49-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59b49-110">EXAMPLES</span></span>

### <span data-ttu-id="59b49-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59b49-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="59b49-112">Das Beispiel ruft alle Abfrageschlüssel des Azure Search Service(en) ab.</span><span class="sxs-lookup"><span data-stu-id="59b49-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="59b49-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59b49-113">PARAMETERS</span></span>

### <span data-ttu-id="59b49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b49-114">-DefaultProfile</span></span>
<span data-ttu-id="59b49-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59b49-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b49-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="59b49-116">-ParentObject</span></span>
<span data-ttu-id="59b49-117">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="59b49-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="59b49-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59b49-118">-ParentResourceId</span></span>
<span data-ttu-id="59b49-119">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="59b49-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="59b49-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b49-120">-ResourceGroupName</span></span>
<span data-ttu-id="59b49-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="59b49-121">Resource Group name.</span></span>

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

### <span data-ttu-id="59b49-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="59b49-122">-ServiceName</span></span>
<span data-ttu-id="59b49-123">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="59b49-123">Search Service name.</span></span>

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

### <span data-ttu-id="59b49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b49-124">CommonParameters</span></span>
<span data-ttu-id="59b49-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b49-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b49-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b49-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59b49-127">INPUTS</span></span>

### <span data-ttu-id="59b49-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="59b49-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="59b49-129">System.String</span><span class="sxs-lookup"><span data-stu-id="59b49-129">System.String</span></span>

## <span data-ttu-id="59b49-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59b49-130">OUTPUTS</span></span>

### <span data-ttu-id="59b49-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="59b49-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="59b49-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59b49-132">NOTES</span></span>

## <span data-ttu-id="59b49-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59b49-133">RELATED LINKS</span></span>

[<span data-ttu-id="59b49-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="59b49-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="59b49-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="59b49-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)