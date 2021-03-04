---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: f73569e8e40af5111a738496ba6ad41ff03058f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927339"
---
# <span data-ttu-id="41295-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="41295-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="41295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41295-102">SYNOPSIS</span></span>
<span data-ttu-id="41295-103">Wandelt einen virtuellen Computer mit blobbasierten Datenträgern in einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="41295-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="41295-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41295-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41295-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41295-105">DESCRIPTION</span></span>
<span data-ttu-id="41295-106">Das **Cmdlet ConvertTo-AzVMManagedDisk** konvertiert einen virtuellen Computer mit blobbasierten Datenträgern in einen virtuellen Computer mit verwalteten Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="41295-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="41295-107">Der virtuelle Computer muss vor dem Aufrufen dieses Vorgangs beendet werden.</span><span class="sxs-lookup"><span data-stu-id="41295-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="41295-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41295-108">EXAMPLES</span></span>

### <span data-ttu-id="41295-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41295-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="41295-110">Mit diesem Befehl werden die blobbasierten Datenträger des virtuellen Computers namens "VM01" in der Ressourcengruppe "ResourceGroup01" in verwaltete Datenträger konvertiert.</span><span class="sxs-lookup"><span data-stu-id="41295-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="41295-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41295-111">PARAMETERS</span></span>

### <span data-ttu-id="41295-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41295-112">-AsJob</span></span>
<span data-ttu-id="41295-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="41295-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41295-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41295-114">-DefaultProfile</span></span>
<span data-ttu-id="41295-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41295-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41295-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41295-116">-ResourceGroupName</span></span>
<span data-ttu-id="41295-117">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="41295-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="41295-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="41295-118">-VMName</span></span>
<span data-ttu-id="41295-119">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="41295-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="41295-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41295-120">-Confirm</span></span>
<span data-ttu-id="41295-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41295-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41295-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41295-122">-WhatIf</span></span>
<span data-ttu-id="41295-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41295-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41295-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41295-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41295-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41295-125">CommonParameters</span></span>
<span data-ttu-id="41295-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41295-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41295-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41295-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41295-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41295-128">INPUTS</span></span>

### <span data-ttu-id="41295-129">System.String</span><span class="sxs-lookup"><span data-stu-id="41295-129">System.String</span></span>

## <span data-ttu-id="41295-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41295-130">OUTPUTS</span></span>

### <span data-ttu-id="41295-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="41295-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="41295-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41295-132">NOTES</span></span>

## <span data-ttu-id="41295-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41295-133">RELATED LINKS</span></span>
