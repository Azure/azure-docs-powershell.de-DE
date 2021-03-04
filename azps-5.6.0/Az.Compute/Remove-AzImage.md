---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: bcbfaefcc94415acdd1100025e1eefc2977f107a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920040"
---
# <span data-ttu-id="3c379-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="3c379-101">Remove-AzImage</span></span>

## <span data-ttu-id="3c379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c379-102">SYNOPSIS</span></span>
<span data-ttu-id="3c379-103">Entfernt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="3c379-103">Removes an image.</span></span>

## <span data-ttu-id="3c379-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c379-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c379-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c379-105">DESCRIPTION</span></span>
<span data-ttu-id="3c379-106">Das **Cmdlet Remove-AzImage** entfernt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="3c379-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="3c379-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c379-107">EXAMPLES</span></span>

### <span data-ttu-id="3c379-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c379-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="3c379-109">Mit diesem Befehl wird das Bild "Image01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3c379-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3c379-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3c379-110">PARAMETERS</span></span>

### <span data-ttu-id="3c379-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c379-111">-AsJob</span></span>
<span data-ttu-id="3c379-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="3c379-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3c379-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c379-113">-DefaultProfile</span></span>
<span data-ttu-id="3c379-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c379-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c379-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3c379-115">-Force</span></span>
<span data-ttu-id="3c379-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3c379-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c379-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3c379-117">-ImageName</span></span>
<span data-ttu-id="3c379-118">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="3c379-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="3c379-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c379-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c379-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3c379-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3c379-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c379-121">-Confirm</span></span>
<span data-ttu-id="3c379-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c379-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c379-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c379-123">-WhatIf</span></span>
<span data-ttu-id="3c379-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c379-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c379-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c379-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c379-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c379-126">CommonParameters</span></span>
<span data-ttu-id="3c379-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c379-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c379-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c379-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c379-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c379-129">INPUTS</span></span>

### <span data-ttu-id="3c379-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3c379-130">System.String</span></span>

## <span data-ttu-id="3c379-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c379-131">OUTPUTS</span></span>

### <span data-ttu-id="3c379-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3c379-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3c379-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3c379-133">NOTES</span></span>

## <span data-ttu-id="3c379-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3c379-134">RELATED LINKS</span></span>
