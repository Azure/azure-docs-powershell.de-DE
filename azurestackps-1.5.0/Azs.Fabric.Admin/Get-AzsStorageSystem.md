---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474785"
---
# <span data-ttu-id="06340-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="06340-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="06340-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06340-102">SYNOPSIS</span></span>
<span data-ttu-id="06340-103">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="06340-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="06340-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06340-104">SYNTAX</span></span>

### <span data-ttu-id="06340-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="06340-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="06340-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="06340-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="06340-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="06340-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="06340-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06340-108">DESCRIPTION</span></span>
<span data-ttu-id="06340-109">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="06340-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="06340-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06340-110">EXAMPLES</span></span>

### <span data-ttu-id="06340-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="06340-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="06340-112">Abrufen aller Speichersubsysteme von einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="06340-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="06340-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="06340-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="06340-114">Rufen Sie ein Speichersubsystem ab, das einen Speicherort und einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="06340-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="06340-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="06340-115">PARAMETERS</span></span>

### <span data-ttu-id="06340-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="06340-116">-Filter</span></span>
<span data-ttu-id="06340-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="06340-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="06340-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="06340-118">-Location</span></span>
<span data-ttu-id="06340-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="06340-119">Location of the resource.</span></span>

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

### <span data-ttu-id="06340-120">-Name</span><span class="sxs-lookup"><span data-stu-id="06340-120">-Name</span></span>
<span data-ttu-id="06340-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="06340-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="06340-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06340-122">-ResourceGroupName</span></span>
<span data-ttu-id="06340-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="06340-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="06340-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="06340-124">-ResourceId</span></span>
<span data-ttu-id="06340-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="06340-125">The resource id.</span></span>

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

### <span data-ttu-id="06340-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="06340-126">-Skip</span></span>
<span data-ttu-id="06340-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="06340-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06340-128">-Top</span><span class="sxs-lookup"><span data-stu-id="06340-128">-Top</span></span>
<span data-ttu-id="06340-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="06340-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="06340-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="06340-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06340-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06340-131">CommonParameters</span></span>
<span data-ttu-id="06340-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06340-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06340-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06340-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06340-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06340-134">INPUTS</span></span>

## <span data-ttu-id="06340-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06340-135">OUTPUTS</span></span>

### <span data-ttu-id="06340-136">Microsoft. AzureStack. Management. Fabric. admin. Models. Speichersystem</span><span class="sxs-lookup"><span data-stu-id="06340-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="06340-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="06340-137">NOTES</span></span>

## <span data-ttu-id="06340-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06340-138">RELATED LINKS</span></span>

