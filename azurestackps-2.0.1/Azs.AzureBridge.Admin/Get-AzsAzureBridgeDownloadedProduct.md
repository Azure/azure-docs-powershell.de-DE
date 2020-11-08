---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b7cc2211df4fd8b9d65c3e93483a485a10ae32
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94007546"
---
# <span data-ttu-id="958cf-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="958cf-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="958cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="958cf-102">SYNOPSIS</span></span>
<span data-ttu-id="958cf-103">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="958cf-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="958cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="958cf-104">SYNTAX</span></span>

### <span data-ttu-id="958cf-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="958cf-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="958cf-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="958cf-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="958cf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="958cf-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="958cf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="958cf-108">DESCRIPTION</span></span>
<span data-ttu-id="958cf-109">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="958cf-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="958cf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="958cf-110">EXAMPLES</span></span>

### <span data-ttu-id="958cf-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="958cf-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="958cf-112">Abrufen einer Liste der heruntergeladenen Azure Bridge-Produkte</span><span class="sxs-lookup"><span data-stu-id="958cf-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="958cf-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="958cf-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="958cf-114">Abrufen eines heruntergeladenen Azure Bridge-Produkts nach Name</span><span class="sxs-lookup"><span data-stu-id="958cf-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="958cf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="958cf-115">PARAMETERS</span></span>

### <span data-ttu-id="958cf-116">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="958cf-116">-ActivationName</span></span>
<span data-ttu-id="958cf-117">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="958cf-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958cf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="958cf-118">-Name</span></span>
<span data-ttu-id="958cf-119">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="958cf-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="958cf-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="958cf-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958cf-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="958cf-122">-ResourceId</span></span>
<span data-ttu-id="958cf-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="958cf-123">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958cf-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="958cf-124">-Skip</span></span>
<span data-ttu-id="958cf-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="958cf-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="958cf-126">-Top</span><span class="sxs-lookup"><span data-stu-id="958cf-126">-Top</span></span>
<span data-ttu-id="958cf-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="958cf-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="958cf-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="958cf-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="958cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958cf-129">CommonParameters</span></span>
<span data-ttu-id="958cf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958cf-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958cf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958cf-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="958cf-132">INPUTS</span></span>

## <span data-ttu-id="958cf-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="958cf-133">OUTPUTS</span></span>

### <span data-ttu-id="958cf-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="958cf-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="958cf-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="958cf-135">NOTES</span></span>

## <span data-ttu-id="958cf-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="958cf-136">RELATED LINKS</span></span>

