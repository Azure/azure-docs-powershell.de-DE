---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827884"
---
# <span data-ttu-id="f1734-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="f1734-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="f1734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1734-102">SYNOPSIS</span></span>
<span data-ttu-id="f1734-103">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="f1734-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="f1734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1734-104">SYNTAX</span></span>

### <span data-ttu-id="f1734-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1734-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f1734-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f1734-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1734-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1734-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f1734-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1734-108">DESCRIPTION</span></span>
<span data-ttu-id="f1734-109">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="f1734-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="f1734-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1734-110">EXAMPLES</span></span>

### <span data-ttu-id="f1734-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1734-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="f1734-112">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="f1734-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="f1734-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1734-113">PARAMETERS</span></span>

### <span data-ttu-id="f1734-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f1734-114">-Name</span></span>
<span data-ttu-id="f1734-115">Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="f1734-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="f1734-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1734-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1734-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="f1734-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="f1734-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1734-118">-ResourceId</span></span>
<span data-ttu-id="f1734-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f1734-119">The resource id.</span></span>

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

### <span data-ttu-id="f1734-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="f1734-120">-Skip</span></span>
<span data-ttu-id="f1734-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1734-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f1734-122">-Top</span><span class="sxs-lookup"><span data-stu-id="f1734-122">-Top</span></span>
<span data-ttu-id="f1734-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="f1734-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f1734-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1734-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f1734-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1734-125">CommonParameters</span></span>
<span data-ttu-id="f1734-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1734-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1734-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1734-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1734-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1734-128">INPUTS</span></span>

## <span data-ttu-id="f1734-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1734-129">OUTPUTS</span></span>

### <span data-ttu-id="f1734-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="f1734-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="f1734-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1734-131">NOTES</span></span>

## <span data-ttu-id="f1734-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1734-132">RELATED LINKS</span></span>

