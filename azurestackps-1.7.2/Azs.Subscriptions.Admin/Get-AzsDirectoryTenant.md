---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827175"
---
# <span data-ttu-id="7039c-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="7039c-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="7039c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7039c-102">SYNOPSIS</span></span>
<span data-ttu-id="7039c-103">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="7039c-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7039c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7039c-104">SYNTAX</span></span>

### <span data-ttu-id="7039c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7039c-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7039c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7039c-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7039c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7039c-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7039c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7039c-108">DESCRIPTION</span></span>
<span data-ttu-id="7039c-109">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="7039c-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7039c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7039c-110">EXAMPLES</span></span>

### <span data-ttu-id="7039c-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7039c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="7039c-112">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="7039c-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7039c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7039c-113">PARAMETERS</span></span>

### <span data-ttu-id="7039c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7039c-114">-Name</span></span>
<span data-ttu-id="7039c-115">Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="7039c-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="7039c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7039c-116">-ResourceGroupName</span></span>
<span data-ttu-id="7039c-117">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7039c-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7039c-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7039c-118">-ResourceId</span></span>
<span data-ttu-id="7039c-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7039c-119">The resource id.</span></span>

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

### <span data-ttu-id="7039c-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="7039c-120">-Skip</span></span>
<span data-ttu-id="7039c-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="7039c-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7039c-122">-Top</span><span class="sxs-lookup"><span data-stu-id="7039c-122">-Top</span></span>
<span data-ttu-id="7039c-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="7039c-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7039c-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7039c-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7039c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7039c-125">CommonParameters</span></span>
<span data-ttu-id="7039c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7039c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7039c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7039c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7039c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7039c-128">INPUTS</span></span>

## <span data-ttu-id="7039c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7039c-129">OUTPUTS</span></span>

### <span data-ttu-id="7039c-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="7039c-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="7039c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7039c-131">NOTES</span></span>

## <span data-ttu-id="7039c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7039c-132">RELATED LINKS</span></span>

