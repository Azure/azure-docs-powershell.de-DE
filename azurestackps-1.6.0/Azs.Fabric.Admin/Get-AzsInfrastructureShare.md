---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662010"
---
# <span data-ttu-id="1c247-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="1c247-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="1c247-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c247-102">SYNOPSIS</span></span>
<span data-ttu-id="1c247-103">Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="1c247-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="1c247-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c247-104">SYNTAX</span></span>

### <span data-ttu-id="1c247-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c247-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c247-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1c247-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c247-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c247-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1c247-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c247-108">DESCRIPTION</span></span>
<span data-ttu-id="1c247-109">Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="1c247-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="1c247-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c247-110">EXAMPLES</span></span>

### <span data-ttu-id="1c247-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c247-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="1c247-112">Gibt eine Liste aller Dateifreigaben zurück.</span><span class="sxs-lookup"><span data-stu-id="1c247-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="1c247-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c247-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="1c247-114">Gibt eine Dateifreigabe basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="1c247-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="1c247-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c247-115">PARAMETERS</span></span>

### <span data-ttu-id="1c247-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="1c247-116">-Filter</span></span>
<span data-ttu-id="1c247-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="1c247-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1c247-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="1c247-118">-Location</span></span>
<span data-ttu-id="1c247-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1c247-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1c247-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c247-120">-Name</span></span>
<span data-ttu-id="1c247-121">Name der Fabric-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="1c247-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="1c247-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c247-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c247-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c247-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1c247-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1c247-124">-ResourceId</span></span>
<span data-ttu-id="1c247-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1c247-125">The resource id.</span></span>

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

### <span data-ttu-id="1c247-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c247-126">CommonParameters</span></span>
<span data-ttu-id="1c247-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c247-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c247-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c247-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c247-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c247-129">INPUTS</span></span>

## <span data-ttu-id="1c247-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c247-130">OUTPUTS</span></span>

### <span data-ttu-id="1c247-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="1c247-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="1c247-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c247-132">NOTES</span></span>

## <span data-ttu-id="1c247-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c247-133">RELATED LINKS</span></span>

