---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 410509f59cc34dd139761a3e4ddb5de9907ef720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945634"
---
# <span data-ttu-id="62d15-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="62d15-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="62d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62d15-102">SYNOPSIS</span></span>
<span data-ttu-id="62d15-103">Entfernen Sie die Vm-Erweiterung aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="62d15-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="62d15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62d15-104">SYNTAX</span></span>

### <span data-ttu-id="62d15-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="62d15-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d15-106">ByName</span><span class="sxs-lookup"><span data-stu-id="62d15-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62d15-107">DESCRIPTION</span></span>
<span data-ttu-id="62d15-108">Entfernen Sie die Erweiterung vm vom Knotentyp nach Name.</span><span class="sxs-lookup"><span data-stu-id="62d15-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="62d15-109">Verwenden [Sie Get-AzServiceFabricManagedNodeType,](./Get-AzServiceFabricManagedNodeType.md) und sehen Sie sich die VmExtensions-Eigenschaft an, um die aktuelle Erweiterung für den Knotentyp zu sehen.</span><span class="sxs-lookup"><span data-stu-id="62d15-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="62d15-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62d15-110">EXAMPLES</span></span>

### <span data-ttu-id="62d15-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62d15-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="62d15-112">Entfernen Sie die Erweiterung vom Knotentyp nach Name.</span><span class="sxs-lookup"><span data-stu-id="62d15-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="62d15-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="62d15-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="62d15-114">Entfernen Sie die Erweiterung vom Knotentyp nach Name mit Piping.</span><span class="sxs-lookup"><span data-stu-id="62d15-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="62d15-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62d15-115">PARAMETERS</span></span>

### <span data-ttu-id="62d15-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62d15-116">-AsJob</span></span>
<span data-ttu-id="62d15-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="62d15-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="62d15-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="62d15-118">-ClusterName</span></span>
<span data-ttu-id="62d15-119">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="62d15-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d15-120">-DefaultProfile</span></span>
<span data-ttu-id="62d15-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62d15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d15-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62d15-122">-InputObject</span></span>
<span data-ttu-id="62d15-123">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="62d15-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d15-124">-Name</span><span class="sxs-lookup"><span data-stu-id="62d15-124">-Name</span></span>
<span data-ttu-id="62d15-125">Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="62d15-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d15-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="62d15-126">-NodeTypeName</span></span>
<span data-ttu-id="62d15-127">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="62d15-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d15-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62d15-128">-PassThru</span></span>
<span data-ttu-id="62d15-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="62d15-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="62d15-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d15-130">-ResourceGroupName</span></span>
<span data-ttu-id="62d15-131">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="62d15-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d15-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62d15-132">-Confirm</span></span>
<span data-ttu-id="62d15-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62d15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d15-134">-WhatIf</span></span>
<span data-ttu-id="62d15-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62d15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d15-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62d15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d15-137">CommonParameters</span></span>
<span data-ttu-id="62d15-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d15-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62d15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d15-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62d15-140">INPUTS</span></span>

### <span data-ttu-id="62d15-141">System.String</span><span class="sxs-lookup"><span data-stu-id="62d15-141">System.String</span></span>

## <span data-ttu-id="62d15-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62d15-142">OUTPUTS</span></span>

### <span data-ttu-id="62d15-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62d15-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="62d15-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="62d15-144">NOTES</span></span>

## <span data-ttu-id="62d15-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="62d15-145">RELATED LINKS</span></span>
