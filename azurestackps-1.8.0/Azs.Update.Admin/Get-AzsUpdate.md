---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827447"
---
# <span data-ttu-id="7b37f-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="7b37f-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="7b37f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b37f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b37f-103">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="7b37f-103">Get the list of available updates.</span></span>

## <span data-ttu-id="7b37f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b37f-104">SYNTAX</span></span>

### <span data-ttu-id="7b37f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b37f-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b37f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7b37f-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7b37f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b37f-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7b37f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b37f-108">DESCRIPTION</span></span>
<span data-ttu-id="7b37f-109">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="7b37f-109">Get the list of available updates.</span></span> <span data-ttu-id="7b37f-110">Updates, die von diesem Modul zurückgegeben werden, werden möglicherweise an "Install-AzsUpdate" umgeleitet (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="7b37f-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="7b37f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b37f-111">EXAMPLES</span></span>

### <span data-ttu-id="7b37f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b37f-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="7b37f-113">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="7b37f-113">Get the list of available updates.</span></span>

### <span data-ttu-id="7b37f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7b37f-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="7b37f-115">Abrufen des spezifischen Updates</span><span class="sxs-lookup"><span data-stu-id="7b37f-115">Get the specific update.</span></span>

## <span data-ttu-id="7b37f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b37f-116">PARAMETERS</span></span>

### <span data-ttu-id="7b37f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b37f-117">-Name</span></span>
<span data-ttu-id="7b37f-118">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="7b37f-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b37f-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="7b37f-119">-Location</span></span>
<span data-ttu-id="7b37f-120">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="7b37f-120">The name of the update location.</span></span>

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

### <span data-ttu-id="7b37f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b37f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b37f-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7b37f-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7b37f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7b37f-123">-ResourceId</span></span>
<span data-ttu-id="7b37f-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7b37f-124">The resource id.</span></span>

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

### <span data-ttu-id="7b37f-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="7b37f-125">-Skip</span></span>
<span data-ttu-id="7b37f-126">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="7b37f-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7b37f-127">-Top</span><span class="sxs-lookup"><span data-stu-id="7b37f-127">-Top</span></span>
<span data-ttu-id="7b37f-128">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="7b37f-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7b37f-129">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b37f-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7b37f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b37f-130">CommonParameters</span></span>
<span data-ttu-id="7b37f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b37f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b37f-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b37f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b37f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b37f-133">INPUTS</span></span>

## <span data-ttu-id="7b37f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b37f-134">OUTPUTS</span></span>

### <span data-ttu-id="7b37f-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="7b37f-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="7b37f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b37f-136">NOTES</span></span>

## <span data-ttu-id="7b37f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b37f-137">RELATED LINKS</span></span>
