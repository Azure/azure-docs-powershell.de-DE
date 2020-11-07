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
ms.locfileid: "93826640"
---
# <span data-ttu-id="8e4f6-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8e4f6-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="8e4f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4f6-103">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8e4f6-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="8e4f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4f6-104">SYNTAX</span></span>

### <span data-ttu-id="8e4f6-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e4f6-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4f6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4f6-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4f6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e4f6-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4f6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e4f6-108">DESCRIPTION</span></span>
<span data-ttu-id="8e4f6-109">Erstellen oder Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8e4f6-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="8e4f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e4f6-110">EXAMPLES</span></span>

### <span data-ttu-id="8e4f6-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e4f6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="8e4f6-112">Aktualisieren eines vorhandenen Speicherkontingents</span><span class="sxs-lookup"><span data-stu-id="8e4f6-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="8e4f6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4f6-113">PARAMETERS</span></span>

### <span data-ttu-id="8e4f6-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="8e4f6-114">-CapacityInGb</span></span>
<span data-ttu-id="8e4f6-115">Maximal-Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="8e4f6-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="8e4f6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e4f6-116">-InputObject</span></span>
<span data-ttu-id="8e4f6-117">Von Get-AzsStorageQuota zurückgegebenes Posbbily-Speicherkontingent</span><span class="sxs-lookup"><span data-stu-id="8e4f6-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="8e4f6-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="8e4f6-118">-Location</span></span>
<span data-ttu-id="8e4f6-119">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-119">Resource location.</span></span>

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

### <span data-ttu-id="8e4f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8e4f6-120">-Name</span></span>
<span data-ttu-id="8e4f6-121">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="8e4f6-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8e4f6-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="8e4f6-123">Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="8e4f6-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8e4f6-124">-ResourceId</span></span>
<span data-ttu-id="8e4f6-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-125">The resource id.</span></span>

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

### <span data-ttu-id="8e4f6-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e4f6-126">-Confirm</span></span>
<span data-ttu-id="8e4f6-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4f6-128">-WhatIf</span></span>
<span data-ttu-id="8e4f6-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4f6-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4f6-131">CommonParameters</span></span>
<span data-ttu-id="8e4f6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4f6-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e4f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4f6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e4f6-134">INPUTS</span></span>

## <span data-ttu-id="8e4f6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e4f6-135">OUTPUTS</span></span>

### <span data-ttu-id="8e4f6-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="8e4f6-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="8e4f6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e4f6-137">NOTES</span></span>

## <span data-ttu-id="8e4f6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e4f6-138">RELATED LINKS</span></span>

