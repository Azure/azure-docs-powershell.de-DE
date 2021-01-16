---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291983"
---
# <span data-ttu-id="a0372-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="a0372-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="a0372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0372-102">SYNOPSIS</span></span>
<span data-ttu-id="a0372-103">Legt die Gateway-HTTP-Anmeldeinformationen eines Azure -HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a0372-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0372-104">SYNTAX</span></span>

### <span data-ttu-id="a0372-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0372-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0372-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0372-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0372-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0372-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0372-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0372-108">DESCRIPTION</span></span>
<span data-ttu-id="a0372-109">Das **Cmdlet "Set-AzHDInsightGatewayCredential"** legt die Gatewayanmeldeinformationen eines Azure -HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a0372-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0372-110">EXAMPLES</span></span>

### <span data-ttu-id="a0372-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0372-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a0372-112">Mit diesem Befehl werden die Gatewayanmeldeinformationen des Clusters mit dem Namen "your-hadoop-001" nach dem Festgelegten Namensparameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0372-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="a0372-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0372-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a0372-114">Mit diesem Befehl werden die Gatewayanmeldeinformationen des Clusters mit dem Parameter "your-hadoop-001 by ResourceId" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0372-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="a0372-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a0372-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a0372-116">Mit diesem Befehl werden die Gatewayanmeldeinformationen des Clusters mit dem Namen "your-hadoop-001" von dem Parametersatz "InputObject" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0372-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="a0372-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0372-117">PARAMETERS</span></span>

### <span data-ttu-id="a0372-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0372-118">-AsJob</span></span>
<span data-ttu-id="a0372-119">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="a0372-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0372-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0372-120">-DefaultProfile</span></span>
<span data-ttu-id="a0372-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0372-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0372-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a0372-122">-HttpCredential</span></span>
<span data-ttu-id="a0372-123">Ruft die Anmeldung für den Benutzer des Clusters ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0372-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0372-124">-InputObject</span></span>
<span data-ttu-id="a0372-125">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0372-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a0372-126">-Name</span></span>
<span data-ttu-id="a0372-127">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0372-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0372-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0372-129">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0372-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0372-130">-ResourceId</span></span>
<span data-ttu-id="a0372-131">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="a0372-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0372-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0372-132">-Confirm</span></span>
<span data-ttu-id="a0372-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0372-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0372-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0372-134">-WhatIf</span></span>
<span data-ttu-id="a0372-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0372-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0372-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0372-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0372-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0372-137">CommonParameters</span></span>
<span data-ttu-id="a0372-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0372-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0372-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0372-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0372-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0372-140">INPUTS</span></span>

### <span data-ttu-id="a0372-141">Keine</span><span class="sxs-lookup"><span data-stu-id="a0372-141">None</span></span>

## <span data-ttu-id="a0372-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0372-142">OUTPUTS</span></span>

### <span data-ttu-id="a0372-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="a0372-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="a0372-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0372-144">NOTES</span></span>

## <span data-ttu-id="a0372-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0372-145">RELATED LINKS</span></span>
