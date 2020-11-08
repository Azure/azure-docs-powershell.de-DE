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
ms.locfileid: "94007537"
---
# <span data-ttu-id="180c9-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="180c9-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="180c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="180c9-102">SYNOPSIS</span></span>
<span data-ttu-id="180c9-103">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="180c9-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="180c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="180c9-104">SYNTAX</span></span>

### <span data-ttu-id="180c9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="180c9-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="180c9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="180c9-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="180c9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="180c9-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="180c9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="180c9-108">DESCRIPTION</span></span>
<span data-ttu-id="180c9-109">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="180c9-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="180c9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="180c9-110">EXAMPLES</span></span>

### <span data-ttu-id="180c9-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="180c9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="180c9-112">Abrufen einer Liste der heruntergeladenen Azure Bridge-Produkte</span><span class="sxs-lookup"><span data-stu-id="180c9-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="180c9-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="180c9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="180c9-114">Abrufen eines heruntergeladenen Azure Bridge-Produkts nach Name</span><span class="sxs-lookup"><span data-stu-id="180c9-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="180c9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="180c9-115">PARAMETERS</span></span>

### <span data-ttu-id="180c9-116">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="180c9-116">-ActivationName</span></span>
<span data-ttu-id="180c9-117">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="180c9-117">Name of the activation.</span></span>

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

### <span data-ttu-id="180c9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="180c9-118">-Name</span></span>
<span data-ttu-id="180c9-119">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="180c9-119">Name of the product.</span></span>

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

### <span data-ttu-id="180c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="180c9-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="180c9-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="180c9-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="180c9-122">-ResourceId</span></span>
<span data-ttu-id="180c9-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="180c9-123">The resource id.</span></span>

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

### <span data-ttu-id="180c9-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="180c9-124">-Skip</span></span>
<span data-ttu-id="180c9-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="180c9-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="180c9-126">-Top</span><span class="sxs-lookup"><span data-stu-id="180c9-126">-Top</span></span>
<span data-ttu-id="180c9-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="180c9-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="180c9-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="180c9-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="180c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180c9-129">CommonParameters</span></span>
<span data-ttu-id="180c9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180c9-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="180c9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180c9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="180c9-132">INPUTS</span></span>

## <span data-ttu-id="180c9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="180c9-133">OUTPUTS</span></span>

### <span data-ttu-id="180c9-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="180c9-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="180c9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="180c9-135">NOTES</span></span>

## <span data-ttu-id="180c9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="180c9-136">RELATED LINKS</span></span>

