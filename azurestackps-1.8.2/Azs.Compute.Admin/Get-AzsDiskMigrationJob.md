---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007111"
---
# <span data-ttu-id="2b6be-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="2b6be-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="2b6be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b6be-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6be-103">Gibt die Liste der verwalteten Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="2b6be-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="2b6be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b6be-104">SYNTAX</span></span>

### <span data-ttu-id="2b6be-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b6be-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b6be-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b6be-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="2b6be-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2b6be-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="2b6be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b6be-108">DESCRIPTION</span></span>
<span data-ttu-id="2b6be-109">Gibt eine Liste der Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="2b6be-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="2b6be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b6be-110">EXAMPLES</span></span>

### <span data-ttu-id="2b6be-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b6be-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="2b6be-112">Abrufen eines bestimmten Migrationsauftrags für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="2b6be-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="2b6be-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b6be-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="2b6be-114">Gibt eine Liste der verwalteten Datenträger Migrationsaufträge am lokalen Standort zurück.</span><span class="sxs-lookup"><span data-stu-id="2b6be-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="2b6be-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b6be-115">PARAMETERS</span></span>

### <span data-ttu-id="2b6be-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="2b6be-116">-Location</span></span>
<span data-ttu-id="2b6be-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2b6be-117">Location of the resource.</span></span>

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

### <span data-ttu-id="2b6be-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2b6be-118">-Name</span></span>
<span data-ttu-id="2b6be-119">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="2b6be-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="2b6be-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2b6be-120">-ResourceId</span></span>
<span data-ttu-id="2b6be-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2b6be-121">The resource id.</span></span>

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

### <span data-ttu-id="2b6be-122">-Status</span><span class="sxs-lookup"><span data-stu-id="2b6be-122">-Status</span></span>
<span data-ttu-id="2b6be-123">Die Parameter des Status des Datenträger Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="2b6be-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="2b6be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6be-124">CommonParameters</span></span>
<span data-ttu-id="2b6be-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6be-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6be-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6be-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b6be-127">INPUTS</span></span>

## <span data-ttu-id="2b6be-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b6be-128">OUTPUTS</span></span>

### <span data-ttu-id="2b6be-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="2b6be-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="2b6be-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b6be-130">NOTES</span></span>

## <span data-ttu-id="2b6be-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b6be-131">RELATED LINKS</span></span>

