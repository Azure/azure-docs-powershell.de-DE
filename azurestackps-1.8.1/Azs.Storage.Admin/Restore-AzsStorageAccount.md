---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840832"
---
# <span data-ttu-id="48172-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48172-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="48172-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48172-102">SYNOPSIS</span></span>
<span data-ttu-id="48172-103">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="48172-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="48172-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48172-104">SYNTAX</span></span>

### <span data-ttu-id="48172-105">Undelete (Standard)</span><span class="sxs-lookup"><span data-stu-id="48172-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48172-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="48172-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48172-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48172-107">DESCRIPTION</span></span>
<span data-ttu-id="48172-108">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="48172-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="48172-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48172-109">EXAMPLES</span></span>

### <span data-ttu-id="48172-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48172-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="48172-111">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="48172-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="48172-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="48172-112">PARAMETERS</span></span>

### <span data-ttu-id="48172-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="48172-113">-FarmName</span></span>
<span data-ttu-id="48172-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="48172-114">Farm Id.</span></span>

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

### <span data-ttu-id="48172-115">-Name</span><span class="sxs-lookup"><span data-stu-id="48172-115">-Name</span></span>
<span data-ttu-id="48172-116">Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="48172-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="48172-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48172-117">-ResourceGroupName</span></span>
<span data-ttu-id="48172-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48172-118">Resource group name.</span></span>

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

### <span data-ttu-id="48172-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="48172-119">-ResourceId</span></span>
<span data-ttu-id="48172-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="48172-120">The resource id.</span></span>

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

### <span data-ttu-id="48172-121">-Force</span><span class="sxs-lookup"><span data-stu-id="48172-121">-Force</span></span>
<span data-ttu-id="48172-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="48172-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48172-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48172-123">-WhatIf</span></span>
<span data-ttu-id="48172-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48172-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48172-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48172-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48172-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48172-126">-Confirm</span></span>
<span data-ttu-id="48172-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48172-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48172-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48172-128">CommonParameters</span></span>
<span data-ttu-id="48172-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48172-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48172-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48172-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48172-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48172-131">INPUTS</span></span>

## <span data-ttu-id="48172-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48172-132">OUTPUTS</span></span>

## <span data-ttu-id="48172-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="48172-133">NOTES</span></span>

## <span data-ttu-id="48172-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48172-134">RELATED LINKS</span></span>
