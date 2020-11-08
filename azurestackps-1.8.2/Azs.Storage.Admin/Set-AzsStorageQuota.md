---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007220"
---
# <span data-ttu-id="e25cc-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e25cc-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="e25cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e25cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e25cc-103">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="e25cc-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e25cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e25cc-104">SYNTAX</span></span>

### <span data-ttu-id="e25cc-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="e25cc-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25cc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e25cc-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25cc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e25cc-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25cc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e25cc-108">DESCRIPTION</span></span>
<span data-ttu-id="e25cc-109">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="e25cc-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e25cc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e25cc-110">EXAMPLES</span></span>

### <span data-ttu-id="e25cc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e25cc-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="e25cc-112">Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="e25cc-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="e25cc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e25cc-113">PARAMETERS</span></span>

### <span data-ttu-id="e25cc-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e25cc-114">-Name</span></span>
<span data-ttu-id="e25cc-115">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="e25cc-115">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e25cc-116">-CapacityInGb</span></span>
<span data-ttu-id="e25cc-117">Maximal-Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="e25cc-117">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e25cc-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e25cc-119">Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="e25cc-119">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="e25cc-120">-Location</span></span>
<span data-ttu-id="e25cc-121">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="e25cc-121">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e25cc-122">-ResourceId</span></span>
<span data-ttu-id="e25cc-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e25cc-123">The resource id.</span></span>

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

### <span data-ttu-id="e25cc-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e25cc-124">-InputObject</span></span>
<span data-ttu-id="e25cc-125">Von Get-AzsStorageQuota zurückgegebenes Posbbily-Speicherkontingent</span><span class="sxs-lookup"><span data-stu-id="e25cc-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25cc-126">-WhatIf</span></span>
<span data-ttu-id="e25cc-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e25cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25cc-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e25cc-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e25cc-129">-Confirm</span></span>
<span data-ttu-id="e25cc-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e25cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25cc-131">CommonParameters</span></span>
<span data-ttu-id="e25cc-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25cc-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25cc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25cc-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e25cc-134">INPUTS</span></span>

## <span data-ttu-id="e25cc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e25cc-135">OUTPUTS</span></span>

### <span data-ttu-id="e25cc-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e25cc-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e25cc-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e25cc-137">NOTES</span></span>

## <span data-ttu-id="e25cc-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e25cc-138">RELATED LINKS</span></span>
