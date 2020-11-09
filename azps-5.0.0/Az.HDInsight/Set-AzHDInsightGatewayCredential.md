---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296302"
---
# <span data-ttu-id="516f6-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="516f6-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="516f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="516f6-102">SYNOPSIS</span></span>
<span data-ttu-id="516f6-103">Legt die Gateway-http-Anmeldeinformationen eines Azure HDInsight-Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="516f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="516f6-104">SYNTAX</span></span>

### <span data-ttu-id="516f6-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="516f6-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="516f6-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="516f6-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="516f6-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="516f6-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="516f6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="516f6-108">DESCRIPTION</span></span>
<span data-ttu-id="516f6-109">Das Cmdlet " **Set-AzHDInsightGatewayCredential** " legt Gateway-Anmeldeinformationen eines Azure HDInsight-Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="516f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="516f6-110">EXAMPLES</span></span>

### <span data-ttu-id="516f6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="516f6-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="516f6-112">Mit diesem Befehl werden die Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" nach Name-Parametersatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="516f6-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="516f6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="516f6-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="516f6-114">Mit diesem Befehl werden die Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" mithilfe des Parameters "resourcecode" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="516f6-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="516f6-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="516f6-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="516f6-116">Mit diesem Befehl werden Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" nach Inputobject-Parametersatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="516f6-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="516f6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="516f6-117">PARAMETERS</span></span>

### <span data-ttu-id="516f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="516f6-118">-AsJob</span></span>
<span data-ttu-id="516f6-119">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="516f6-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="516f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516f6-120">-DefaultProfile</span></span>
<span data-ttu-id="516f6-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="516f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516f6-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="516f6-122">-HttpCredential</span></span>
<span data-ttu-id="516f6-123">Ruft die Anmeldung für den Benutzer des Clusters ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="516f6-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="516f6-124">-InputObject</span></span>
<span data-ttu-id="516f6-125">Ruft das Eingabeobjekt ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="516f6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="516f6-126">-Name</span></span>
<span data-ttu-id="516f6-127">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-127">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="516f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="516f6-129">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="516f6-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="516f6-130">-ResourceId</span></span>
<span data-ttu-id="516f6-131">Ruft die Ressourcen-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="516f6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="516f6-132">-Confirm</span></span>
<span data-ttu-id="516f6-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="516f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="516f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="516f6-134">-WhatIf</span></span>
<span data-ttu-id="516f6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="516f6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="516f6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="516f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="516f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516f6-137">CommonParameters</span></span>
<span data-ttu-id="516f6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516f6-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="516f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516f6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="516f6-140">INPUTS</span></span>

### <span data-ttu-id="516f6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="516f6-141">None</span></span>

## <span data-ttu-id="516f6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="516f6-142">OUTPUTS</span></span>

### <span data-ttu-id="516f6-143">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="516f6-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="516f6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="516f6-144">NOTES</span></span>

## <span data-ttu-id="516f6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="516f6-145">RELATED LINKS</span></span>
