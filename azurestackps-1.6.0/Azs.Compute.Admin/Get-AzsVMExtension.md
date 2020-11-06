---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474638"
---
# <span data-ttu-id="b24f6-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b24f6-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="b24f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b24f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b24f6-103">Gibt die aktuell verfügbaren Virtual Machine-Bild Erweiterungen zurück.</span><span class="sxs-lookup"><span data-stu-id="b24f6-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="b24f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b24f6-104">SYNTAX</span></span>

### <span data-ttu-id="b24f6-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b24f6-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b24f6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b24f6-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b24f6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24f6-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b24f6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b24f6-108">DESCRIPTION</span></span>
<span data-ttu-id="b24f6-109">Gibt Bild Erweiterungen für virtuelle Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="b24f6-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="b24f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b24f6-110">EXAMPLES</span></span>

### <span data-ttu-id="b24f6-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b24f6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="b24f6-112">Rufen Sie alle VM-Erweiterungen an einem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="b24f6-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="b24f6-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b24f6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="b24f6-114">Spezifische VM-Erweiterung abrufen.</span><span class="sxs-lookup"><span data-stu-id="b24f6-114">Get specific VM extension.</span></span>

## <span data-ttu-id="b24f6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b24f6-115">PARAMETERS</span></span>

### <span data-ttu-id="b24f6-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="b24f6-116">-Location</span></span>
<span data-ttu-id="b24f6-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b24f6-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b24f6-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b24f6-118">-Publisher</span></span>
<span data-ttu-id="b24f6-119">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="b24f6-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="b24f6-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b24f6-120">-ResourceId</span></span>
<span data-ttu-id="b24f6-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b24f6-121">The resource id.</span></span>

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

### <span data-ttu-id="b24f6-122">-Typ</span><span class="sxs-lookup"><span data-stu-id="b24f6-122">-Type</span></span>
<span data-ttu-id="b24f6-123">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b24f6-123">Type of extension.</span></span>

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

### <span data-ttu-id="b24f6-124">-Version</span><span class="sxs-lookup"><span data-stu-id="b24f6-124">-Version</span></span>
<span data-ttu-id="b24f6-125">Die Version der Bild Erweiterung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b24f6-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="b24f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24f6-126">CommonParameters</span></span>
<span data-ttu-id="b24f6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24f6-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24f6-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b24f6-129">INPUTS</span></span>

## <span data-ttu-id="b24f6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b24f6-130">OUTPUTS</span></span>

### <span data-ttu-id="b24f6-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="b24f6-131">VmExtensionObject</span></span>

## <span data-ttu-id="b24f6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b24f6-132">NOTES</span></span>

## <span data-ttu-id="b24f6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b24f6-133">RELATED LINKS</span></span>

