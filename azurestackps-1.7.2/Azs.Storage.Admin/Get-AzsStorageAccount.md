---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827160"
---
# <span data-ttu-id="5e333-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e333-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="5e333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e333-102">SYNOPSIS</span></span>
<span data-ttu-id="5e333-103">Gibt das angeforderte Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="5e333-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="5e333-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e333-104">SYNTAX</span></span>

### <span data-ttu-id="5e333-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e333-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5e333-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5e333-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e333-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e333-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e333-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e333-108">DESCRIPTION</span></span>
<span data-ttu-id="5e333-109">Gibt das angeforderte Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="5e333-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="5e333-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e333-110">EXAMPLES</span></span>

### <span data-ttu-id="5e333-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e333-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="5e333-112">Abrufen einer Liste von Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="5e333-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="5e333-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e333-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="5e333-114">Abrufen von Details des angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e333-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="5e333-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e333-115">PARAMETERS</span></span>

### <span data-ttu-id="5e333-116">-Farmname</span><span class="sxs-lookup"><span data-stu-id="5e333-116">-FarmName</span></span>
<span data-ttu-id="5e333-117">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="5e333-117">Farm Id.</span></span>

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

### <span data-ttu-id="5e333-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5e333-118">-Name</span></span>
<span data-ttu-id="5e333-119">Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="5e333-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="5e333-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e333-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e333-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e333-121">Resource group name.</span></span>

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

### <span data-ttu-id="5e333-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e333-122">-ResourceId</span></span>
<span data-ttu-id="5e333-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e333-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e333-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="5e333-124">-Skip</span></span>
<span data-ttu-id="5e333-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e333-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5e333-126">– Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5e333-126">-Summary</span></span>
<span data-ttu-id="5e333-127">Switch für ob Zusammenfassungs-oder Detailinformationen werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e333-127">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e333-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5e333-128">-Top</span></span>
<span data-ttu-id="5e333-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="5e333-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5e333-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5e333-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5e333-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e333-131">CommonParameters</span></span>
<span data-ttu-id="5e333-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e333-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e333-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e333-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e333-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e333-134">INPUTS</span></span>

## <span data-ttu-id="5e333-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e333-135">OUTPUTS</span></span>

### <span data-ttu-id="5e333-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e333-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="5e333-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e333-137">NOTES</span></span>

## <span data-ttu-id="5e333-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e333-138">RELATED LINKS</span></span>

