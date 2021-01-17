---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473451"
---
# <span data-ttu-id="bb411-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb411-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="bb411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb411-102">SYNOPSIS</span></span>
<span data-ttu-id="bb411-103">Entfernt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="bb411-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="bb411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb411-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb411-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb411-105">DESCRIPTION</span></span>
<span data-ttu-id="bb411-106">Das **Cmdlet "Remove-AzPrivateEndpoint"** entfernt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="bb411-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="bb411-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb411-107">EXAMPLES</span></span>

### <span data-ttu-id="bb411-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb411-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="bb411-109">In diesem Beispiel wird ein privater Endpunkt namens "MyPrivateEndpoint1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb411-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="bb411-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb411-110">PARAMETERS</span></span>

### <span data-ttu-id="bb411-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb411-111">-AsJob</span></span>
<span data-ttu-id="bb411-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bb411-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb411-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb411-113">-DefaultProfile</span></span>
<span data-ttu-id="bb411-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb411-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb411-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb411-115">-Force</span></span>
<span data-ttu-id="bb411-116">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="bb411-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="bb411-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bb411-117">-Name</span></span>
<span data-ttu-id="bb411-118">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="bb411-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="bb411-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb411-119">-PassThru</span></span>
<span data-ttu-id="bb411-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bb411-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb411-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bb411-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb411-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb411-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb411-123">Der Ressourcengruppenname des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="bb411-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="bb411-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb411-124">-Confirm</span></span>
<span data-ttu-id="bb411-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb411-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb411-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb411-126">-WhatIf</span></span>
<span data-ttu-id="bb411-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb411-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb411-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb411-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb411-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb411-129">CommonParameters</span></span>
<span data-ttu-id="bb411-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb411-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb411-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb411-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb411-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb411-132">INPUTS</span></span>

### <span data-ttu-id="bb411-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bb411-133">System.String</span></span>

## <span data-ttu-id="bb411-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb411-134">OUTPUTS</span></span>

### <span data-ttu-id="bb411-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb411-135">System.Boolean</span></span>

## <span data-ttu-id="bb411-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb411-136">NOTES</span></span>

## <span data-ttu-id="bb411-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb411-137">RELATED LINKS</span></span>

[<span data-ttu-id="bb411-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb411-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="bb411-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb411-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)