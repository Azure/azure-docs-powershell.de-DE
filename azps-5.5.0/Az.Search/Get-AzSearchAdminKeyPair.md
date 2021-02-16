---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: e6f2495392eed73e5576d8502f86a08e325337f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150844"
---
# <span data-ttu-id="4dd56-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="4dd56-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="4dd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd56-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd56-103">Ruft das Administratorschlüsselpaar des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4dd56-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4dd56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dd56-104">SYNTAX</span></span>

### <span data-ttu-id="4dd56-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dd56-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dd56-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd56-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dd56-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd56-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dd56-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dd56-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd56-109">Das **Cmdlet "Get-AzSearchAdminKeyPair"** ruft das Administratorschlüsselpaar des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4dd56-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4dd56-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dd56-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd56-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dd56-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="4dd56-112">Das Beispiel ruft das Administratorschlüsselpaar des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4dd56-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4dd56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dd56-113">PARAMETERS</span></span>

### <span data-ttu-id="4dd56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd56-114">-DefaultProfile</span></span>
<span data-ttu-id="4dd56-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dd56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd56-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4dd56-116">-ParentObject</span></span>
<span data-ttu-id="4dd56-117">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="4dd56-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="4dd56-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd56-118">-ParentResourceId</span></span>
<span data-ttu-id="4dd56-119">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="4dd56-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4dd56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd56-120">-ResourceGroupName</span></span>
<span data-ttu-id="4dd56-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4dd56-121">Resource Group name.</span></span>

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

### <span data-ttu-id="4dd56-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4dd56-122">-ServiceName</span></span>
<span data-ttu-id="4dd56-123">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="4dd56-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="4dd56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd56-124">CommonParameters</span></span>
<span data-ttu-id="4dd56-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd56-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dd56-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd56-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dd56-127">INPUTS</span></span>

### <span data-ttu-id="4dd56-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4dd56-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4dd56-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4dd56-129">System.String</span></span>

## <span data-ttu-id="4dd56-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dd56-130">OUTPUTS</span></span>

### <span data-ttu-id="4dd56-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="4dd56-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="4dd56-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4dd56-132">NOTES</span></span>

## <span data-ttu-id="4dd56-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4dd56-133">RELATED LINKS</span></span>

[<span data-ttu-id="4dd56-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="4dd56-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
