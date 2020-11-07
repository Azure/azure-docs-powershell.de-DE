---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93665445"
---
# <span data-ttu-id="15b64-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="15b64-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="15b64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15b64-102">SYNOPSIS</span></span>
<span data-ttu-id="15b64-103">Löschen Sie ein Produkt, das von Azure Marketplace heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="15b64-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="15b64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b64-104">SYNTAX</span></span>

### <span data-ttu-id="15b64-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="15b64-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15b64-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="15b64-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15b64-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15b64-107">DESCRIPTION</span></span>
<span data-ttu-id="15b64-108">Löschen Sie ein Produkt, das von Azure Marketplace heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="15b64-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="15b64-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15b64-109">EXAMPLES</span></span>

### <span data-ttu-id="15b64-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="15b64-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="15b64-111">Löschen eines Produkts, das von Azure Marketplace heruntergeladen wurde</span><span class="sxs-lookup"><span data-stu-id="15b64-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="15b64-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="15b64-112">PARAMETERS</span></span>

### <span data-ttu-id="15b64-113">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="15b64-113">-ActivationName</span></span>
<span data-ttu-id="15b64-114">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="15b64-114">Name of the activation.</span></span>

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

### <span data-ttu-id="15b64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15b64-115">-AsJob</span></span>
<span data-ttu-id="15b64-116">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="15b64-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="15b64-117">-Force</span><span class="sxs-lookup"><span data-stu-id="15b64-117">-Force</span></span>
<span data-ttu-id="15b64-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="15b64-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="15b64-119">-Name</span><span class="sxs-lookup"><span data-stu-id="15b64-119">-Name</span></span>
<span data-ttu-id="15b64-120">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="15b64-120">Name of the product.</span></span>

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

### <span data-ttu-id="15b64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b64-121">-ResourceGroupName</span></span>
<span data-ttu-id="15b64-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="15b64-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="15b64-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15b64-123">-ResourceId</span></span>
<span data-ttu-id="15b64-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="15b64-124">The resource id.</span></span>

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

### <span data-ttu-id="15b64-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15b64-125">-Confirm</span></span>
<span data-ttu-id="15b64-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15b64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b64-127">-WhatIf</span></span>
<span data-ttu-id="15b64-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15b64-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b64-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15b64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b64-130">CommonParameters</span></span>
<span data-ttu-id="15b64-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b64-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b64-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b64-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15b64-133">INPUTS</span></span>

## <span data-ttu-id="15b64-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15b64-134">OUTPUTS</span></span>

### <span data-ttu-id="15b64-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="15b64-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="15b64-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="15b64-136">NOTES</span></span>

## <span data-ttu-id="15b64-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15b64-137">RELATED LINKS</span></span>

