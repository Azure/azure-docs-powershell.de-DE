---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170603"
---
# <span data-ttu-id="50e49-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="50e49-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="50e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e49-102">SYNOPSIS</span></span>
<span data-ttu-id="50e49-103">Entfernen von Inhalten in Der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="50e49-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="50e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50e49-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e49-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50e49-105">DESCRIPTION</span></span>
<span data-ttu-id="50e49-106">Remove-AzFrontDoorContent Zwischenspeicherung von Inhalten in einer Eingangstür</span><span class="sxs-lookup"><span data-stu-id="50e49-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="50e49-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50e49-107">EXAMPLES</span></span>

### <span data-ttu-id="50e49-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50e49-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="50e49-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50e49-109">PARAMETERS</span></span>

### <span data-ttu-id="50e49-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="50e49-110">-ContentPath</span></span>
<span data-ttu-id="50e49-111">Die Pfade zu dem Inhalt, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="50e49-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="50e49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e49-112">-DefaultProfile</span></span>
<span data-ttu-id="50e49-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50e49-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50e49-114">-Name</span><span class="sxs-lookup"><span data-stu-id="50e49-114">-Name</span></span>
<span data-ttu-id="50e49-115">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="50e49-115">Front Door name.</span></span>

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

### <span data-ttu-id="50e49-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50e49-116">-PassThru</span></span>
<span data-ttu-id="50e49-117">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="50e49-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="50e49-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e49-118">-ResourceGroupName</span></span>
<span data-ttu-id="50e49-119">Der Ressourcengruppenname der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="50e49-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="50e49-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50e49-120">-Confirm</span></span>
<span data-ttu-id="50e49-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50e49-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e49-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50e49-122">-WhatIf</span></span>
<span data-ttu-id="50e49-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50e49-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50e49-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50e49-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50e49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e49-125">CommonParameters</span></span>
<span data-ttu-id="50e49-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e49-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50e49-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e49-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50e49-128">INPUTS</span></span>

### <span data-ttu-id="50e49-129">Keine</span><span class="sxs-lookup"><span data-stu-id="50e49-129">None</span></span>

## <span data-ttu-id="50e49-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50e49-130">OUTPUTS</span></span>

### <span data-ttu-id="50e49-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50e49-131">System.Boolean</span></span>

## <span data-ttu-id="50e49-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50e49-132">NOTES</span></span>

## <span data-ttu-id="50e49-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50e49-133">RELATED LINKS</span></span>
