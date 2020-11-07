---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93506086"
---
# <span data-ttu-id="195e4-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="195e4-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="195e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="195e4-102">SYNOPSIS</span></span>
<span data-ttu-id="195e4-103">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="195e4-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="195e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="195e4-104">SYNTAX</span></span>

### <span data-ttu-id="195e4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="195e4-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="195e4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="195e4-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="195e4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="195e4-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="195e4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="195e4-108">DESCRIPTION</span></span>
<span data-ttu-id="195e4-109">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="195e4-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="195e4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="195e4-110">EXAMPLES</span></span>

### <span data-ttu-id="195e4-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="195e4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="195e4-112">Abrufen einer Liste der heruntergeladenen Azure Bridge-Produkte</span><span class="sxs-lookup"><span data-stu-id="195e4-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="195e4-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="195e4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="195e4-114">Abrufen eines heruntergeladenen Azure Bridge-Produkts nach Name</span><span class="sxs-lookup"><span data-stu-id="195e4-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="195e4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="195e4-115">PARAMETERS</span></span>

### <span data-ttu-id="195e4-116">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="195e4-116">-ActivationName</span></span>
<span data-ttu-id="195e4-117">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="195e4-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="195e4-118">-Name</span></span>
<span data-ttu-id="195e4-119">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="195e4-119">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="195e4-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="195e4-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="195e4-122">-ResourceId</span></span>
<span data-ttu-id="195e4-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="195e4-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="195e4-124">-Skip</span></span>
<span data-ttu-id="195e4-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="195e4-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-126">-Top</span><span class="sxs-lookup"><span data-stu-id="195e4-126">-Top</span></span>
<span data-ttu-id="195e4-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="195e4-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="195e4-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="195e4-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195e4-129">CommonParameters</span></span>
<span data-ttu-id="195e4-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195e4-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195e4-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="195e4-132">INPUTS</span></span>

## <span data-ttu-id="195e4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="195e4-133">OUTPUTS</span></span>

### <span data-ttu-id="195e4-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="195e4-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="195e4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="195e4-135">NOTES</span></span>

## <span data-ttu-id="195e4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="195e4-136">RELATED LINKS</span></span>

