---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840604"
---
# <span data-ttu-id="6a7e1-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="6a7e1-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="6a7e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7e1-103">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-103">Get the list of update locations.</span></span>

## <span data-ttu-id="6a7e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a7e1-104">SYNTAX</span></span>

### <span data-ttu-id="6a7e1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a7e1-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a7e1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6a7e1-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a7e1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7e1-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6a7e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a7e1-108">DESCRIPTION</span></span>
<span data-ttu-id="6a7e1-109">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-109">Get the list of update locations.</span></span> <span data-ttu-id="6a7e1-110">Die zurückgegebenen Speicherorte können verwendet werden, um verfügbare Updates an einem bestimmten Speicherort mithilfe von Get-AzsUpdate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="6a7e1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a7e1-111">EXAMPLES</span></span>

### <span data-ttu-id="6a7e1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a7e1-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="6a7e1-113">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-113">Get the list of update locations.</span></span>

## <span data-ttu-id="6a7e1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a7e1-114">PARAMETERS</span></span>

### <span data-ttu-id="6a7e1-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="6a7e1-115">-Location</span></span>
<span data-ttu-id="6a7e1-116">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-116">Name of the Location.</span></span>

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

### <span data-ttu-id="6a7e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a7e1-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6a7e1-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6a7e1-119">-ResourceId</span></span>
<span data-ttu-id="6a7e1-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-120">The resource id.</span></span>

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

### <span data-ttu-id="6a7e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7e1-121">CommonParameters</span></span>
<span data-ttu-id="6a7e1-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7e1-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7e1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7e1-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a7e1-124">INPUTS</span></span>

## <span data-ttu-id="6a7e1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a7e1-125">OUTPUTS</span></span>

### <span data-ttu-id="6a7e1-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation angegeben ist</span><span class="sxs-lookup"><span data-stu-id="6a7e1-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="6a7e1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a7e1-127">NOTES</span></span>

## <span data-ttu-id="6a7e1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a7e1-128">RELATED LINKS</span></span>
