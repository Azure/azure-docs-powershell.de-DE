---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: 49da6e1efbd1bb0e6b0ac4dc693d51fe5b58bfac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950307"
---
# <span data-ttu-id="beeda-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beeda-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="beeda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beeda-102">SYNOPSIS</span></span>
<span data-ttu-id="beeda-103">Entfernt eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="beeda-103">Removes a container registry.</span></span>

## <span data-ttu-id="beeda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="beeda-104">SYNTAX</span></span>

### <span data-ttu-id="beeda-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="beeda-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beeda-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beeda-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beeda-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="beeda-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beeda-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="beeda-108">DESCRIPTION</span></span>
<span data-ttu-id="beeda-109">Das Remove-AzContainerRegistry cmdlet entfernt eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="beeda-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="beeda-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="beeda-110">EXAMPLES</span></span>

### <span data-ttu-id="beeda-111">Beispiel 1: Entfernen einer angegebenen Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="beeda-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="beeda-112">Mit diesem Befehl wird die angegebene Containerregistrierung entfernt.</span><span class="sxs-lookup"><span data-stu-id="beeda-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="beeda-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="beeda-113">PARAMETERS</span></span>

### <span data-ttu-id="beeda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeda-114">-DefaultProfile</span></span>
<span data-ttu-id="beeda-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="beeda-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beeda-116">-Name</span><span class="sxs-lookup"><span data-stu-id="beeda-116">-Name</span></span>
<span data-ttu-id="beeda-117">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="beeda-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeda-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beeda-118">-PassThru</span></span>
<span data-ttu-id="beeda-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn das Entfernen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="beeda-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="beeda-120">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="beeda-120">-Registry</span></span>
<span data-ttu-id="beeda-121">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="beeda-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beeda-122">-ResourceGroupName</span></span>
<span data-ttu-id="beeda-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="beeda-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeda-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="beeda-124">-ResourceId</span></span>
<span data-ttu-id="beeda-125">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="beeda-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beeda-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beeda-126">-Confirm</span></span>
<span data-ttu-id="beeda-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beeda-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beeda-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beeda-128">-WhatIf</span></span>
<span data-ttu-id="beeda-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beeda-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beeda-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beeda-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beeda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeda-131">CommonParameters</span></span>
<span data-ttu-id="beeda-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeda-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beeda-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeda-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="beeda-134">INPUTS</span></span>

### <span data-ttu-id="beeda-135">System.String</span><span class="sxs-lookup"><span data-stu-id="beeda-135">System.String</span></span>

## <span data-ttu-id="beeda-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="beeda-136">OUTPUTS</span></span>

### <span data-ttu-id="beeda-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="beeda-137">System.Boolean</span></span>

## <span data-ttu-id="beeda-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="beeda-138">NOTES</span></span>

## <span data-ttu-id="beeda-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="beeda-139">RELATED LINKS</span></span>

[<span data-ttu-id="beeda-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beeda-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="beeda-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beeda-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="beeda-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beeda-142">Update-AzContainerRegistry</span></span>]()

