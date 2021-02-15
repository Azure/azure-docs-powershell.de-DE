---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166572"
---
# <span data-ttu-id="9fd99-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9fd99-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="9fd99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fd99-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd99-103">Konvertiert einen virtuellen Computer mit blob-basierten Datenträgern in einen virtuellen Computer mit verwalteten Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="9fd99-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="9fd99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fd99-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd99-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fd99-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd99-106">Das **Cmdlet ConvertTo-AzVMManagedDisk** konvertiert einen virtuellen Computer mit blob-basierten Datenträgern in einen virtuellen Computer mit verwalteten Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="9fd99-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="9fd99-107">Der virtuelle Computer muss "stop-deallocated" sein, bevor dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fd99-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="9fd99-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9fd99-108">EXAMPLES</span></span>

### <span data-ttu-id="9fd99-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9fd99-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="9fd99-110">Mit diesem Befehl werden die blob-basierten Datenträger des virtuellen Computers "VM01" in der Ressourcengruppe "ResourceGroup01" in verwaltete Datenträger konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9fd99-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="9fd99-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fd99-111">PARAMETERS</span></span>

### <span data-ttu-id="9fd99-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fd99-112">-AsJob</span></span>
<span data-ttu-id="9fd99-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9fd99-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fd99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd99-114">-DefaultProfile</span></span>
<span data-ttu-id="9fd99-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fd99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fd99-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd99-116">-ResourceGroupName</span></span>
<span data-ttu-id="9fd99-117">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9fd99-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9fd99-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9fd99-118">-VMName</span></span>
<span data-ttu-id="9fd99-119">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9fd99-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9fd99-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fd99-120">-Confirm</span></span>
<span data-ttu-id="9fd99-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fd99-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fd99-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9fd99-122">-WhatIf</span></span>
<span data-ttu-id="9fd99-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fd99-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fd99-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fd99-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fd99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd99-125">CommonParameters</span></span>
<span data-ttu-id="9fd99-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd99-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fd99-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd99-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9fd99-128">INPUTS</span></span>

### <span data-ttu-id="9fd99-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9fd99-129">System.String</span></span>

## <span data-ttu-id="9fd99-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9fd99-130">OUTPUTS</span></span>

### <span data-ttu-id="9fd99-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9fd99-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9fd99-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9fd99-132">NOTES</span></span>

## <span data-ttu-id="9fd99-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9fd99-133">RELATED LINKS</span></span>
