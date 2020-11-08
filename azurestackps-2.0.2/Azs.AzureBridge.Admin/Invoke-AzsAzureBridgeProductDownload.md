---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94007538"
---
# <span data-ttu-id="8ee0c-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="8ee0c-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="8ee0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ee0c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee0c-103">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="8ee0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ee0c-104">SYNTAX</span></span>

### <span data-ttu-id="8ee0c-105">Products_Download (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ee0c-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee0c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee0c-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ee0c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ee0c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ee0c-108">Lädt ein Produkt aus Azure Marketplace herunter.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="8ee0c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ee0c-109">EXAMPLES</span></span>

### <span data-ttu-id="8ee0c-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ee0c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="8ee0c-111">Herunterladen eines Produkts von Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="8ee0c-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="8ee0c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ee0c-112">PARAMETERS</span></span>

### <span data-ttu-id="8ee0c-113">-Aktivierungsname</span><span class="sxs-lookup"><span data-stu-id="8ee0c-113">-ActivationName</span></span>
<span data-ttu-id="8ee0c-114">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee0c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ee0c-115">-AsJob</span></span>
<span data-ttu-id="8ee0c-116">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8ee0c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ee0c-117">-Force</span></span>
<span data-ttu-id="8ee0c-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8ee0c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8ee0c-119">-Name</span></span>
<span data-ttu-id="8ee0c-120">Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee0c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee0c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ee0c-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee0c-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8ee0c-123">-ResourceId</span></span>
<span data-ttu-id="8ee0c-124">Ressourcenbezeichner für Azure Bridge-Produkt.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="8ee0c-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ee0c-125">-Confirm</span></span>
<span data-ttu-id="8ee0c-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee0c-127">-WhatIf</span></span>
<span data-ttu-id="8ee0c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee0c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee0c-130">CommonParameters</span></span>
<span data-ttu-id="8ee0c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee0c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee0c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ee0c-133">INPUTS</span></span>

## <span data-ttu-id="8ee0c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ee0c-134">OUTPUTS</span></span>

## <span data-ttu-id="8ee0c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ee0c-135">NOTES</span></span>

## <span data-ttu-id="8ee0c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ee0c-136">RELATED LINKS</span></span>

