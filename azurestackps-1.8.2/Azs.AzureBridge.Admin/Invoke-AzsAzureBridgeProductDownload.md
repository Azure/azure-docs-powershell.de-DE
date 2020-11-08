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
ms.locfileid: "94175339"
---
# <span data-ttu-id="29c91-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="29c91-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="29c91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29c91-102">SYNOPSIS</span></span>
<span data-ttu-id="29c91-103">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="29c91-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="29c91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29c91-104">SYNTAX</span></span>

### <span data-ttu-id="29c91-105">Products_Download (Standard)</span><span class="sxs-lookup"><span data-stu-id="29c91-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c91-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29c91-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29c91-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29c91-107">DESCRIPTION</span></span>
<span data-ttu-id="29c91-108">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="29c91-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="29c91-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29c91-109">EXAMPLES</span></span>

### <span data-ttu-id="29c91-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29c91-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="29c91-111">Herunterladen eines Produkts von Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="29c91-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="29c91-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="29c91-112">PARAMETERS</span></span>

### <span data-ttu-id="29c91-113">-Name</span><span class="sxs-lookup"><span data-stu-id="29c91-113">-Name</span></span>
<span data-ttu-id="29c91-114">Name des Produkts</span><span class="sxs-lookup"><span data-stu-id="29c91-114">Name of the product</span></span>

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

### <span data-ttu-id="29c91-115">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="29c91-115">-ActivationName</span></span>
<span data-ttu-id="29c91-116">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="29c91-116">Name of the activation.</span></span>

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

### <span data-ttu-id="29c91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c91-117">-ResourceGroupName</span></span>
<span data-ttu-id="29c91-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="29c91-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="29c91-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29c91-119">-ResourceId</span></span>
<span data-ttu-id="29c91-120">Ressourcenbezeichner für Azure Bridge-Produkt.</span><span class="sxs-lookup"><span data-stu-id="29c91-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="29c91-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29c91-121">-AsJob</span></span>
<span data-ttu-id="29c91-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="29c91-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="29c91-123">-Force</span><span class="sxs-lookup"><span data-stu-id="29c91-123">-Force</span></span>
<span data-ttu-id="29c91-124">Parameter wechseln, um keine Bestätigung zu fordern</span><span class="sxs-lookup"><span data-stu-id="29c91-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="29c91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c91-125">-WhatIf</span></span>
<span data-ttu-id="29c91-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29c91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c91-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29c91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c91-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29c91-128">-Confirm</span></span>
<span data-ttu-id="29c91-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29c91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c91-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c91-130">CommonParameters</span></span>
<span data-ttu-id="29c91-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c91-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c91-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c91-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c91-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29c91-133">INPUTS</span></span>

## <span data-ttu-id="29c91-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29c91-134">OUTPUTS</span></span>

## <span data-ttu-id="29c91-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="29c91-135">NOTES</span></span>

## <span data-ttu-id="29c91-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29c91-136">RELATED LINKS</span></span>
