---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368877"
---
# <span data-ttu-id="7b1e2-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="7b1e2-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="7b1e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1e2-103">Erstellen Sie einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="7b1e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b1e2-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1e2-106">Das **Cmdlet Invoke-AzVMReimage** stellt einen virtuellen Azure-Computer neu ab.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="7b1e2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b1e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b1e2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b1e2-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7b1e2-109">Mit diesem Befehl wird der virtuelle Computer "VirtualMachine07" in ResourceGroup11 neu abbilden.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7b1e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b1e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7b1e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b1e2-111">-AsJob</span></span>
<span data-ttu-id="7b1e2-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7b1e2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b1e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1e2-113">-DefaultProfile</span></span>
<span data-ttu-id="7b1e2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b1e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b1e2-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7b1e2-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="7b1e2-117">-TempDisk</span></span>
<span data-ttu-id="7b1e2-118">Gibt an, ob der Datenträger neu gebildert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="7b1e2-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="7b1e2-119">-VMName</span></span>
<span data-ttu-id="7b1e2-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="7b1e2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b1e2-121">-Confirm</span></span>
<span data-ttu-id="7b1e2-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1e2-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7b1e2-123">-WhatIf</span></span>
<span data-ttu-id="7b1e2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b1e2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1e2-126">CommonParameters</span></span>
<span data-ttu-id="7b1e2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1e2-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b1e2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1e2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b1e2-129">INPUTS</span></span>

### <span data-ttu-id="7b1e2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7b1e2-130">System.String</span></span>

## <span data-ttu-id="7b1e2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b1e2-131">OUTPUTS</span></span>

### <span data-ttu-id="7b1e2-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7b1e2-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7b1e2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7b1e2-133">NOTES</span></span>

## <span data-ttu-id="7b1e2-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7b1e2-134">RELATED LINKS</span></span>
