---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
ms.openlocfilehash: 563b8acadcf84359af740f504f3b25555a2e45f1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850168"
---
# <span data-ttu-id="6722a-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6722a-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="6722a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6722a-102">SYNOPSIS</span></span>
<span data-ttu-id="6722a-103">Wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="6722a-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6722a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6722a-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6722a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6722a-105">DESCRIPTION</span></span>
<span data-ttu-id="6722a-106">Das **ConvertTo-AzureRmVMManagedDisk-** Cmdlet wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="6722a-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="6722a-107">Die Zuweisung des virtuellen Computers muss beendet werden, bevor dieser Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6722a-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="6722a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6722a-108">EXAMPLES</span></span>

### <span data-ttu-id="6722a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6722a-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="6722a-110">Dieser Befehl wandelt die BLOB-basierten Datenträger des virtuellen Computers mit dem Namen "VM01" in der Ressourcengruppe "ResourceGroup01" auf verwaltete Datenträger um.</span><span class="sxs-lookup"><span data-stu-id="6722a-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="6722a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6722a-111">PARAMETERS</span></span>

### <span data-ttu-id="6722a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6722a-112">-AsJob</span></span>
<span data-ttu-id="6722a-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6722a-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6722a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6722a-114">-DefaultProfile</span></span>
<span data-ttu-id="6722a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6722a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6722a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6722a-116">-ResourceGroupName</span></span>
<span data-ttu-id="6722a-117">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6722a-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6722a-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="6722a-118">-VMName</span></span>
<span data-ttu-id="6722a-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="6722a-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="6722a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6722a-120">-Confirm</span></span>
<span data-ttu-id="6722a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6722a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6722a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6722a-122">-WhatIf</span></span>
<span data-ttu-id="6722a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6722a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6722a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6722a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6722a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6722a-125">CommonParameters</span></span>
<span data-ttu-id="6722a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6722a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6722a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6722a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6722a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6722a-128">INPUTS</span></span>

### <span data-ttu-id="6722a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6722a-129">System.String</span></span>

## <span data-ttu-id="6722a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6722a-130">OUTPUTS</span></span>

### <span data-ttu-id="6722a-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="6722a-131">System.Object</span></span>

## <span data-ttu-id="6722a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6722a-132">NOTES</span></span>

## <span data-ttu-id="6722a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6722a-133">RELATED LINKS</span></span>

