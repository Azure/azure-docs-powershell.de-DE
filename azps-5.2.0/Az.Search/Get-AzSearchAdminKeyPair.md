---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370599"
---
# <span data-ttu-id="4b15d-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="4b15d-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="4b15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b15d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b15d-103">Ruft das Administratorschlüsselpaar des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4b15d-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="4b15d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b15d-104">SYNTAX</span></span>

### <span data-ttu-id="4b15d-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b15d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b15d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b15d-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b15d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b15d-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b15d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b15d-108">DESCRIPTION</span></span>
<span data-ttu-id="4b15d-109">Das **Cmdlet "Get-AzSearchAdminKeyPair"** ruft das Administratorschlüsselpaar des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4b15d-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="4b15d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b15d-110">EXAMPLES</span></span>

### <span data-ttu-id="4b15d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b15d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="4b15d-112">Das Beispiel ruft das Administratorschlüsselpaar des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="4b15d-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="4b15d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b15d-113">PARAMETERS</span></span>

### <span data-ttu-id="4b15d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b15d-114">-DefaultProfile</span></span>
<span data-ttu-id="4b15d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b15d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b15d-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4b15d-116">-ParentObject</span></span>
<span data-ttu-id="4b15d-117">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="4b15d-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="4b15d-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4b15d-118">-ParentResourceId</span></span>
<span data-ttu-id="4b15d-119">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4b15d-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4b15d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b15d-120">-ResourceGroupName</span></span>
<span data-ttu-id="4b15d-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4b15d-121">Resource Group name.</span></span>

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

### <span data-ttu-id="4b15d-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4b15d-122">-ServiceName</span></span>
<span data-ttu-id="4b15d-123">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="4b15d-123">Search Service name.</span></span>

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

### <span data-ttu-id="4b15d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b15d-124">CommonParameters</span></span>
<span data-ttu-id="4b15d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b15d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b15d-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b15d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b15d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b15d-127">INPUTS</span></span>

### <span data-ttu-id="4b15d-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4b15d-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4b15d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4b15d-129">System.String</span></span>

## <span data-ttu-id="4b15d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b15d-130">OUTPUTS</span></span>

### <span data-ttu-id="4b15d-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="4b15d-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="4b15d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b15d-132">NOTES</span></span>

## <span data-ttu-id="4b15d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b15d-133">RELATED LINKS</span></span>

[<span data-ttu-id="4b15d-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="4b15d-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
