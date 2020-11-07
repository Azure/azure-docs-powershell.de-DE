---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 74398a027a7ec9de916640b39834cb1045cfe1a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824700"
---
# <span data-ttu-id="7e81f-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e81f-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="7e81f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e81f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e81f-103">Entfernen Sie Service Fabric, eine Anwendungstypen Version aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="7e81f-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="7e81f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e81f-104">SYNTAX</span></span>

### <span data-ttu-id="7e81f-105">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e81f-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e81f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e81f-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e81f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e81f-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e81f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e81f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e81f-109">Mit diesem Cmdlet wird Service Fabric eine Anwendungstypen Version aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="7e81f-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="7e81f-110">Alle Anwendungen unter dieser Ressource müssen entfernt werden, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e81f-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="7e81f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e81f-111">EXAMPLES</span></span>

### <span data-ttu-id="7e81f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e81f-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="7e81f-113">In diesem Beispiel wird die Version "V1" unter dem Typ "testAppType" entfernt.</span><span class="sxs-lookup"><span data-stu-id="7e81f-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="7e81f-114">Es gibt alle Anwendungen unter dieser Ressource der Befehl löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="7e81f-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="7e81f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e81f-115">PARAMETERS</span></span>

### <span data-ttu-id="7e81f-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="7e81f-116">-ClusterName</span></span>
<span data-ttu-id="7e81f-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="7e81f-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7e81f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e81f-118">-DefaultProfile</span></span>
<span data-ttu-id="7e81f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e81f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e81f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e81f-120">-Force</span></span>
<span data-ttu-id="7e81f-121">Ohne Eingabeaufforderung entfernen.</span><span class="sxs-lookup"><span data-stu-id="7e81f-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="7e81f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e81f-122">-InputObject</span></span>
<span data-ttu-id="7e81f-123">Die Version des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="7e81f-123">The application type version resource.</span></span>

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

### <span data-ttu-id="7e81f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7e81f-124">-Name</span></span>
<span data-ttu-id="7e81f-125">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="7e81f-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="7e81f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e81f-126">-PassThru</span></span>
<span data-ttu-id="7e81f-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="7e81f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7e81f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e81f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e81f-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7e81f-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7e81f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7e81f-130">-ResourceId</span></span>
<span data-ttu-id="7e81f-131">Arm-Ressourcen-Nr. des Anwendungstyps Version.</span><span class="sxs-lookup"><span data-stu-id="7e81f-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="7e81f-132">-Version</span><span class="sxs-lookup"><span data-stu-id="7e81f-132">-Version</span></span>
<span data-ttu-id="7e81f-133">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="7e81f-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="7e81f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e81f-134">-Confirm</span></span>
<span data-ttu-id="7e81f-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e81f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e81f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e81f-136">-WhatIf</span></span>
<span data-ttu-id="7e81f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e81f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e81f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e81f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e81f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e81f-139">CommonParameters</span></span>
<span data-ttu-id="7e81f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e81f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e81f-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e81f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e81f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e81f-142">INPUTS</span></span>

### <span data-ttu-id="7e81f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7e81f-143">System.String</span></span>

### <span data-ttu-id="7e81f-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e81f-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="7e81f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e81f-145">OUTPUTS</span></span>

### <span data-ttu-id="7e81f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e81f-146">System.Boolean</span></span>

## <span data-ttu-id="7e81f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e81f-147">NOTES</span></span>

## <span data-ttu-id="7e81f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e81f-148">RELATED LINKS</span></span>
