---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166862"
---
# <span data-ttu-id="b6e19-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="b6e19-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="b6e19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6e19-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e19-103">Ruft das Administratorschlüssel Paar des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="b6e19-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="b6e19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6e19-104">SYNTAX</span></span>

### <span data-ttu-id="b6e19-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6e19-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e19-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e19-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6e19-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e19-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6e19-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6e19-108">DESCRIPTION</span></span>
<span data-ttu-id="b6e19-109">Das Cmdlet " **Get-AzSearchAdminKeyPair** " Ruft das Administratorschlüssel Paar des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="b6e19-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="b6e19-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6e19-110">EXAMPLES</span></span>

### <span data-ttu-id="b6e19-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6e19-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="b6e19-112">Im Beispiel wird ein Administratorschlüssel Paar des Azure-Suchdiensts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b6e19-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="b6e19-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6e19-113">PARAMETERS</span></span>

### <span data-ttu-id="b6e19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e19-114">-DefaultProfile</span></span>
<span data-ttu-id="b6e19-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6e19-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e19-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6e19-116">-ParentObject</span></span>
<span data-ttu-id="b6e19-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b6e19-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="b6e19-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e19-118">-ParentResourceId</span></span>
<span data-ttu-id="b6e19-119">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="b6e19-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b6e19-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e19-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6e19-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b6e19-121">Resource Group name.</span></span>

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

### <span data-ttu-id="b6e19-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b6e19-122">-ServiceName</span></span>
<span data-ttu-id="b6e19-123">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="b6e19-123">Search Service name.</span></span>

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

### <span data-ttu-id="b6e19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e19-124">CommonParameters</span></span>
<span data-ttu-id="b6e19-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e19-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e19-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e19-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6e19-127">INPUTS</span></span>

### <span data-ttu-id="b6e19-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b6e19-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b6e19-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6e19-129">System.String</span></span>

## <span data-ttu-id="b6e19-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6e19-130">OUTPUTS</span></span>

### <span data-ttu-id="b6e19-131">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b6e19-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="b6e19-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6e19-132">NOTES</span></span>

## <span data-ttu-id="b6e19-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6e19-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6e19-134">Neu – AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b6e19-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
