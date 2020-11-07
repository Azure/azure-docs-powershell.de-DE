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
ms.locfileid: "93827363"
---
# <span data-ttu-id="9a873-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="9a873-101">Get-AzsPlan</span></span>

## <span data-ttu-id="9a873-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a873-102">SYNOPSIS</span></span>
<span data-ttu-id="9a873-103">Alle Pläne in allen Abonnements auflisten.</span><span class="sxs-lookup"><span data-stu-id="9a873-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="9a873-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a873-104">SYNTAX</span></span>

### <span data-ttu-id="9a873-105">Bauteile (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a873-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9a873-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9a873-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="9a873-107">Liste</span><span class="sxs-lookup"><span data-stu-id="9a873-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9a873-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a873-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9a873-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a873-109">DESCRIPTION</span></span>
<span data-ttu-id="9a873-110">Alle Pläne in allen Abonnements auflisten.</span><span class="sxs-lookup"><span data-stu-id="9a873-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="9a873-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a873-111">EXAMPLES</span></span>

### <span data-ttu-id="9a873-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a873-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="9a873-113">Rufen Sie einen spezifische-Plan unter diesen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="9a873-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="9a873-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a873-114">PARAMETERS</span></span>

### <span data-ttu-id="9a873-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9a873-115">-Name</span></span>
<span data-ttu-id="9a873-116">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="9a873-116">Name of the plan.</span></span>

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

### <span data-ttu-id="9a873-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a873-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a873-118">Der Name der Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="9a873-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9a873-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a873-119">-ResourceId</span></span>
<span data-ttu-id="9a873-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9a873-120">The resource id.</span></span>

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

### <span data-ttu-id="9a873-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="9a873-121">-Skip</span></span>
<span data-ttu-id="9a873-122">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="9a873-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9a873-123">-Top</span><span class="sxs-lookup"><span data-stu-id="9a873-123">-Top</span></span>
<span data-ttu-id="9a873-124">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="9a873-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9a873-125">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9a873-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9a873-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a873-126">CommonParameters</span></span>
<span data-ttu-id="9a873-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a873-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a873-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a873-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a873-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a873-129">INPUTS</span></span>

## <span data-ttu-id="9a873-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a873-130">OUTPUTS</span></span>

### <span data-ttu-id="9a873-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="9a873-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="9a873-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a873-132">NOTES</span></span>

## <span data-ttu-id="9a873-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a873-133">RELATED LINKS</span></span>

