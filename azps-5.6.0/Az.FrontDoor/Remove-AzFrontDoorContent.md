---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: 608c80322e46f3c6871bac0350fcc8ae5a5113bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950235"
---
# <span data-ttu-id="4dc96-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="4dc96-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="4dc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc96-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc96-103">Entfernen von Inhalten in der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="4dc96-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="4dc96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dc96-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc96-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dc96-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc96-106">Remove-AzFrontDoorContent entfernt zwischengespeicherten Inhalt in einer Eingangstür</span><span class="sxs-lookup"><span data-stu-id="4dc96-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="4dc96-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dc96-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc96-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dc96-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="4dc96-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4dc96-109">PARAMETERS</span></span>

### <span data-ttu-id="4dc96-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="4dc96-110">-ContentPath</span></span>
<span data-ttu-id="4dc96-111">Die Pfade zu den zu löschende Inhalten.</span><span class="sxs-lookup"><span data-stu-id="4dc96-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc96-112">-DefaultProfile</span></span>
<span data-ttu-id="4dc96-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dc96-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc96-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4dc96-114">-Name</span></span>
<span data-ttu-id="4dc96-115">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="4dc96-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc96-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dc96-116">-PassThru</span></span>
<span data-ttu-id="4dc96-117">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="4dc96-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="4dc96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc96-118">-ResourceGroupName</span></span>
<span data-ttu-id="4dc96-119">Der Ressourcengruppenname der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="4dc96-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc96-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4dc96-120">-Confirm</span></span>
<span data-ttu-id="4dc96-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dc96-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc96-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc96-122">-WhatIf</span></span>
<span data-ttu-id="4dc96-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc96-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc96-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dc96-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc96-125">CommonParameters</span></span>
<span data-ttu-id="4dc96-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc96-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dc96-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc96-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dc96-128">INPUTS</span></span>

### <span data-ttu-id="4dc96-129">Keine</span><span class="sxs-lookup"><span data-stu-id="4dc96-129">None</span></span>

## <span data-ttu-id="4dc96-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dc96-130">OUTPUTS</span></span>

### <span data-ttu-id="4dc96-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dc96-131">System.Boolean</span></span>

## <span data-ttu-id="4dc96-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4dc96-132">NOTES</span></span>

## <span data-ttu-id="4dc96-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4dc96-133">RELATED LINKS</span></span>
