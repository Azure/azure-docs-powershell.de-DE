---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474702"
---
# <span data-ttu-id="3a3cc-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="3a3cc-101">Get-AzsPlan</span></span>

## <span data-ttu-id="3a3cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3cc-103">Alle Pläne in allen Abonnements auflisten.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="3a3cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a3cc-104">SYNTAX</span></span>

### <span data-ttu-id="3a3cc-105">Bauteile (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a3cc-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3a3cc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3a3cc-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="3a3cc-107">Liste</span><span class="sxs-lookup"><span data-stu-id="3a3cc-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3a3cc-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a3cc-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3a3cc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a3cc-109">DESCRIPTION</span></span>
<span data-ttu-id="3a3cc-110">Alle Pläne in allen Abonnements auflisten.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="3a3cc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a3cc-111">EXAMPLES</span></span>

### <span data-ttu-id="3a3cc-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a3cc-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="3a3cc-113">Rufen Sie einen spezifische-Plan unter diesen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="3a3cc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a3cc-114">PARAMETERS</span></span>

### <span data-ttu-id="3a3cc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3a3cc-115">-Name</span></span>
<span data-ttu-id="3a3cc-116">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-116">Name of the plan.</span></span>

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

### <span data-ttu-id="3a3cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a3cc-118">Der Name der Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3cc-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a3cc-119">-ResourceId</span></span>
<span data-ttu-id="3a3cc-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-120">The resource id.</span></span>

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

### <span data-ttu-id="3a3cc-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="3a3cc-121">-Skip</span></span>
<span data-ttu-id="3a3cc-122">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3cc-123">-Top</span><span class="sxs-lookup"><span data-stu-id="3a3cc-123">-Top</span></span>
<span data-ttu-id="3a3cc-124">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3a3cc-125">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3cc-126">CommonParameters</span></span>
<span data-ttu-id="3a3cc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3cc-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3cc-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a3cc-129">INPUTS</span></span>

## <span data-ttu-id="3a3cc-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a3cc-130">OUTPUTS</span></span>

### <span data-ttu-id="3a3cc-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="3a3cc-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="3a3cc-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a3cc-132">NOTES</span></span>

## <span data-ttu-id="3a3cc-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a3cc-133">RELATED LINKS</span></span>

