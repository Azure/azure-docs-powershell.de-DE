---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827359"
---
# <span data-ttu-id="b9289-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b9289-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="b9289-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9289-102">SYNOPSIS</span></span>
<span data-ttu-id="b9289-103">Alle Kontingente auflisten.</span><span class="sxs-lookup"><span data-stu-id="b9289-103">List all quotas.</span></span>

## <span data-ttu-id="b9289-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9289-104">SYNTAX</span></span>

### <span data-ttu-id="b9289-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9289-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9289-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b9289-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9289-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9289-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b9289-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9289-108">DESCRIPTION</span></span>
<span data-ttu-id="b9289-109">Alle Kontingente auflisten.</span><span class="sxs-lookup"><span data-stu-id="b9289-109">List all quotas.</span></span>
<span data-ttu-id="b9289-110">Begrenzen Sie die Liste, indem Sie einen Namen oder Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b9289-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="b9289-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9289-111">EXAMPLES</span></span>

### <span data-ttu-id="b9289-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9289-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="b9289-113">Listet alle Netzwerk Kontingente auf.</span><span class="sxs-lookup"><span data-stu-id="b9289-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="b9289-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9289-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b9289-115">Ruft das angegebene Netzwerk Kontingent ab.</span><span class="sxs-lookup"><span data-stu-id="b9289-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="b9289-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9289-116">PARAMETERS</span></span>

### <span data-ttu-id="b9289-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="b9289-117">-Filter</span></span>
<span data-ttu-id="b9289-118">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="b9289-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9289-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="b9289-119">-Location</span></span>
<span data-ttu-id="b9289-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9289-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9289-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b9289-121">-Name</span></span>
<span data-ttu-id="b9289-122">Netzwerk Kontingent Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b9289-122">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9289-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9289-123">-ResourceId</span></span>
<span data-ttu-id="b9289-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b9289-124">The resource id.</span></span>

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

### <span data-ttu-id="b9289-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9289-125">CommonParameters</span></span>
<span data-ttu-id="b9289-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9289-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9289-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9289-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9289-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9289-128">INPUTS</span></span>

## <span data-ttu-id="b9289-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9289-129">OUTPUTS</span></span>

### <span data-ttu-id="b9289-130">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="b9289-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="b9289-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9289-131">NOTES</span></span>

## <span data-ttu-id="b9289-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9289-132">RELATED LINKS</span></span>

