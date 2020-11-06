---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474865"
---
# <span data-ttu-id="4438b-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4438b-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="4438b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4438b-102">SYNOPSIS</span></span>
<span data-ttu-id="4438b-103">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="4438b-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="4438b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4438b-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4438b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4438b-105">DESCRIPTION</span></span>
<span data-ttu-id="4438b-106">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="4438b-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="4438b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4438b-107">EXAMPLES</span></span>

### <span data-ttu-id="4438b-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4438b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="4438b-109">Erstellen Sie eine neue Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="4438b-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="4438b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4438b-110">PARAMETERS</span></span>

### <span data-ttu-id="4438b-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="4438b-111">-Location</span></span>
<span data-ttu-id="4438b-112">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4438b-112">Location of the resource.</span></span>

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

### <span data-ttu-id="4438b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4438b-113">-Name</span></span>
<span data-ttu-id="4438b-114">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="4438b-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="4438b-115">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="4438b-115">-OfferName</span></span>
<span data-ttu-id="4438b-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="4438b-116">Name of an offer.</span></span>

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

### <span data-ttu-id="4438b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4438b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4438b-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4438b-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4438b-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4438b-119">-SubscriptionId</span></span>
<span data-ttu-id="4438b-120">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="4438b-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="4438b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4438b-121">-Confirm</span></span>
<span data-ttu-id="4438b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4438b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4438b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4438b-123">-WhatIf</span></span>
<span data-ttu-id="4438b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4438b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4438b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4438b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4438b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4438b-126">CommonParameters</span></span>
<span data-ttu-id="4438b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4438b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4438b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4438b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4438b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4438b-129">INPUTS</span></span>

## <span data-ttu-id="4438b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4438b-130">OUTPUTS</span></span>

### <span data-ttu-id="4438b-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4438b-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="4438b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="4438b-132">NOTES</span></span>

## <span data-ttu-id="4438b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4438b-133">RELATED LINKS</span></span>

