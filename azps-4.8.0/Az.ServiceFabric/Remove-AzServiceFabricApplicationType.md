---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008928"
---
# <span data-ttu-id="36d1f-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36d1f-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="36d1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="36d1f-103">Entfernen Sie den Dienst Fabric, und geben Sie einen Anwendungstyp aus dem Cluster ein.</span><span class="sxs-lookup"><span data-stu-id="36d1f-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="36d1f-104">Dadurch werden alle Typen Versionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="36d1f-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="36d1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36d1f-105">SYNTAX</span></span>

### <span data-ttu-id="36d1f-106">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="36d1f-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36d1f-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d1f-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36d1f-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d1f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36d1f-109">DESCRIPTION</span></span>
<span data-ttu-id="36d1f-110">Mit diesem Cmdlet wird ein Anwendungstyp aus dem Cluster entfernt, und alle Typversionen werden unter dieser Ressource entfernt, allerdings sollten alle darunter liegenden Anwendungen entfernt werden, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="36d1f-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="36d1f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36d1f-111">EXAMPLES</span></span>

### <span data-ttu-id="36d1f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36d1f-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="36d1f-113">In diesem Beispiel wird der Anwendungstyp "testAppType" und alle darunter liegenden Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="36d1f-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="36d1f-114">Wenn Anwendungen vorhanden sind, die mit diesem Typ erstellt wurden, wird mit dem Befehl eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="36d1f-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="36d1f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="36d1f-115">PARAMETERS</span></span>

### <span data-ttu-id="36d1f-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="36d1f-116">-ClusterName</span></span>
<span data-ttu-id="36d1f-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="36d1f-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="36d1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d1f-118">-DefaultProfile</span></span>
<span data-ttu-id="36d1f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36d1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="36d1f-120">-Force</span></span>
<span data-ttu-id="36d1f-121">Ohne Eingabeaufforderung entfernen.</span><span class="sxs-lookup"><span data-stu-id="36d1f-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="36d1f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36d1f-122">-InputObject</span></span>
<span data-ttu-id="36d1f-123">Die Ressource des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="36d1f-123">The application type resource.</span></span>

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

### <span data-ttu-id="36d1f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="36d1f-124">-Name</span></span>
<span data-ttu-id="36d1f-125">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="36d1f-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="36d1f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d1f-126">-PassThru</span></span>
<span data-ttu-id="36d1f-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="36d1f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="36d1f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d1f-128">-ResourceGroupName</span></span>
<span data-ttu-id="36d1f-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="36d1f-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="36d1f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="36d1f-130">-ResourceId</span></span>
<span data-ttu-id="36d1f-131">Arm-Ressourcentyp des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="36d1f-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="36d1f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36d1f-132">-Confirm</span></span>
<span data-ttu-id="36d1f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36d1f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d1f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d1f-134">-WhatIf</span></span>
<span data-ttu-id="36d1f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36d1f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d1f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36d1f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d1f-137">CommonParameters</span></span>
<span data-ttu-id="36d1f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d1f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36d1f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d1f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36d1f-140">INPUTS</span></span>

### <span data-ttu-id="36d1f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="36d1f-141">System.String</span></span>

### <span data-ttu-id="36d1f-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="36d1f-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="36d1f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36d1f-143">OUTPUTS</span></span>

### <span data-ttu-id="36d1f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36d1f-144">System.Boolean</span></span>

## <span data-ttu-id="36d1f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="36d1f-145">NOTES</span></span>

## <span data-ttu-id="36d1f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36d1f-146">RELATED LINKS</span></span>
