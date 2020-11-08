---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007146"
---
# <span data-ttu-id="8bf9c-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="8bf9c-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="8bf9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bf9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf9c-103">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-103">Get the list of available updates.</span></span>

## <span data-ttu-id="8bf9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bf9c-104">SYNTAX</span></span>

### <span data-ttu-id="8bf9c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bf9c-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bf9c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8bf9c-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bf9c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bf9c-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8bf9c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bf9c-108">DESCRIPTION</span></span>
<span data-ttu-id="8bf9c-109">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-109">Get the list of available updates.</span></span> <span data-ttu-id="8bf9c-110">Updates, die von diesem Modul zurückgegeben werden, werden möglicherweise an "Install-AzsUpdate" umgeleitet (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="8bf9c-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="8bf9c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bf9c-111">EXAMPLES</span></span>

### <span data-ttu-id="8bf9c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bf9c-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="8bf9c-113">Rufen Sie die Liste der verfügbaren Updates ab.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-113">Get the list of available updates.</span></span>

### <span data-ttu-id="8bf9c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8bf9c-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="8bf9c-115">Abrufen des spezifischen Updates</span><span class="sxs-lookup"><span data-stu-id="8bf9c-115">Get the specific update.</span></span>

## <span data-ttu-id="8bf9c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bf9c-116">PARAMETERS</span></span>

### <span data-ttu-id="8bf9c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8bf9c-117">-Name</span></span>
<span data-ttu-id="8bf9c-118">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-118">Name of the update.</span></span>

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

### <span data-ttu-id="8bf9c-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="8bf9c-119">-Location</span></span>
<span data-ttu-id="8bf9c-120">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-120">The name of the update location.</span></span>

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

### <span data-ttu-id="8bf9c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf9c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8bf9c-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8bf9c-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8bf9c-123">-ResourceId</span></span>
<span data-ttu-id="8bf9c-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-124">The resource id.</span></span>

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

### <span data-ttu-id="8bf9c-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="8bf9c-125">-Skip</span></span>
<span data-ttu-id="8bf9c-126">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8bf9c-127">-Top</span><span class="sxs-lookup"><span data-stu-id="8bf9c-127">-Top</span></span>
<span data-ttu-id="8bf9c-128">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8bf9c-129">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8bf9c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf9c-130">CommonParameters</span></span>
<span data-ttu-id="8bf9c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf9c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf9c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf9c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf9c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bf9c-133">INPUTS</span></span>

## <span data-ttu-id="8bf9c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bf9c-134">OUTPUTS</span></span>

### <span data-ttu-id="8bf9c-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="8bf9c-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="8bf9c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bf9c-136">NOTES</span></span>

## <span data-ttu-id="8bf9c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bf9c-137">RELATED LINKS</span></span>
