---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650331"
---
# <span data-ttu-id="605d8-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="605d8-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="605d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="605d8-102">SYNOPSIS</span></span>
<span data-ttu-id="605d8-103">Rufen Sie die Liste der Update Läufe ab.</span><span class="sxs-lookup"><span data-stu-id="605d8-103">Get the list of update runs.</span></span>

## <span data-ttu-id="605d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="605d8-104">SYNTAX</span></span>

### <span data-ttu-id="605d8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="605d8-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="605d8-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="605d8-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="605d8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="605d8-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="605d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605d8-108">DESCRIPTION</span></span>
<span data-ttu-id="605d8-109">Rufen Sie die Liste der Update Läufe ab.</span><span class="sxs-lookup"><span data-stu-id="605d8-109">Get the list of update runs.</span></span> <span data-ttu-id="605d8-110">Instanzen der zurückgegebenen UpdateRun-Objekte können ggf. an Restart-AzsUpdateRun umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="605d8-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="605d8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="605d8-111">EXAMPLES</span></span>

### <span data-ttu-id="605d8-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="605d8-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="605d8-113">Abrufen einer Liste aller Versuche, ein bestimmtes Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="605d8-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="605d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="605d8-114">PARAMETERS</span></span>

### <span data-ttu-id="605d8-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="605d8-115">-Location</span></span>
<span data-ttu-id="605d8-116">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="605d8-116">The name of the update location.</span></span>

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

### <span data-ttu-id="605d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="605d8-117">-Name</span></span>
<span data-ttu-id="605d8-118">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="605d8-118">Update run identifier.</span></span>

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

### <span data-ttu-id="605d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="605d8-120">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="605d8-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="605d8-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="605d8-121">-ResourceId</span></span>
<span data-ttu-id="605d8-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="605d8-122">The resource id.</span></span>

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

### <span data-ttu-id="605d8-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="605d8-123">-Skip</span></span>
<span data-ttu-id="605d8-124">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="605d8-124">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="605d8-125">-Top</span><span class="sxs-lookup"><span data-stu-id="605d8-125">-Top</span></span>
<span data-ttu-id="605d8-126">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="605d8-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="605d8-127">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="605d8-127">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="605d8-128">-Updatename</span><span class="sxs-lookup"><span data-stu-id="605d8-128">-UpdateName</span></span>
<span data-ttu-id="605d8-129">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="605d8-129">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605d8-130">CommonParameters</span></span>
<span data-ttu-id="605d8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605d8-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605d8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="605d8-133">INPUTS</span></span>

## <span data-ttu-id="605d8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="605d8-134">OUTPUTS</span></span>

### <span data-ttu-id="605d8-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="605d8-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="605d8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="605d8-136">NOTES</span></span>

## <span data-ttu-id="605d8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="605d8-137">RELATED LINKS</span></span>

