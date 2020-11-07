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
ms.locfileid: "93661948"
---
# <span data-ttu-id="5e7d7-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="5e7d7-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="5e7d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7d7-103">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="5e7d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e7d7-104">SYNTAX</span></span>

### <span data-ttu-id="5e7d7-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e7d7-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5e7d7-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5e7d7-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e7d7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7d7-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5e7d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e7d7-108">DESCRIPTION</span></span>
<span data-ttu-id="5e7d7-109">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="5e7d7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e7d7-110">EXAMPLES</span></span>

### <span data-ttu-id="5e7d7-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e7d7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="5e7d7-112">Abrufen aller Speichersubsysteme von einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="5e7d7-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="5e7d7-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e7d7-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="5e7d7-114">Rufen Sie ein Speichersubsystem ab, das einen Speicherort und einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="5e7d7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e7d7-115">PARAMETERS</span></span>

### <span data-ttu-id="5e7d7-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="5e7d7-116">-Filter</span></span>
<span data-ttu-id="5e7d7-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="5e7d7-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5e7d7-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="5e7d7-118">-Location</span></span>
<span data-ttu-id="5e7d7-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5e7d7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e7d7-120">-Name</span></span>
<span data-ttu-id="5e7d7-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5e7d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e7d7-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5e7d7-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e7d7-124">-ResourceId</span></span>
<span data-ttu-id="5e7d7-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-125">The resource id.</span></span>

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

### <span data-ttu-id="5e7d7-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5e7d7-126">-Skip</span></span>
<span data-ttu-id="5e7d7-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5e7d7-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5e7d7-128">-Top</span></span>
<span data-ttu-id="5e7d7-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5e7d7-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5e7d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7d7-131">CommonParameters</span></span>
<span data-ttu-id="5e7d7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7d7-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7d7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7d7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e7d7-134">INPUTS</span></span>

## <span data-ttu-id="5e7d7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e7d7-135">OUTPUTS</span></span>

### <span data-ttu-id="5e7d7-136">Microsoft. AzureStack. Management. Fabric. admin. Models. Speichersystem</span><span class="sxs-lookup"><span data-stu-id="5e7d7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="5e7d7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e7d7-137">NOTES</span></span>

## <span data-ttu-id="5e7d7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e7d7-138">RELATED LINKS</span></span>

