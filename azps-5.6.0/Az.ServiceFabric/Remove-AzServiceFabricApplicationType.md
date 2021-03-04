---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: dbd2e29a3136576ecf5596c4a401d689fd0631a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945677"
---
# <span data-ttu-id="bf208-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bf208-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="bf208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf208-102">SYNOPSIS</span></span>
<span data-ttu-id="bf208-103">Entfernen Sie service fabric einen Anwendungstyp aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="bf208-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="bf208-104">Dadurch werden alle Typversionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf208-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="bf208-105">Unterstützt nur ARM bereitgestellten Anwendungstypen.</span><span class="sxs-lookup"><span data-stu-id="bf208-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="bf208-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf208-106">SYNTAX</span></span>

### <span data-ttu-id="bf208-107">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf208-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf208-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf208-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf208-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf208-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf208-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf208-110">DESCRIPTION</span></span>
<span data-ttu-id="bf208-111">Dieses Cmdlet entfernt einen Anwendungstyp aus dem Cluster und entfernt alle Typversion unter dieser Ressource, aber alle Anwendungen unter dieser Ressource sollten entfernt werden, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf208-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="bf208-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf208-112">EXAMPLES</span></span>

### <span data-ttu-id="bf208-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf208-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="bf208-114">In diesem Beispiel werden der Anwendungstyp "testAppType" und die ganze Version unter dem Beispiel entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf208-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="bf208-115">Wenn anwendungen mit diesem Typ erstellt wurden, wird mit dem Befehl eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="bf208-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="bf208-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf208-116">PARAMETERS</span></span>

### <span data-ttu-id="bf208-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bf208-117">-ClusterName</span></span>
<span data-ttu-id="bf208-118">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="bf208-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf208-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf208-119">-DefaultProfile</span></span>
<span data-ttu-id="bf208-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf208-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf208-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="bf208-121">-Force</span></span>
<span data-ttu-id="bf208-122">Entfernen Sie ohne Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="bf208-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="bf208-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf208-123">-InputObject</span></span>
<span data-ttu-id="bf208-124">Die Ressource für den Anwendungstyp.</span><span class="sxs-lookup"><span data-stu-id="bf208-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf208-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bf208-125">-Name</span></span>
<span data-ttu-id="bf208-126">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="bf208-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf208-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf208-127">-PassThru</span></span>
<span data-ttu-id="bf208-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bf208-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bf208-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf208-129">-ResourceGroupName</span></span>
<span data-ttu-id="bf208-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bf208-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf208-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf208-131">-ResourceId</span></span>
<span data-ttu-id="bf208-132">Arm ResourceId des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="bf208-132">Arm ResourceId of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf208-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf208-133">-Confirm</span></span>
<span data-ttu-id="bf208-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf208-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf208-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf208-135">-WhatIf</span></span>
<span data-ttu-id="bf208-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf208-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf208-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf208-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf208-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf208-138">CommonParameters</span></span>
<span data-ttu-id="bf208-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf208-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf208-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf208-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf208-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf208-141">INPUTS</span></span>

### <span data-ttu-id="bf208-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bf208-142">System.String</span></span>

### <span data-ttu-id="bf208-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="bf208-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="bf208-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf208-144">OUTPUTS</span></span>

### <span data-ttu-id="bf208-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf208-145">System.Boolean</span></span>

## <span data-ttu-id="bf208-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf208-146">NOTES</span></span>

## <span data-ttu-id="bf208-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf208-147">RELATED LINKS</span></span>
