---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499418"
---
# <span data-ttu-id="461d0-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="461d0-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="461d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="461d0-102">SYNOPSIS</span></span>
<span data-ttu-id="461d0-103">Ruft das Administratorschlüssel Paar des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="461d0-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="461d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="461d0-104">SYNTAX</span></span>

### <span data-ttu-id="461d0-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="461d0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="461d0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="461d0-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="461d0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="461d0-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="461d0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="461d0-108">DESCRIPTION</span></span>
<span data-ttu-id="461d0-109">Das Cmdlet " **Get-AzureRmSearchAdminKeyPair** " Ruft das Administratorschlüssel Paar des Azure-Suchdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="461d0-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="461d0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="461d0-110">EXAMPLES</span></span>

### <span data-ttu-id="461d0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="461d0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="461d0-112">Im Beispiel wird ein Administratorschlüssel Paar des Azure-Suchdiensts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="461d0-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="461d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="461d0-113">PARAMETERS</span></span>

### <span data-ttu-id="461d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461d0-114">-DefaultProfile</span></span>
<span data-ttu-id="461d0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="461d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="461d0-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="461d0-116">-ParentObject</span></span>
<span data-ttu-id="461d0-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="461d0-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="461d0-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="461d0-118">-ParentResourceId</span></span>
<span data-ttu-id="461d0-119">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="461d0-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="461d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="461d0-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="461d0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="461d0-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="461d0-122">-ServiceName</span></span>
<span data-ttu-id="461d0-123">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="461d0-123">Search Service name.</span></span>

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

### <span data-ttu-id="461d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461d0-124">CommonParameters</span></span>
<span data-ttu-id="461d0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461d0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="461d0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461d0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="461d0-127">INPUTS</span></span>

### <span data-ttu-id="461d0-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="461d0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="461d0-129">Parameter: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="461d0-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="461d0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="461d0-130">System.String</span></span>

## <span data-ttu-id="461d0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="461d0-131">OUTPUTS</span></span>

### <span data-ttu-id="461d0-132">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="461d0-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="461d0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="461d0-133">NOTES</span></span>

## <span data-ttu-id="461d0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="461d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="461d0-135">Neu – AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="461d0-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
