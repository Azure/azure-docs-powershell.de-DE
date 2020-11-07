---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826643"
---
# <span data-ttu-id="54ae8-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54ae8-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="54ae8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="54ae8-103">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="54ae8-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="54ae8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ae8-104">SYNTAX</span></span>

### <span data-ttu-id="54ae8-105">Undelete (Standard)</span><span class="sxs-lookup"><span data-stu-id="54ae8-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ae8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54ae8-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ae8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54ae8-107">DESCRIPTION</span></span>
<span data-ttu-id="54ae8-108">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="54ae8-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="54ae8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54ae8-109">EXAMPLES</span></span>

### <span data-ttu-id="54ae8-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54ae8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="54ae8-111">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="54ae8-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="54ae8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="54ae8-112">PARAMETERS</span></span>

### <span data-ttu-id="54ae8-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="54ae8-113">-FarmName</span></span>
<span data-ttu-id="54ae8-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="54ae8-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ae8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54ae8-115">-Force</span></span>
<span data-ttu-id="54ae8-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="54ae8-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ae8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="54ae8-117">-Name</span></span>
<span data-ttu-id="54ae8-118">Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="54ae8-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ae8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ae8-119">-ResourceGroupName</span></span>
<span data-ttu-id="54ae8-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54ae8-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ae8-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="54ae8-121">-ResourceId</span></span>
<span data-ttu-id="54ae8-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="54ae8-122">The resource id.</span></span>

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

### <span data-ttu-id="54ae8-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54ae8-123">-Confirm</span></span>
<span data-ttu-id="54ae8-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54ae8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ae8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ae8-125">-WhatIf</span></span>
<span data-ttu-id="54ae8-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54ae8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ae8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54ae8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ae8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ae8-128">CommonParameters</span></span>
<span data-ttu-id="54ae8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ae8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ae8-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ae8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ae8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54ae8-131">INPUTS</span></span>

## <span data-ttu-id="54ae8-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54ae8-132">OUTPUTS</span></span>

## <span data-ttu-id="54ae8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="54ae8-133">NOTES</span></span>

## <span data-ttu-id="54ae8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54ae8-134">RELATED LINKS</span></span>

