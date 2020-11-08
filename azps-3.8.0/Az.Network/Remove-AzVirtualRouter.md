---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6d879357a71e18d9f1b6beb25044bd5d4394a497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004175"
---
# <span data-ttu-id="aa4fd-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="aa4fd-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="aa4fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4fd-103">Löscht eine Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="aa4fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa4fd-104">SYNTAX</span></span>

### <span data-ttu-id="aa4fd-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa4fd-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4fd-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4fd-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4fd-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4fd-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa4fd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa4fd-108">DESCRIPTION</span></span>
<span data-ttu-id="aa4fd-109">Das Cmdlet **Remove-AzVirtualRouter** löscht eine Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="aa4fd-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="aa4fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa4fd-110">EXAMPLES</span></span>

### <span data-ttu-id="aa4fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa4fd-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="aa4fd-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa4fd-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="aa4fd-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aa4fd-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="aa4fd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa4fd-114">PARAMETERS</span></span>

### <span data-ttu-id="aa4fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa4fd-115">-AsJob</span></span>
<span data-ttu-id="aa4fd-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aa4fd-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4fd-117">-DefaultProfile</span></span>
<span data-ttu-id="aa4fd-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="aa4fd-119">-Force</span></span>
<span data-ttu-id="aa4fd-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="aa4fd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa4fd-121">-InputObject</span></span>
<span data-ttu-id="aa4fd-122">Das Eingabeobjekt für den virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-122">The virtual router input object.</span></span>

```yaml
Type: PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa4fd-123">-PassThru</span></span>
<span data-ttu-id="aa4fd-124">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa4fd-126">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-126">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aa4fd-127">-ResourceId</span></span>
<span data-ttu-id="aa4fd-128">Die Ressourcen-ID des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-128">The virtual router resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-129">-Routername</span><span class="sxs-lookup"><span data-stu-id="aa4fd-129">-RouterName</span></span>
<span data-ttu-id="aa4fd-130">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-130">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa4fd-131">-Confirm</span></span>
<span data-ttu-id="aa4fd-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4fd-133">-WhatIf</span></span>
<span data-ttu-id="aa4fd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa4fd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4fd-136">CommonParameters</span></span>
<span data-ttu-id="aa4fd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4fd-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4fd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4fd-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa4fd-139">INPUTS</span></span>

### <span data-ttu-id="aa4fd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aa4fd-140">System.String</span></span>

### <span data-ttu-id="aa4fd-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="aa4fd-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="aa4fd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa4fd-142">OUTPUTS</span></span>

### <span data-ttu-id="aa4fd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa4fd-143">System.Boolean</span></span>

## <span data-ttu-id="aa4fd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa4fd-144">NOTES</span></span>

## <span data-ttu-id="aa4fd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa4fd-145">RELATED LINKS</span></span>
