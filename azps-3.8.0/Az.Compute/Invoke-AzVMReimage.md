---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996187"
---
# <span data-ttu-id="b745c-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b745c-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="b745c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b745c-102">SYNOPSIS</span></span>
<span data-ttu-id="b745c-103">Umbilden einer virtuellen Azure-Maschine</span><span class="sxs-lookup"><span data-stu-id="b745c-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="b745c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b745c-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b745c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b745c-105">DESCRIPTION</span></span>
<span data-ttu-id="b745c-106">Mit dem Cmdlet **Invoke-AzVMReimage** wird eine Azure Virtual Machine erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="b745c-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="b745c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b745c-107">EXAMPLES</span></span>

### <span data-ttu-id="b745c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b745c-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b745c-109">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="b745c-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b745c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b745c-110">PARAMETERS</span></span>

### <span data-ttu-id="b745c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b745c-111">-AsJob</span></span>
<span data-ttu-id="b745c-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b745c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b745c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b745c-113">-DefaultProfile</span></span>
<span data-ttu-id="b745c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b745c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b745c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b745c-115">-ResourceGroupName</span></span>
<span data-ttu-id="b745c-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b745c-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b745c-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="b745c-117">-TempDisk</span></span>
<span data-ttu-id="b745c-118">Gibt an, ob der temporäre Datenträger erneut abgespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b745c-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="b745c-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b745c-119">-VMName</span></span>
<span data-ttu-id="b745c-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b745c-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b745c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b745c-121">-Confirm</span></span>
<span data-ttu-id="b745c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b745c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b745c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b745c-123">-WhatIf</span></span>
<span data-ttu-id="b745c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b745c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b745c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b745c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b745c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b745c-126">CommonParameters</span></span>
<span data-ttu-id="b745c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b745c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b745c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b745c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b745c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b745c-129">INPUTS</span></span>

### <span data-ttu-id="b745c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b745c-130">System.String</span></span>

## <span data-ttu-id="b745c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b745c-131">OUTPUTS</span></span>

### <span data-ttu-id="b745c-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b745c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b745c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b745c-133">NOTES</span></span>

## <span data-ttu-id="b745c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b745c-134">RELATED LINKS</span></span>
