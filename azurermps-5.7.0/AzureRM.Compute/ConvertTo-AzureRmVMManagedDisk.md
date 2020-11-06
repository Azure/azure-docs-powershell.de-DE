---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503861"
---
# <span data-ttu-id="096f4-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="096f4-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="096f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="096f4-102">SYNOPSIS</span></span>
<span data-ttu-id="096f4-103">Wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="096f4-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="096f4-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="096f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="096f4-105">DESCRIPTION</span></span>
<span data-ttu-id="096f4-106">Das **ConvertTo-AzureRmVMManagedDisk-** Cmdlet wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="096f4-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="096f4-107">Die Zuweisung des virtuellen Computers muss beendet werden, bevor dieser Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="096f4-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="096f4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="096f4-108">EXAMPLES</span></span>

### <span data-ttu-id="096f4-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="096f4-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="096f4-110">Dieser Befehl wandelt die BLOB-basierten Datenträger des virtuellen Computers mit dem Namen "VM01" in der Ressourcengruppe "ResourceGroup01" auf verwaltete Datenträger um.</span><span class="sxs-lookup"><span data-stu-id="096f4-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="096f4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="096f4-111">PARAMETERS</span></span>

### <span data-ttu-id="096f4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096f4-112">-ResourceGroupName</span></span>
<span data-ttu-id="096f4-113">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="096f4-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096f4-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="096f4-114">-VMName</span></span>
<span data-ttu-id="096f4-115">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="096f4-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096f4-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="096f4-116">-Confirm</span></span>
<span data-ttu-id="096f4-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="096f4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096f4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096f4-118">-WhatIf</span></span>
<span data-ttu-id="096f4-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="096f4-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="096f4-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="096f4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096f4-121">CommonParameters</span></span>
<span data-ttu-id="096f4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096f4-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096f4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="096f4-124">INPUTS</span></span>

### <span data-ttu-id="096f4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="096f4-125">System.String</span></span>

## <span data-ttu-id="096f4-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="096f4-126">OUTPUTS</span></span>

### <span data-ttu-id="096f4-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="096f4-127">System.Object</span></span>

## <span data-ttu-id="096f4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="096f4-128">NOTES</span></span>

## <span data-ttu-id="096f4-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="096f4-129">RELATED LINKS</span></span>

