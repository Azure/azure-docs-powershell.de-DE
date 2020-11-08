---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008657"
---
# <span data-ttu-id="813b9-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="813b9-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="813b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="813b9-102">SYNOPSIS</span></span>
<span data-ttu-id="813b9-103">Wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="813b9-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="813b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="813b9-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="813b9-105">DESCRIPTION</span></span>
<span data-ttu-id="813b9-106">Das **ConvertTo-AzVMManagedDisk-** Cmdlet wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="813b9-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="813b9-107">Die Zuweisung des virtuellen Computers muss beendet werden, bevor dieser Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="813b9-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="813b9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="813b9-108">EXAMPLES</span></span>

### <span data-ttu-id="813b9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="813b9-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="813b9-110">Dieser Befehl wandelt die BLOB-basierten Datenträger des virtuellen Computers mit dem Namen "VM01" in der Ressourcengruppe "ResourceGroup01" auf verwaltete Datenträger um.</span><span class="sxs-lookup"><span data-stu-id="813b9-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="813b9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="813b9-111">PARAMETERS</span></span>

### <span data-ttu-id="813b9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="813b9-112">-AsJob</span></span>
<span data-ttu-id="813b9-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="813b9-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813b9-114">-DefaultProfile</span></span>
<span data-ttu-id="813b9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="813b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813b9-116">-ResourceGroupName</span></span>
<span data-ttu-id="813b9-117">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="813b9-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="813b9-118">-VMName</span></span>
<span data-ttu-id="813b9-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="813b9-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="813b9-120">-Confirm</span></span>
<span data-ttu-id="813b9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="813b9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813b9-122">-WhatIf</span></span>
<span data-ttu-id="813b9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="813b9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="813b9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="813b9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813b9-125">CommonParameters</span></span>
<span data-ttu-id="813b9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813b9-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="813b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813b9-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="813b9-128">INPUTS</span></span>

### <span data-ttu-id="813b9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="813b9-129">System.String</span></span>

## <span data-ttu-id="813b9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="813b9-130">OUTPUTS</span></span>

### <span data-ttu-id="813b9-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="813b9-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="813b9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="813b9-132">NOTES</span></span>

## <span data-ttu-id="813b9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="813b9-133">RELATED LINKS</span></span>
