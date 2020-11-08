---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94007545"
---
# <span data-ttu-id="46244-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="46244-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="46244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46244-102">SYNOPSIS</span></span>
<span data-ttu-id="46244-103">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="46244-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="46244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46244-104">SYNTAX</span></span>

### <span data-ttu-id="46244-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="46244-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46244-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="46244-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="46244-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46244-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="46244-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46244-108">DESCRIPTION</span></span>
<span data-ttu-id="46244-109">Gibt eine Liste der Produkte zurück, die von Azure Marketplace heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="46244-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="46244-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46244-110">EXAMPLES</span></span>

### <span data-ttu-id="46244-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46244-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="46244-112">Rufen Sie eine Liste der Produkte ab, die von Azure Marketplace heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="46244-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="46244-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="46244-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="46244-114">Abrufen von Produktinformationen, die über den Namen von Azure Marketplace heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="46244-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="46244-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="46244-115">PARAMETERS</span></span>

### <span data-ttu-id="46244-116">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="46244-116">-ActivationName</span></span>
<span data-ttu-id="46244-117">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="46244-117">Name of the activation.</span></span>

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

### <span data-ttu-id="46244-118">-Name</span><span class="sxs-lookup"><span data-stu-id="46244-118">-Name</span></span>
<span data-ttu-id="46244-119">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="46244-119">Name of the product.</span></span>

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

### <span data-ttu-id="46244-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46244-120">-ResourceGroupName</span></span>
<span data-ttu-id="46244-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="46244-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="46244-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="46244-122">-ResourceId</span></span>
<span data-ttu-id="46244-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="46244-123">The resource id.</span></span>

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

### <span data-ttu-id="46244-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="46244-124">-Skip</span></span>
<span data-ttu-id="46244-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="46244-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="46244-126">-Top</span><span class="sxs-lookup"><span data-stu-id="46244-126">-Top</span></span>
<span data-ttu-id="46244-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="46244-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="46244-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="46244-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="46244-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46244-129">CommonParameters</span></span>
<span data-ttu-id="46244-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46244-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46244-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46244-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46244-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46244-132">INPUTS</span></span>

## <span data-ttu-id="46244-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46244-133">OUTPUTS</span></span>

### <span data-ttu-id="46244-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="46244-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="46244-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="46244-135">NOTES</span></span>

## <span data-ttu-id="46244-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46244-136">RELATED LINKS</span></span>

