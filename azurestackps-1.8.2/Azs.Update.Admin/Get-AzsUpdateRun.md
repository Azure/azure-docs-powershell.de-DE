---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007140"
---
# <span data-ttu-id="16056-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="16056-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="16056-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16056-102">SYNOPSIS</span></span>
<span data-ttu-id="16056-103">Rufen Sie die Liste der Update Läufe ab.</span><span class="sxs-lookup"><span data-stu-id="16056-103">Get the list of update runs.</span></span>

## <span data-ttu-id="16056-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16056-104">SYNTAX</span></span>

### <span data-ttu-id="16056-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="16056-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="16056-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="16056-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="16056-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="16056-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="16056-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16056-108">DESCRIPTION</span></span>
<span data-ttu-id="16056-109">Rufen Sie die Liste der Update Läufe ab.</span><span class="sxs-lookup"><span data-stu-id="16056-109">Get the list of update runs.</span></span> <span data-ttu-id="16056-110">Instanzen der zurückgegebenen UpdateRun-Objekte können ggf. an Restart-AzsUpdateRun umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="16056-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="16056-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16056-111">EXAMPLES</span></span>

### <span data-ttu-id="16056-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16056-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="16056-113">Abrufen einer Liste aller Versuche, ein bestimmtes Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="16056-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="16056-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="16056-114">PARAMETERS</span></span>

### <span data-ttu-id="16056-115">-Name</span><span class="sxs-lookup"><span data-stu-id="16056-115">-Name</span></span>
<span data-ttu-id="16056-116">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="16056-116">Update run identifier.</span></span>

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

### <span data-ttu-id="16056-117">-Updatename</span><span class="sxs-lookup"><span data-stu-id="16056-117">-UpdateName</span></span>
<span data-ttu-id="16056-118">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="16056-118">Name of the update.</span></span>

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

### <span data-ttu-id="16056-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="16056-119">-Location</span></span>
<span data-ttu-id="16056-120">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="16056-120">The name of the update location.</span></span>

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

### <span data-ttu-id="16056-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16056-121">-ResourceGroupName</span></span>
<span data-ttu-id="16056-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="16056-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="16056-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16056-123">-ResourceId</span></span>
<span data-ttu-id="16056-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16056-124">The resource id.</span></span>

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

### <span data-ttu-id="16056-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="16056-125">-Skip</span></span>
<span data-ttu-id="16056-126">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="16056-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="16056-127">-Top</span><span class="sxs-lookup"><span data-stu-id="16056-127">-Top</span></span>
<span data-ttu-id="16056-128">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="16056-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="16056-129">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="16056-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="16056-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16056-130">CommonParameters</span></span>
<span data-ttu-id="16056-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16056-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16056-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16056-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16056-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16056-133">INPUTS</span></span>

## <span data-ttu-id="16056-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16056-134">OUTPUTS</span></span>

### <span data-ttu-id="16056-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="16056-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="16056-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="16056-136">NOTES</span></span>

## <span data-ttu-id="16056-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16056-137">RELATED LINKS</span></span>
