---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 96560f393c361996ad906d1207647ba53f53cbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944242"
---
# <span data-ttu-id="57780-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="57780-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="57780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57780-102">SYNOPSIS</span></span>
<span data-ttu-id="57780-103">Erstellen Sie ein erneutes Abbild eines virtuellen Azure-Computers.</span><span class="sxs-lookup"><span data-stu-id="57780-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="57780-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57780-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57780-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57780-105">DESCRIPTION</span></span>
<span data-ttu-id="57780-106">Das **Cmdlet Invoke-AzVMReimage** stellt einen virtuellen Azure-Computer neu nach.</span><span class="sxs-lookup"><span data-stu-id="57780-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="57780-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57780-107">EXAMPLES</span></span>

### <span data-ttu-id="57780-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57780-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="57780-109">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu nachgebildt.</span><span class="sxs-lookup"><span data-stu-id="57780-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="57780-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="57780-110">PARAMETERS</span></span>

### <span data-ttu-id="57780-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57780-111">-AsJob</span></span>
<span data-ttu-id="57780-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="57780-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57780-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57780-113">-DefaultProfile</span></span>
<span data-ttu-id="57780-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57780-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57780-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57780-115">-ResourceGroupName</span></span>
<span data-ttu-id="57780-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="57780-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="57780-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="57780-117">-TempDisk</span></span>
<span data-ttu-id="57780-118">Gibt an, ob der Temp-Datenträger neu gebildt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57780-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="57780-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="57780-119">-VMName</span></span>
<span data-ttu-id="57780-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="57780-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="57780-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57780-121">-Confirm</span></span>
<span data-ttu-id="57780-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57780-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57780-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57780-123">-WhatIf</span></span>
<span data-ttu-id="57780-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57780-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57780-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57780-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57780-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57780-126">CommonParameters</span></span>
<span data-ttu-id="57780-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57780-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57780-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57780-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57780-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57780-129">INPUTS</span></span>

### <span data-ttu-id="57780-130">System.String</span><span class="sxs-lookup"><span data-stu-id="57780-130">System.String</span></span>

## <span data-ttu-id="57780-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57780-131">OUTPUTS</span></span>

### <span data-ttu-id="57780-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="57780-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="57780-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="57780-133">NOTES</span></span>

## <span data-ttu-id="57780-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="57780-134">RELATED LINKS</span></span>
