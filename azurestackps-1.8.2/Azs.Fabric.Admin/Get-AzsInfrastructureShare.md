---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007167"
---
# <span data-ttu-id="d1ce8-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="d1ce8-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="d1ce8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ce8-103">Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="d1ce8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1ce8-104">SYNTAX</span></span>

### <span data-ttu-id="d1ce8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1ce8-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ce8-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d1ce8-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ce8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1ce8-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d1ce8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="d1ce8-109">Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="d1ce8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1ce8-110">EXAMPLES</span></span>

### <span data-ttu-id="d1ce8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1ce8-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="d1ce8-112">Gibt eine Liste aller Dateifreigaben zurück.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="d1ce8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d1ce8-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="d1ce8-114">Gibt eine Dateifreigabe basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="d1ce8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1ce8-115">PARAMETERS</span></span>

### <span data-ttu-id="d1ce8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d1ce8-116">-Name</span></span>
<span data-ttu-id="d1ce8-117">Name der Fabric-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="d1ce8-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="d1ce8-118">-Location</span></span>
<span data-ttu-id="d1ce8-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d1ce8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ce8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1ce8-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d1ce8-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1ce8-122">-ResourceId</span></span>
<span data-ttu-id="d1ce8-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-123">The resource id.</span></span>

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

### <span data-ttu-id="d1ce8-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="d1ce8-124">-Filter</span></span>
<span data-ttu-id="d1ce8-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="d1ce8-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="d1ce8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ce8-126">CommonParameters</span></span>
<span data-ttu-id="d1ce8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ce8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ce8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ce8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ce8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1ce8-129">INPUTS</span></span>

## <span data-ttu-id="d1ce8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1ce8-130">OUTPUTS</span></span>

### <span data-ttu-id="d1ce8-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="d1ce8-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="d1ce8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1ce8-132">NOTES</span></span>

## <span data-ttu-id="d1ce8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1ce8-133">RELATED LINKS</span></span>
