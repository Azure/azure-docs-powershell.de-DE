---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357929"
---
# <span data-ttu-id="7cb60-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="7cb60-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="7cb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb60-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb60-103">Entfernen Sie die erweiterung "vm" aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="7cb60-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="7cb60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cb60-104">SYNTAX</span></span>

### <span data-ttu-id="7cb60-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cb60-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb60-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7cb60-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb60-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cb60-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb60-108">Entfernen Sie die erweiterung "vm" nach Name aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="7cb60-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="7cb60-109">Verwenden [Sie "Get-AzServiceFabricManagedNodeType",](./Get-AzServiceFabricManagedNodeType.md) und sehen Sie sich die Eigenschaft "VmExtensions" an, um die aktuelle Erweiterung für den Knotentyp zu sehen.</span><span class="sxs-lookup"><span data-stu-id="7cb60-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="7cb60-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cb60-110">EXAMPLES</span></span>

### <span data-ttu-id="7cb60-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cb60-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="7cb60-112">Entfernen Sie die Erweiterung vom Knotentyp nach Name.</span><span class="sxs-lookup"><span data-stu-id="7cb60-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="7cb60-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7cb60-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="7cb60-114">Entfernen Sie die Erweiterung vom Knotentyp nach Name mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7cb60-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="7cb60-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cb60-115">PARAMETERS</span></span>

### <span data-ttu-id="7cb60-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb60-116">-AsJob</span></span>
<span data-ttu-id="7cb60-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="7cb60-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7cb60-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7cb60-118">-ClusterName</span></span>
<span data-ttu-id="7cb60-119">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="7cb60-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7cb60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb60-120">-DefaultProfile</span></span>
<span data-ttu-id="7cb60-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cb60-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb60-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb60-122">-InputObject</span></span>
<span data-ttu-id="7cb60-123">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="7cb60-123">Node type resource</span></span>

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

### <span data-ttu-id="7cb60-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7cb60-124">-Name</span></span>
<span data-ttu-id="7cb60-125">Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="7cb60-125">extension name.</span></span>

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

### <span data-ttu-id="7cb60-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="7cb60-126">-NodeTypeName</span></span>
<span data-ttu-id="7cb60-127">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="7cb60-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="7cb60-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cb60-128">-PassThru</span></span>
<span data-ttu-id="7cb60-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7cb60-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7cb60-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb60-130">-ResourceGroupName</span></span>
<span data-ttu-id="7cb60-131">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7cb60-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7cb60-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cb60-132">-Confirm</span></span>
<span data-ttu-id="7cb60-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7cb60-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb60-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7cb60-134">-WhatIf</span></span>
<span data-ttu-id="7cb60-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cb60-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb60-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cb60-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb60-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb60-137">CommonParameters</span></span>
<span data-ttu-id="7cb60-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb60-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb60-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cb60-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb60-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cb60-140">INPUTS</span></span>

### <span data-ttu-id="7cb60-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7cb60-141">System.String</span></span>

## <span data-ttu-id="7cb60-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cb60-142">OUTPUTS</span></span>

### <span data-ttu-id="7cb60-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7cb60-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="7cb60-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7cb60-144">NOTES</span></span>

## <span data-ttu-id="7cb60-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7cb60-145">RELATED LINKS</span></span>
