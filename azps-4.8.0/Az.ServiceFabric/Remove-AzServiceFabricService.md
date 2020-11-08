---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008930"
---
# <span data-ttu-id="bdef9-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bdef9-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="bdef9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdef9-102">SYNOPSIS</span></span>
<span data-ttu-id="bdef9-103">Entfernen eines Diensts aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="bdef9-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="bdef9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdef9-104">SYNTAX</span></span>

### <span data-ttu-id="bdef9-105">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdef9-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdef9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdef9-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdef9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bdef9-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdef9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdef9-108">DESCRIPTION</span></span>
<span data-ttu-id="bdef9-109">Mit diesem Cmdlet wird ein Dienst Formular des Clusters entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdef9-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="bdef9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdef9-110">EXAMPLES</span></span>

### <span data-ttu-id="bdef9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdef9-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="bdef9-112">In diesem Beispiel wird der Dienst "testApp ~ testService1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdef9-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="bdef9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdef9-113">PARAMETERS</span></span>

### <span data-ttu-id="bdef9-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bdef9-114">-ApplicationName</span></span>
<span data-ttu-id="bdef9-115">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="bdef9-115">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdef9-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="bdef9-116">-ClusterName</span></span>
<span data-ttu-id="bdef9-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="bdef9-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bdef9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdef9-118">-DefaultProfile</span></span>
<span data-ttu-id="bdef9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdef9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdef9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bdef9-120">-Force</span></span>
<span data-ttu-id="bdef9-121">Ohne Eingabeaufforderung entfernen.</span><span class="sxs-lookup"><span data-stu-id="bdef9-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="bdef9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdef9-122">-InputObject</span></span>
<span data-ttu-id="bdef9-123">Die Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="bdef9-123">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdef9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bdef9-124">-Name</span></span>
<span data-ttu-id="bdef9-125">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="bdef9-125">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdef9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdef9-126">-PassThru</span></span>
<span data-ttu-id="bdef9-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bdef9-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bdef9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdef9-128">-ResourceGroupName</span></span>
<span data-ttu-id="bdef9-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bdef9-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bdef9-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bdef9-130">-ResourceId</span></span>
<span data-ttu-id="bdef9-131">Arm-resourcecode des Diensts.</span><span class="sxs-lookup"><span data-stu-id="bdef9-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="bdef9-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdef9-132">-Confirm</span></span>
<span data-ttu-id="bdef9-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdef9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdef9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdef9-134">-WhatIf</span></span>
<span data-ttu-id="bdef9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdef9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdef9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdef9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdef9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdef9-137">CommonParameters</span></span>
<span data-ttu-id="bdef9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdef9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdef9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdef9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdef9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdef9-140">INPUTS</span></span>

### <span data-ttu-id="bdef9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bdef9-141">System.String</span></span>

### <span data-ttu-id="bdef9-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="bdef9-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="bdef9-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdef9-143">OUTPUTS</span></span>

### <span data-ttu-id="bdef9-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdef9-144">System.Boolean</span></span>

## <span data-ttu-id="bdef9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdef9-145">NOTES</span></span>

## <span data-ttu-id="bdef9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdef9-146">RELATED LINKS</span></span>
