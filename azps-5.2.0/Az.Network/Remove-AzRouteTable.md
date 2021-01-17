---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365306"
---
# <span data-ttu-id="c643b-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c643b-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="c643b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c643b-102">SYNOPSIS</span></span>
<span data-ttu-id="c643b-103">Entfernt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="c643b-103">Removes a route table.</span></span>

## <span data-ttu-id="c643b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c643b-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c643b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c643b-105">DESCRIPTION</span></span>
<span data-ttu-id="c643b-106">Das **Cmdlet "Remove-AzRouteTable"** entfernt eine Azure-Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="c643b-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="c643b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c643b-107">EXAMPLES</span></span>

### <span data-ttu-id="c643b-108">Beispiel 1: Entfernen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="c643b-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c643b-109">Mit diesem Befehl wird die Routentabelle mit dem Namen "RouteTable01" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c643b-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="c643b-110">Das Cmdlet fordert Sie zur Bestätigung auf, bevor die Tabelle entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c643b-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="c643b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c643b-111">PARAMETERS</span></span>

### <span data-ttu-id="c643b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c643b-112">-AsJob</span></span>
<span data-ttu-id="c643b-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c643b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c643b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c643b-114">-DefaultProfile</span></span>
<span data-ttu-id="c643b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c643b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c643b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c643b-116">-Force</span></span>
<span data-ttu-id="c643b-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c643b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c643b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c643b-118">-Name</span></span>
<span data-ttu-id="c643b-119">Gibt den Namen der Routentabelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c643b-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c643b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c643b-120">-PassThru</span></span>
<span data-ttu-id="c643b-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c643b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c643b-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c643b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c643b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c643b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c643b-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Routentabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c643b-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c643b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c643b-125">-Confirm</span></span>
<span data-ttu-id="c643b-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c643b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c643b-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c643b-127">-WhatIf</span></span>
<span data-ttu-id="c643b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c643b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c643b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c643b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c643b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c643b-130">CommonParameters</span></span>
<span data-ttu-id="c643b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c643b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c643b-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c643b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c643b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c643b-133">INPUTS</span></span>

### <span data-ttu-id="c643b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c643b-134">System.String</span></span>

## <span data-ttu-id="c643b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c643b-135">OUTPUTS</span></span>

### <span data-ttu-id="c643b-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c643b-136">System.Boolean</span></span>

## <span data-ttu-id="c643b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c643b-137">NOTES</span></span>

## <span data-ttu-id="c643b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c643b-138">RELATED LINKS</span></span>

[<span data-ttu-id="c643b-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c643b-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c643b-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c643b-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="c643b-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c643b-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


