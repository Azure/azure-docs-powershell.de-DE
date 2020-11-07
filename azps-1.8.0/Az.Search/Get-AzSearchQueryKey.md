---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9283fb0a2fd366029a5ca2bc618daf7ad8a3de3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659486"
---
# <span data-ttu-id="5d95f-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5d95f-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="5d95f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d95f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d95f-103">Ruft den Abfrage Schlüssel (n) des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="5d95f-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="5d95f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d95f-104">SYNTAX</span></span>

### <span data-ttu-id="5d95f-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d95f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d95f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d95f-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d95f-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d95f-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d95f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d95f-108">DESCRIPTION</span></span>
<span data-ttu-id="5d95f-109">Das Cmdlet " **Get-AzSearchQueryKey** " ruft Abfrage Schlüssel (s) des Azure Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="5d95f-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="5d95f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d95f-110">EXAMPLES</span></span>

### <span data-ttu-id="5d95f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d95f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="5d95f-112">Im Beispiel werden alle Abfrage Schlüssel (s) des Azure-Suchdiensts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5d95f-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="5d95f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d95f-113">PARAMETERS</span></span>

### <span data-ttu-id="5d95f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d95f-114">-DefaultProfile</span></span>
<span data-ttu-id="5d95f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d95f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d95f-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5d95f-116">-ParentObject</span></span>
<span data-ttu-id="5d95f-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5d95f-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5d95f-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5d95f-118">-ParentResourceId</span></span>
<span data-ttu-id="5d95f-119">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="5d95f-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5d95f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d95f-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d95f-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d95f-121">Resource Group name.</span></span>

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

### <span data-ttu-id="5d95f-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5d95f-122">-ServiceName</span></span>
<span data-ttu-id="5d95f-123">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5d95f-123">Search Service name.</span></span>

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

### <span data-ttu-id="5d95f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d95f-124">CommonParameters</span></span>
<span data-ttu-id="5d95f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d95f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d95f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d95f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d95f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d95f-127">INPUTS</span></span>

### <span data-ttu-id="5d95f-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5d95f-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="5d95f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5d95f-129">System.String</span></span>

## <span data-ttu-id="5d95f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d95f-130">OUTPUTS</span></span>

### <span data-ttu-id="5d95f-131">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5d95f-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="5d95f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d95f-132">NOTES</span></span>

## <span data-ttu-id="5d95f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d95f-133">RELATED LINKS</span></span>

[<span data-ttu-id="5d95f-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5d95f-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="5d95f-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5d95f-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)