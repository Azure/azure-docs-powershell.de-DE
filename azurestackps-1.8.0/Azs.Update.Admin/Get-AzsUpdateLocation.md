---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827779"
---
# <span data-ttu-id="0afe3-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="0afe3-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="0afe3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0afe3-102">SYNOPSIS</span></span>
<span data-ttu-id="0afe3-103">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="0afe3-103">Get the list of update locations.</span></span>

## <span data-ttu-id="0afe3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0afe3-104">SYNTAX</span></span>

### <span data-ttu-id="0afe3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0afe3-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0afe3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0afe3-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0afe3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0afe3-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0afe3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0afe3-108">DESCRIPTION</span></span>
<span data-ttu-id="0afe3-109">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="0afe3-109">Get the list of update locations.</span></span> <span data-ttu-id="0afe3-110">Die zurückgegebenen Speicherorte können verwendet werden, um verfügbare Updates an einem bestimmten Speicherort mithilfe von Get-AzsUpdate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0afe3-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="0afe3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0afe3-111">EXAMPLES</span></span>

### <span data-ttu-id="0afe3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0afe3-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="0afe3-113">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="0afe3-113">Get the list of update locations.</span></span>

## <span data-ttu-id="0afe3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0afe3-114">PARAMETERS</span></span>

### <span data-ttu-id="0afe3-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="0afe3-115">-Location</span></span>
<span data-ttu-id="0afe3-116">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="0afe3-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afe3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0afe3-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0afe3-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0afe3-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0afe3-119">-ResourceId</span></span>
<span data-ttu-id="0afe3-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0afe3-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afe3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afe3-121">CommonParameters</span></span>
<span data-ttu-id="0afe3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afe3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afe3-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afe3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afe3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0afe3-124">INPUTS</span></span>

## <span data-ttu-id="0afe3-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0afe3-125">OUTPUTS</span></span>

### <span data-ttu-id="0afe3-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation angegeben ist</span><span class="sxs-lookup"><span data-stu-id="0afe3-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="0afe3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0afe3-127">NOTES</span></span>

## <span data-ttu-id="0afe3-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0afe3-128">RELATED LINKS</span></span>
