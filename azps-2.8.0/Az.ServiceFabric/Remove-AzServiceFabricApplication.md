---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 1ad1e8220ed77a9206503adaf4f9924f95fe4f44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824703"
---
# <span data-ttu-id="8297b-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8297b-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="8297b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8297b-102">SYNOPSIS</span></span>
<span data-ttu-id="8297b-103">Entfernen einer Anwendung aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="8297b-103">Remove an application from the cluster.</span></span> <span data-ttu-id="8297b-104">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="8297b-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="8297b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8297b-105">SYNTAX</span></span>

### <span data-ttu-id="8297b-106">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="8297b-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8297b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8297b-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8297b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8297b-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8297b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8297b-109">DESCRIPTION</span></span>
<span data-ttu-id="8297b-110">Dieses Cmdlet entfernt eine Anwendungsform des Clusters.</span><span class="sxs-lookup"><span data-stu-id="8297b-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="8297b-111">Hierdurch werden alle Dienste, falls vorhanden, unter der Anwendungsressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="8297b-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="8297b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8297b-112">EXAMPLES</span></span>

### <span data-ttu-id="8297b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8297b-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="8297b-114">In diesem Beispiel wird die Anwendung "testApp" aus der Ressourcengruppe "testRG" und dem Cluster "testCluster" entfernt.</span><span class="sxs-lookup"><span data-stu-id="8297b-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="8297b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8297b-115">PARAMETERS</span></span>

### <span data-ttu-id="8297b-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8297b-116">-ClusterName</span></span>
<span data-ttu-id="8297b-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="8297b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8297b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8297b-118">-DefaultProfile</span></span>
<span data-ttu-id="8297b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8297b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8297b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8297b-120">-Force</span></span>
<span data-ttu-id="8297b-121">Ohne Eingabeaufforderung entfernen.</span><span class="sxs-lookup"><span data-stu-id="8297b-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="8297b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8297b-122">-InputObject</span></span>
<span data-ttu-id="8297b-123">Die Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="8297b-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8297b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8297b-124">-Name</span></span>
<span data-ttu-id="8297b-125">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="8297b-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8297b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8297b-126">-PassThru</span></span>
<span data-ttu-id="8297b-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="8297b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8297b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8297b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8297b-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8297b-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8297b-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8297b-130">-ResourceId</span></span>
<span data-ttu-id="8297b-131">Arm-Quell Code der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8297b-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="8297b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8297b-132">-Confirm</span></span>
<span data-ttu-id="8297b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8297b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8297b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8297b-134">-WhatIf</span></span>
<span data-ttu-id="8297b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8297b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8297b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8297b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8297b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8297b-137">CommonParameters</span></span>
<span data-ttu-id="8297b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8297b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8297b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8297b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8297b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8297b-140">INPUTS</span></span>

### <span data-ttu-id="8297b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8297b-141">System.String</span></span>

### <span data-ttu-id="8297b-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="8297b-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="8297b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8297b-143">OUTPUTS</span></span>

### <span data-ttu-id="8297b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8297b-144">System.Boolean</span></span>

## <span data-ttu-id="8297b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8297b-145">NOTES</span></span>

## <span data-ttu-id="8297b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8297b-146">RELATED LINKS</span></span>
