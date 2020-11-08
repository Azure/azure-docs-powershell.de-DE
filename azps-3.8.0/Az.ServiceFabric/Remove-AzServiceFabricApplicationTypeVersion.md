---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: f50baca10d3079ac800b694670ce2b4c8c85fc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996383"
---
# <span data-ttu-id="d13b1-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d13b1-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="d13b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d13b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d13b1-103">Entfernen Sie Service Fabric, eine Anwendungstypen Version aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="d13b1-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="d13b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d13b1-104">SYNTAX</span></span>

### <span data-ttu-id="d13b1-105">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="d13b1-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13b1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d13b1-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13b1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d13b1-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13b1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d13b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d13b1-109">Mit diesem Cmdlet wird Service Fabric eine Anwendungstypen Version aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="d13b1-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="d13b1-110">Alle Anwendungen unter dieser Ressource müssen entfernt werden, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="d13b1-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="d13b1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d13b1-111">EXAMPLES</span></span>

### <span data-ttu-id="d13b1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d13b1-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="d13b1-113">In diesem Beispiel wird die Version "V1" unter dem Typ "testAppType" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d13b1-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="d13b1-114">Es gibt alle Anwendungen unter dieser Ressource der Befehl löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="d13b1-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="d13b1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d13b1-115">PARAMETERS</span></span>

### <span data-ttu-id="d13b1-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d13b1-116">-ClusterName</span></span>
<span data-ttu-id="d13b1-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="d13b1-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d13b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13b1-118">-DefaultProfile</span></span>
<span data-ttu-id="d13b1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d13b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d13b1-120">-Force</span></span>
<span data-ttu-id="d13b1-121">Ohne Eingabeaufforderung entfernen.</span><span class="sxs-lookup"><span data-stu-id="d13b1-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="d13b1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d13b1-122">-InputObject</span></span>
<span data-ttu-id="d13b1-123">Die Version des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="d13b1-123">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d13b1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d13b1-124">-Name</span></span>
<span data-ttu-id="d13b1-125">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="d13b1-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d13b1-126">-PassThru</span></span>
<span data-ttu-id="d13b1-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="d13b1-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d13b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="d13b1-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d13b1-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d13b1-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d13b1-130">-ResourceId</span></span>
<span data-ttu-id="d13b1-131">Arm-Ressourcen-Nr. des Anwendungstyps Version.</span><span class="sxs-lookup"><span data-stu-id="d13b1-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="d13b1-132">-Version</span><span class="sxs-lookup"><span data-stu-id="d13b1-132">-Version</span></span>
<span data-ttu-id="d13b1-133">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="d13b1-133">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13b1-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d13b1-134">-Confirm</span></span>
<span data-ttu-id="d13b1-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d13b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13b1-136">-WhatIf</span></span>
<span data-ttu-id="d13b1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d13b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d13b1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d13b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13b1-139">CommonParameters</span></span>
<span data-ttu-id="d13b1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d13b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13b1-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13b1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13b1-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d13b1-142">INPUTS</span></span>

### <span data-ttu-id="d13b1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d13b1-143">System.String</span></span>

### <span data-ttu-id="d13b1-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d13b1-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="d13b1-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d13b1-145">OUTPUTS</span></span>

### <span data-ttu-id="d13b1-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d13b1-146">System.Boolean</span></span>

## <span data-ttu-id="d13b1-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d13b1-147">NOTES</span></span>

## <span data-ttu-id="d13b1-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d13b1-148">RELATED LINKS</span></span>
