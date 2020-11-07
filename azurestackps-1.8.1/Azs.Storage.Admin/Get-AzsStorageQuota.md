---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840599"
---
# <span data-ttu-id="e5a90-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e5a90-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="e5a90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5a90-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a90-103">Gibt eine Liste der Speicherkontingente an der angegebenen Position zurück.</span><span class="sxs-lookup"><span data-stu-id="e5a90-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="e5a90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a90-104">SYNTAX</span></span>

### <span data-ttu-id="e5a90-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5a90-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e5a90-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e5a90-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="e5a90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5a90-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e5a90-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5a90-108">DESCRIPTION</span></span>
<span data-ttu-id="e5a90-109">Gibt eine Liste der Speicherkontingente an der angegebenen Position zurück.</span><span class="sxs-lookup"><span data-stu-id="e5a90-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="e5a90-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5a90-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a90-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5a90-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="e5a90-112">Rufen Sie die Liste der Speicherkontingente ab.</span><span class="sxs-lookup"><span data-stu-id="e5a90-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="e5a90-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5a90-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="e5a90-114">Abrufen von Details des angegebenen Speicherkontingents anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="e5a90-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="e5a90-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a90-115">PARAMETERS</span></span>

### <span data-ttu-id="e5a90-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a90-116">-Name</span></span>
<span data-ttu-id="e5a90-117">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="e5a90-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="e5a90-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e5a90-118">-Location</span></span>
<span data-ttu-id="e5a90-119">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="e5a90-119">Resource location.</span></span>

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

### <span data-ttu-id="e5a90-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e5a90-120">-ResourceId</span></span>
<span data-ttu-id="e5a90-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e5a90-121">The resource id.</span></span>

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

### <span data-ttu-id="e5a90-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="e5a90-122">-Skip</span></span>
<span data-ttu-id="e5a90-123">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5a90-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e5a90-124">-Top</span><span class="sxs-lookup"><span data-stu-id="e5a90-124">-Top</span></span>
<span data-ttu-id="e5a90-125">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="e5a90-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e5a90-126">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e5a90-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e5a90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a90-127">CommonParameters</span></span>
<span data-ttu-id="e5a90-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a90-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a90-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a90-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5a90-130">INPUTS</span></span>

## <span data-ttu-id="e5a90-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5a90-131">OUTPUTS</span></span>

### <span data-ttu-id="e5a90-132">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e5a90-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e5a90-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5a90-133">NOTES</span></span>

## <span data-ttu-id="e5a90-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5a90-134">RELATED LINKS</span></span>
