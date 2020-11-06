---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478594"
---
# <span data-ttu-id="76bd2-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76bd2-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="76bd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="76bd2-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="76bd2-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76bd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76bd2-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76bd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="76bd2-106">Das Cmdlet **Remove-AzureRmAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="76bd2-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="76bd2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="76bd2-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="76bd2-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="76bd2-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="76bd2-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="76bd2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="76bd2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="76bd2-111">-Force</span></span>
<span data-ttu-id="76bd2-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="76bd2-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76bd2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="76bd2-113">-Name</span></span>
<span data-ttu-id="76bd2-114">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="76bd2-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76bd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="76bd2-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="76bd2-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bd2-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76bd2-117">-Confirm</span></span>
<span data-ttu-id="76bd2-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76bd2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76bd2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76bd2-119">-WhatIf</span></span>
<span data-ttu-id="76bd2-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76bd2-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="76bd2-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76bd2-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76bd2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bd2-122">CommonParameters</span></span>
<span data-ttu-id="76bd2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76bd2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bd2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76bd2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bd2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76bd2-125">INPUTS</span></span>

### <span data-ttu-id="76bd2-126">Keine</span><span class="sxs-lookup"><span data-stu-id="76bd2-126">None</span></span>
<span data-ttu-id="76bd2-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="76bd2-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76bd2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76bd2-128">OUTPUTS</span></span>

## <span data-ttu-id="76bd2-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="76bd2-129">NOTES</span></span>

## <span data-ttu-id="76bd2-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76bd2-130">RELATED LINKS</span></span>

[<span data-ttu-id="76bd2-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76bd2-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="76bd2-132">Neu – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76bd2-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


