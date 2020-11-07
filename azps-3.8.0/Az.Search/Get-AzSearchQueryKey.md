---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845819"
---
# <span data-ttu-id="53d0c-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="53d0c-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="53d0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="53d0c-103">Ruft den Abfrage Schlüssel (n) des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="53d0c-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="53d0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53d0c-104">SYNTAX</span></span>

### <span data-ttu-id="53d0c-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53d0c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d0c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53d0c-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53d0c-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53d0c-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53d0c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53d0c-108">DESCRIPTION</span></span>
<span data-ttu-id="53d0c-109">Das Cmdlet " **Get-AzSearchQueryKey** " ruft Abfrage Schlüssel (s) des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="53d0c-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="53d0c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53d0c-110">EXAMPLES</span></span>

### <span data-ttu-id="53d0c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53d0c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="53d0c-112">Im Beispiel werden alle Abfrage Schlüssel (s) des Azure-Suchdiensts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="53d0c-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="53d0c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="53d0c-113">PARAMETERS</span></span>

### <span data-ttu-id="53d0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d0c-114">-DefaultProfile</span></span>
<span data-ttu-id="53d0c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53d0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53d0c-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="53d0c-116">-ParentObject</span></span>
<span data-ttu-id="53d0c-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="53d0c-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="53d0c-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="53d0c-118">-ParentResourceId</span></span>
<span data-ttu-id="53d0c-119">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="53d0c-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="53d0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="53d0c-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53d0c-121">Resource Group name.</span></span>

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

### <span data-ttu-id="53d0c-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="53d0c-122">-ServiceName</span></span>
<span data-ttu-id="53d0c-123">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="53d0c-123">Search Service name.</span></span>

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

### <span data-ttu-id="53d0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d0c-124">CommonParameters</span></span>
<span data-ttu-id="53d0c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d0c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53d0c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d0c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53d0c-127">INPUTS</span></span>

### <span data-ttu-id="53d0c-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="53d0c-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="53d0c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="53d0c-129">System.String</span></span>

## <span data-ttu-id="53d0c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53d0c-130">OUTPUTS</span></span>

### <span data-ttu-id="53d0c-131">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="53d0c-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="53d0c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="53d0c-132">NOTES</span></span>

## <span data-ttu-id="53d0c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53d0c-133">RELATED LINKS</span></span>

[<span data-ttu-id="53d0c-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="53d0c-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="53d0c-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="53d0c-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)