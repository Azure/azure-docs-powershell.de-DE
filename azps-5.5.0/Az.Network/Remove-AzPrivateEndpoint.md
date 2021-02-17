---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158956"
---
# <span data-ttu-id="82b27-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82b27-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="82b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b27-102">SYNOPSIS</span></span>
<span data-ttu-id="82b27-103">Entfernt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="82b27-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="82b27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82b27-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b27-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82b27-105">DESCRIPTION</span></span>
<span data-ttu-id="82b27-106">Das **Cmdlet "Remove-AzPrivateEndpoint"** entfernt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="82b27-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="82b27-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82b27-107">EXAMPLES</span></span>

### <span data-ttu-id="82b27-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82b27-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="82b27-109">In diesem Beispiel wird ein privater Endpunkt namens "MyPrivateEndpoint1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="82b27-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="82b27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82b27-110">PARAMETERS</span></span>

### <span data-ttu-id="82b27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b27-111">-AsJob</span></span>
<span data-ttu-id="82b27-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82b27-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b27-113">-DefaultProfile</span></span>
<span data-ttu-id="82b27-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82b27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="82b27-115">-Force</span></span>
<span data-ttu-id="82b27-116">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="82b27-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="82b27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82b27-117">-Name</span></span>
<span data-ttu-id="82b27-118">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="82b27-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="82b27-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82b27-119">-PassThru</span></span>
<span data-ttu-id="82b27-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="82b27-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82b27-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="82b27-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82b27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b27-122">-ResourceGroupName</span></span>
<span data-ttu-id="82b27-123">Der Ressourcengruppenname des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="82b27-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="82b27-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82b27-124">-Confirm</span></span>
<span data-ttu-id="82b27-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82b27-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b27-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82b27-126">-WhatIf</span></span>
<span data-ttu-id="82b27-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82b27-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b27-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82b27-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b27-129">CommonParameters</span></span>
<span data-ttu-id="82b27-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b27-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82b27-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b27-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82b27-132">INPUTS</span></span>

### <span data-ttu-id="82b27-133">System.String</span><span class="sxs-lookup"><span data-stu-id="82b27-133">System.String</span></span>

## <span data-ttu-id="82b27-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82b27-134">OUTPUTS</span></span>

### <span data-ttu-id="82b27-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82b27-135">System.Boolean</span></span>

## <span data-ttu-id="82b27-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82b27-136">NOTES</span></span>

## <span data-ttu-id="82b27-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82b27-137">RELATED LINKS</span></span>

[<span data-ttu-id="82b27-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82b27-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="82b27-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82b27-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)