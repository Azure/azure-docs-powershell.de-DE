---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93851131"
---
# <span data-ttu-id="fd096-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="fd096-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="fd096-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd096-102">SYNOPSIS</span></span>
<span data-ttu-id="fd096-103">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="fd096-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="fd096-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd096-104">SYNTAX</span></span>

### <span data-ttu-id="fd096-105">Products_Download (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd096-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd096-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd096-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd096-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd096-107">DESCRIPTION</span></span>
<span data-ttu-id="fd096-108">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="fd096-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="fd096-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd096-109">EXAMPLES</span></span>

### <span data-ttu-id="fd096-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd096-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="fd096-111">Herunterladen eines Produkts von Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="fd096-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="fd096-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd096-112">PARAMETERS</span></span>

### <span data-ttu-id="fd096-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fd096-113">-Name</span></span>
<span data-ttu-id="fd096-114">Name des Produkts</span><span class="sxs-lookup"><span data-stu-id="fd096-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd096-115">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="fd096-115">-ActivationName</span></span>
<span data-ttu-id="fd096-116">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="fd096-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd096-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd096-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd096-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="fd096-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd096-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fd096-119">-ResourceId</span></span>
<span data-ttu-id="fd096-120">Ressourcenbezeichner für Azure Bridge-Produkt.</span><span class="sxs-lookup"><span data-stu-id="fd096-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="fd096-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd096-121">-AsJob</span></span>
<span data-ttu-id="fd096-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="fd096-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="fd096-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fd096-123">-Force</span></span>
<span data-ttu-id="fd096-124">Parameter wechseln, um keine Bestätigung zu fordern</span><span class="sxs-lookup"><span data-stu-id="fd096-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="fd096-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd096-125">-WhatIf</span></span>
<span data-ttu-id="fd096-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd096-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd096-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd096-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd096-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd096-128">-Confirm</span></span>
<span data-ttu-id="fd096-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd096-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd096-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd096-130">CommonParameters</span></span>
<span data-ttu-id="fd096-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd096-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd096-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd096-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd096-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd096-133">INPUTS</span></span>

## <span data-ttu-id="fd096-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd096-134">OUTPUTS</span></span>

## <span data-ttu-id="fd096-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd096-135">NOTES</span></span>

## <span data-ttu-id="fd096-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd096-136">RELATED LINKS</span></span>
