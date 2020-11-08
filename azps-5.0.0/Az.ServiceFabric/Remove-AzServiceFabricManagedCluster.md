---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176068"
---
# <span data-ttu-id="a75b9-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a75b9-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="a75b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a75b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a75b9-103">Clusterressource entfernen.</span><span class="sxs-lookup"><span data-stu-id="a75b9-103">Remove cluster resource.</span></span>

## <span data-ttu-id="a75b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a75b9-104">SYNTAX</span></span>

### <span data-ttu-id="a75b9-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="a75b9-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75b9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a75b9-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75b9-107">ById</span><span class="sxs-lookup"><span data-stu-id="a75b9-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a75b9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a75b9-108">DESCRIPTION</span></span>
<span data-ttu-id="a75b9-109">Cluster entfernen dadurch werden auch die Knotentypen unter dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="a75b9-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="a75b9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a75b9-110">EXAMPLES</span></span>

### <span data-ttu-id="a75b9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a75b9-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="a75b9-112">Cluster entfernen.</span><span class="sxs-lookup"><span data-stu-id="a75b9-112">Remove cluster.</span></span>

### <span data-ttu-id="a75b9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a75b9-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="a75b9-114">Entfernen Sie Cluster mit Piping.</span><span class="sxs-lookup"><span data-stu-id="a75b9-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="a75b9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a75b9-115">PARAMETERS</span></span>

### <span data-ttu-id="a75b9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a75b9-116">-AsJob</span></span>
<span data-ttu-id="a75b9-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="a75b9-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a75b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75b9-118">-DefaultProfile</span></span>
<span data-ttu-id="a75b9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a75b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a75b9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a75b9-120">-InputObject</span></span>
<span data-ttu-id="a75b9-121">Verwaltete Cluster Ressource</span><span class="sxs-lookup"><span data-stu-id="a75b9-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a75b9-122">-Name</span></span>
<span data-ttu-id="a75b9-123">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="a75b9-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a75b9-124">-PassThru</span></span>
<span data-ttu-id="a75b9-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a75b9-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a75b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a75b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="a75b9-127">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a75b9-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a75b9-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a75b9-128">-ResourceId</span></span>
<span data-ttu-id="a75b9-129">Verwaltete Cluster-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a75b9-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b9-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a75b9-130">-Confirm</span></span>
<span data-ttu-id="a75b9-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a75b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a75b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a75b9-132">-WhatIf</span></span>
<span data-ttu-id="a75b9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a75b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a75b9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a75b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a75b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75b9-135">CommonParameters</span></span>
<span data-ttu-id="a75b9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75b9-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a75b9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75b9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a75b9-138">INPUTS</span></span>

### <span data-ttu-id="a75b9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a75b9-139">System.String</span></span>

## <span data-ttu-id="a75b9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a75b9-140">OUTPUTS</span></span>

### <span data-ttu-id="a75b9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a75b9-141">System.Boolean</span></span>

## <span data-ttu-id="a75b9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a75b9-142">NOTES</span></span>

## <span data-ttu-id="a75b9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a75b9-143">RELATED LINKS</span></span>
