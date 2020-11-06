---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475458"
---
# <span data-ttu-id="8b980-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8b980-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="8b980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b980-102">SYNOPSIS</span></span>
<span data-ttu-id="8b980-103">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8b980-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="8b980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b980-104">SYNTAX</span></span>

### <span data-ttu-id="8b980-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b980-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b980-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b980-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b980-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8b980-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b980-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b980-108">DESCRIPTION</span></span>
<span data-ttu-id="8b980-109">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8b980-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="8b980-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b980-110">EXAMPLES</span></span>

### <span data-ttu-id="8b980-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b980-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="8b980-112">Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8b980-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="8b980-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b980-113">PARAMETERS</span></span>

### <span data-ttu-id="8b980-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="8b980-114">-CapacityInGb</span></span>
<span data-ttu-id="8b980-115">Maximal-Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="8b980-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="8b980-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b980-116">-InputObject</span></span>
<span data-ttu-id="8b980-117">Von Get-AzsStorageQuota zurückgegebenes Posbbily-Speicherkontingent</span><span class="sxs-lookup"><span data-stu-id="8b980-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="8b980-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="8b980-118">-Location</span></span>
<span data-ttu-id="8b980-119">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="8b980-119">Resource location.</span></span>

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

### <span data-ttu-id="8b980-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8b980-120">-Name</span></span>
<span data-ttu-id="8b980-121">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="8b980-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="8b980-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8b980-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="8b980-123">Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="8b980-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="8b980-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b980-124">-ResourceId</span></span>
<span data-ttu-id="8b980-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8b980-125">The resource id.</span></span>

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

### <span data-ttu-id="8b980-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b980-126">-Confirm</span></span>
<span data-ttu-id="8b980-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b980-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b980-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b980-128">-WhatIf</span></span>
<span data-ttu-id="8b980-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b980-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b980-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b980-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b980-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b980-131">CommonParameters</span></span>
<span data-ttu-id="8b980-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b980-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b980-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b980-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b980-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b980-134">INPUTS</span></span>

## <span data-ttu-id="8b980-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b980-135">OUTPUTS</span></span>

### <span data-ttu-id="8b980-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="8b980-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="8b980-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b980-137">NOTES</span></span>

## <span data-ttu-id="8b980-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b980-138">RELATED LINKS</span></span>

