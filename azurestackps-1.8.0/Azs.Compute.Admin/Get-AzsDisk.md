---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827676"
---
# <span data-ttu-id="791b8-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="791b8-101">Get-AzsDisk</span></span>

## <span data-ttu-id="791b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="791b8-102">SYNOPSIS</span></span>
<span data-ttu-id="791b8-103">Gibt die Liste der verwalteten Datenträger zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="791b8-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="791b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="791b8-104">SYNTAX</span></span>

### <span data-ttu-id="791b8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="791b8-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="791b8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="791b8-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="791b8-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="791b8-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="791b8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="791b8-108">DESCRIPTION</span></span>
<span data-ttu-id="791b8-109">Gibt eine Liste von Datenträgern zurück.</span><span class="sxs-lookup"><span data-stu-id="791b8-109">Returns a list of disks.</span></span>

## <span data-ttu-id="791b8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="791b8-110">EXAMPLES</span></span>

### <span data-ttu-id="791b8-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="791b8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="791b8-112">Gibt eine Liste der verwalteten Datenträger am lokalen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="791b8-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="791b8-113">Standardmäßig werden die ersten 100-Datenträger</span><span class="sxs-lookup"><span data-stu-id="791b8-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="791b8-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="791b8-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="791b8-115">Besorgen Sie sich einen bestimmten verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="791b8-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="791b8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="791b8-116">PARAMETERS</span></span>

### <span data-ttu-id="791b8-117">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="791b8-117">-Count</span></span>
<span data-ttu-id="791b8-118">Die maximale Anzahl von Datenträgern, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="791b8-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="791b8-119">-Location</span></span>
<span data-ttu-id="791b8-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="791b8-120">Location of the resource.</span></span>

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

### <span data-ttu-id="791b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="791b8-121">-Name</span></span>
<span data-ttu-id="791b8-122">Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="791b8-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="791b8-123">-ResourceId</span></span>
<span data-ttu-id="791b8-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="791b8-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="791b8-125">-SharePath</span></span>
<span data-ttu-id="791b8-126">Die Quell Freigabe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="791b8-126">The source share which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-127">-Start</span><span class="sxs-lookup"><span data-stu-id="791b8-127">-Start</span></span>
<span data-ttu-id="791b8-128">Der startIndex von Datenträgern in Query.</span><span class="sxs-lookup"><span data-stu-id="791b8-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-129">-Status</span><span class="sxs-lookup"><span data-stu-id="791b8-129">-Status</span></span>
<span data-ttu-id="791b8-130">Die Parameter des Datenträger Zustands.</span><span class="sxs-lookup"><span data-stu-id="791b8-130">The parameters of disk state.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="791b8-131">-UserSubscriptionId</span></span>
<span data-ttu-id="791b8-132">Die Mandanten-Abonnement-ID, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="791b8-132">Tenant Subscription Id which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791b8-133">CommonParameters</span></span>
<span data-ttu-id="791b8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791b8-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791b8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791b8-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="791b8-136">INPUTS</span></span>

## <span data-ttu-id="791b8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="791b8-137">OUTPUTS</span></span>

### <span data-ttu-id="791b8-138">Microsoft. AzureStack. Management. Compute. admin. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="791b8-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="791b8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="791b8-139">NOTES</span></span>

## <span data-ttu-id="791b8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="791b8-140">RELATED LINKS</span></span>

