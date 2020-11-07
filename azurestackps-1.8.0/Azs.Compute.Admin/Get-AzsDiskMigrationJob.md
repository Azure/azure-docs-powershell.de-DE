---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827668"
---
# <span data-ttu-id="9022f-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9022f-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="9022f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9022f-102">SYNOPSIS</span></span>
<span data-ttu-id="9022f-103">Gibt die Liste der verwalteten Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="9022f-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="9022f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9022f-104">SYNTAX</span></span>

### <span data-ttu-id="9022f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9022f-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="9022f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9022f-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="9022f-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9022f-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="9022f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9022f-108">DESCRIPTION</span></span>
<span data-ttu-id="9022f-109">Gibt eine Liste der Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="9022f-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="9022f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9022f-110">EXAMPLES</span></span>

### <span data-ttu-id="9022f-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9022f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="9022f-112">Abrufen eines bestimmten Migrationsauftrags für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="9022f-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="9022f-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9022f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="9022f-114">Gibt eine Liste der verwalteten Datenträger Migrationsaufträge am lokalen Standort zurück.</span><span class="sxs-lookup"><span data-stu-id="9022f-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="9022f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9022f-115">PARAMETERS</span></span>

### <span data-ttu-id="9022f-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="9022f-116">-Location</span></span>
<span data-ttu-id="9022f-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9022f-117">Location of the resource.</span></span>

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

### <span data-ttu-id="9022f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9022f-118">-Name</span></span>
<span data-ttu-id="9022f-119">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="9022f-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9022f-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9022f-120">-ResourceId</span></span>
<span data-ttu-id="9022f-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9022f-121">The resource id.</span></span>

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

### <span data-ttu-id="9022f-122">-Status</span><span class="sxs-lookup"><span data-stu-id="9022f-122">-Status</span></span>
<span data-ttu-id="9022f-123">Die Parameter des Status des Datenträger Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="9022f-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="9022f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9022f-124">CommonParameters</span></span>
<span data-ttu-id="9022f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9022f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9022f-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9022f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9022f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9022f-127">INPUTS</span></span>

## <span data-ttu-id="9022f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9022f-128">OUTPUTS</span></span>

### <span data-ttu-id="9022f-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9022f-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="9022f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9022f-130">NOTES</span></span>

## <span data-ttu-id="9022f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9022f-131">RELATED LINKS</span></span>

