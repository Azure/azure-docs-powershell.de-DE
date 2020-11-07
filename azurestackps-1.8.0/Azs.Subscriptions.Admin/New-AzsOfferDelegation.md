---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827835"
---
# <span data-ttu-id="be4e2-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="be4e2-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="be4e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="be4e2-103">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="be4e2-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="be4e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be4e2-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be4e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="be4e2-106">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="be4e2-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="be4e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="be4e2-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="be4e2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="be4e2-109">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="be4e2-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="be4e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be4e2-110">PARAMETERS</span></span>

### <span data-ttu-id="be4e2-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="be4e2-111">-Location</span></span>
<span data-ttu-id="be4e2-112">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="be4e2-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4e2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="be4e2-113">-Name</span></span>
<span data-ttu-id="be4e2-114">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="be4e2-114">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4e2-115">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="be4e2-115">-OfferName</span></span>
<span data-ttu-id="be4e2-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="be4e2-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="be4e2-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="be4e2-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4e2-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="be4e2-119">-SubscriptionId</span></span>
<span data-ttu-id="be4e2-120">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="be4e2-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4e2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be4e2-121">-Confirm</span></span>
<span data-ttu-id="be4e2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be4e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be4e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be4e2-123">-WhatIf</span></span>
<span data-ttu-id="be4e2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be4e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be4e2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be4e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be4e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4e2-126">CommonParameters</span></span>
<span data-ttu-id="be4e2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be4e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4e2-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be4e2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4e2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be4e2-129">INPUTS</span></span>

## <span data-ttu-id="be4e2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be4e2-130">OUTPUTS</span></span>

### <span data-ttu-id="be4e2-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="be4e2-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="be4e2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="be4e2-132">NOTES</span></span>

## <span data-ttu-id="be4e2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be4e2-133">RELATED LINKS</span></span>

