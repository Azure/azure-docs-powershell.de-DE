---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165553"
---
# <span data-ttu-id="23987-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="23987-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="23987-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23987-102">SYNOPSIS</span></span>
<span data-ttu-id="23987-103">Entfernen Sie die VM-Erweiterung vom Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="23987-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="23987-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23987-104">SYNTAX</span></span>

### <span data-ttu-id="23987-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="23987-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23987-106">ByName</span><span class="sxs-lookup"><span data-stu-id="23987-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23987-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23987-107">DESCRIPTION</span></span>
<span data-ttu-id="23987-108">Entfernen Sie die VM-Erweiterung vom Knotentyp nach Namen.</span><span class="sxs-lookup"><span data-stu-id="23987-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="23987-109">Verwenden Sie [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) , und schauen Sie sich die VmExtensions-Eigenschaft an, um die aktuelle Erweiterung des Knotentyps anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="23987-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="23987-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23987-110">EXAMPLES</span></span>

### <span data-ttu-id="23987-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23987-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="23987-112">Entfernen Sie die Erweiterung vom Knotentyp nach Namen.</span><span class="sxs-lookup"><span data-stu-id="23987-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="23987-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23987-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="23987-114">Entfernen Sie die Erweiterung aus dem Knotentyp mit dem Namen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="23987-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="23987-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="23987-115">PARAMETERS</span></span>

### <span data-ttu-id="23987-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23987-116">-AsJob</span></span>
<span data-ttu-id="23987-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="23987-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="23987-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="23987-118">-ClusterName</span></span>
<span data-ttu-id="23987-119">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="23987-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="23987-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23987-120">-DefaultProfile</span></span>
<span data-ttu-id="23987-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23987-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23987-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23987-122">-InputObject</span></span>
<span data-ttu-id="23987-123">Knotentyp Ressource</span><span class="sxs-lookup"><span data-stu-id="23987-123">Node type resource</span></span>

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

### <span data-ttu-id="23987-124">-Name</span><span class="sxs-lookup"><span data-stu-id="23987-124">-Name</span></span>
<span data-ttu-id="23987-125">Name der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="23987-125">extension name.</span></span>

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

### <span data-ttu-id="23987-126">-NodeType</span><span class="sxs-lookup"><span data-stu-id="23987-126">-NodeTypeName</span></span>
<span data-ttu-id="23987-127">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="23987-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="23987-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23987-128">-PassThru</span></span>
<span data-ttu-id="23987-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="23987-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="23987-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23987-130">-ResourceGroupName</span></span>
<span data-ttu-id="23987-131">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="23987-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="23987-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23987-132">-Confirm</span></span>
<span data-ttu-id="23987-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23987-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23987-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23987-134">-WhatIf</span></span>
<span data-ttu-id="23987-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23987-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23987-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23987-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23987-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23987-137">CommonParameters</span></span>
<span data-ttu-id="23987-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23987-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23987-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23987-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23987-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23987-140">INPUTS</span></span>

### <span data-ttu-id="23987-141">System. String</span><span class="sxs-lookup"><span data-stu-id="23987-141">System.String</span></span>

## <span data-ttu-id="23987-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23987-142">OUTPUTS</span></span>

### <span data-ttu-id="23987-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="23987-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="23987-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="23987-144">NOTES</span></span>

## <span data-ttu-id="23987-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23987-145">RELATED LINKS</span></span>
