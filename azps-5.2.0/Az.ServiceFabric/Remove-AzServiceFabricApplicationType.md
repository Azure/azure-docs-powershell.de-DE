---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300240"
---
# <span data-ttu-id="df4f4-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="df4f4-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="df4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="df4f4-103">Remove Service fabric an application type from the cluster.</span><span class="sxs-lookup"><span data-stu-id="df4f4-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="df4f4-104">Dadurch werden alle Typversionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="df4f4-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="df4f4-105">Unterstützt nur ARM bereitgestellten Anwendungstypen.</span><span class="sxs-lookup"><span data-stu-id="df4f4-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="df4f4-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df4f4-106">SYNTAX</span></span>

### <span data-ttu-id="df4f4-107">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="df4f4-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4f4-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df4f4-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4f4-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df4f4-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4f4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df4f4-110">DESCRIPTION</span></span>
<span data-ttu-id="df4f4-111">Mit diesem Cmdlet wird ein Anwendungstyp aus dem Cluster entfernt, und es wird die Version aller Typen unter dieser Ressource entfernt, aber alle Anwendungen unter dieser Ressource sollten vor dem Ausführen dieses Befehls entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="df4f4-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="df4f4-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df4f4-112">EXAMPLES</span></span>

### <span data-ttu-id="df4f4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df4f4-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="df4f4-114">In diesem Beispiel werden der Anwendungstyp "testAppType" und die hierin enthaltene Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="df4f4-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="df4f4-115">Wenn Anwendungen mit diesem Typ erstellt wurden, wird durch den Befehl eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="df4f4-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="df4f4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df4f4-116">PARAMETERS</span></span>

### <span data-ttu-id="df4f4-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="df4f4-117">-ClusterName</span></span>
<span data-ttu-id="df4f4-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="df4f4-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="df4f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4f4-119">-DefaultProfile</span></span>
<span data-ttu-id="df4f4-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df4f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4f4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="df4f4-121">-Force</span></span>
<span data-ttu-id="df4f4-122">"Ohne Eingabeaufforderung entfernen" aus.</span><span class="sxs-lookup"><span data-stu-id="df4f4-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="df4f4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4f4-123">-InputObject</span></span>
<span data-ttu-id="df4f4-124">Die Anwendungstypressource.</span><span class="sxs-lookup"><span data-stu-id="df4f4-124">The application type resource.</span></span>

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

### <span data-ttu-id="df4f4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="df4f4-125">-Name</span></span>
<span data-ttu-id="df4f4-126">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="df4f4-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="df4f4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df4f4-127">-PassThru</span></span>
<span data-ttu-id="df4f4-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="df4f4-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="df4f4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4f4-129">-ResourceGroupName</span></span>
<span data-ttu-id="df4f4-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="df4f4-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="df4f4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4f4-131">-ResourceId</span></span>
<span data-ttu-id="df4f4-132">Arm ResourceId des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="df4f4-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="df4f4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df4f4-133">-Confirm</span></span>
<span data-ttu-id="df4f4-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df4f4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4f4-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df4f4-135">-WhatIf</span></span>
<span data-ttu-id="df4f4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df4f4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df4f4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df4f4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4f4-138">CommonParameters</span></span>
<span data-ttu-id="df4f4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4f4-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df4f4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4f4-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df4f4-141">INPUTS</span></span>

### <span data-ttu-id="df4f4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="df4f4-142">System.String</span></span>

### <span data-ttu-id="df4f4-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="df4f4-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="df4f4-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df4f4-144">OUTPUTS</span></span>

### <span data-ttu-id="df4f4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df4f4-145">System.Boolean</span></span>

## <span data-ttu-id="df4f4-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df4f4-146">NOTES</span></span>

## <span data-ttu-id="df4f4-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df4f4-147">RELATED LINKS</span></span>
