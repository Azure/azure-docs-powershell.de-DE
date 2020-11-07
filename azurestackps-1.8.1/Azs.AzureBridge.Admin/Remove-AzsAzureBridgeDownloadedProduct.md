---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93851063"
---
# <span data-ttu-id="b81f7-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="b81f7-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="b81f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b81f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b81f7-103">Löschen Sie ein Produkt, das von Azure Marketplace heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b81f7-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b81f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b81f7-104">SYNTAX</span></span>

### <span data-ttu-id="b81f7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b81f7-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b81f7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b81f7-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b81f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b81f7-107">DESCRIPTION</span></span>
<span data-ttu-id="b81f7-108">Löschen Sie ein Produkt, das von Azure Marketplace heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b81f7-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b81f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b81f7-109">EXAMPLES</span></span>

### <span data-ttu-id="b81f7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b81f7-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b81f7-111">Löschen eines Produkts, das von Azure Marketplace heruntergeladen wurde</span><span class="sxs-lookup"><span data-stu-id="b81f7-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="b81f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b81f7-112">PARAMETERS</span></span>

### <span data-ttu-id="b81f7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b81f7-113">-Name</span></span>
<span data-ttu-id="b81f7-114">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="b81f7-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-115">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="b81f7-115">-ActivationName</span></span>
<span data-ttu-id="b81f7-116">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="b81f7-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b81f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b81f7-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="b81f7-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b81f7-119">-Force</span></span>
<span data-ttu-id="b81f7-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b81f7-120">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b81f7-121">-ResourceId</span></span>
<span data-ttu-id="b81f7-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b81f7-122">The resource id.</span></span>

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

### <span data-ttu-id="b81f7-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b81f7-123">-AsJob</span></span>
<span data-ttu-id="b81f7-124">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b81f7-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b81f7-125">-WhatIf</span></span>
<span data-ttu-id="b81f7-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b81f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b81f7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b81f7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b81f7-128">-Confirm</span></span>
<span data-ttu-id="b81f7-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b81f7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81f7-130">CommonParameters</span></span>
<span data-ttu-id="b81f7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b81f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81f7-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81f7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81f7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b81f7-133">INPUTS</span></span>

## <span data-ttu-id="b81f7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b81f7-134">OUTPUTS</span></span>

### <span data-ttu-id="b81f7-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="b81f7-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="b81f7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b81f7-136">NOTES</span></span>

## <span data-ttu-id="b81f7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b81f7-137">RELATED LINKS</span></span>
