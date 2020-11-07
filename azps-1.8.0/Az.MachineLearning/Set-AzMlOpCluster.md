---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819152"
---
# <span data-ttu-id="7d9a4-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7d9a4-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="7d9a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9a4-103">Legt die Eigenschaften eines Vorgangs Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="7d9a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d9a4-104">SYNTAX</span></span>

### <span data-ttu-id="7d9a4-105">SetByIndividualParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d9a4-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d9a4-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7d9a4-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d9a4-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d9a4-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d9a4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d9a4-108">DESCRIPTION</span></span>
<span data-ttu-id="7d9a4-109">Legt alle Eigenschaften eines Vorgangs Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="7d9a4-110">Da bei Verwendung eines Clusterobjekts alle Eigenschaften festgelegt werden, muss ein vollständig gültiges Eingabeobjekt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="7d9a4-111">Schreibgeschützte Eigenschaften werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="7d9a4-112">Nur einige Eigenschaften sind derzeit aktualisierbar, wie in den Parametersätzen zu sehen ist.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="7d9a4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d9a4-113">EXAMPLES</span></span>

### <span data-ttu-id="7d9a4-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d9a4-114">Example 1</span></span>
<span data-ttu-id="7d9a4-115">Aktualisieren eines Clusters mit einzelnen Parametern</span><span class="sxs-lookup"><span data-stu-id="7d9a4-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="7d9a4-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7d9a4-116">Example 2</span></span>
<span data-ttu-id="7d9a4-117">Aktualisieren eines Clusters mit einem Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="7d9a4-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="7d9a4-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d9a4-118">PARAMETERS</span></span>

### <span data-ttu-id="7d9a4-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="7d9a4-119">-AgentCount</span></span>
<span data-ttu-id="7d9a4-120">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9a4-121">-DefaultProfile</span></span>
<span data-ttu-id="7d9a4-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9a4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7d9a4-123">-InputObject</span></span>
<span data-ttu-id="7d9a4-124">Die Clustereigenschaften für die Operation.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7d9a4-125">-Name</span></span>
<span data-ttu-id="7d9a4-126">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d9a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d9a4-128">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7d9a4-129">-ResourceId</span></span>
<span data-ttu-id="7d9a4-130">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d9a4-131">-SslCertificate</span></span>
<span data-ttu-id="7d9a4-132">Die SSL-Zertifikatsdaten im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="7d9a4-133">-SslCName</span></span>
<span data-ttu-id="7d9a4-134">Der CNAME für das SSL-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="7d9a4-135">-SslKey</span></span>
<span data-ttu-id="7d9a4-136">Die SSL-Schlüsseldaten im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="7d9a4-137">-SslStatus</span></span>
<span data-ttu-id="7d9a4-138">SSL-Status</span><span class="sxs-lookup"><span data-stu-id="7d9a4-138">SSL status.</span></span>
<span data-ttu-id="7d9a4-139">Mögliche Werte sind "aktiviert" und "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="7d9a4-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9a4-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d9a4-140">-Confirm</span></span>
<span data-ttu-id="7d9a4-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d9a4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d9a4-142">-WhatIf</span></span>
<span data-ttu-id="7d9a4-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d9a4-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d9a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9a4-145">CommonParameters</span></span>
<span data-ttu-id="7d9a4-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9a4-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9a4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9a4-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d9a4-148">INPUTS</span></span>

### <span data-ttu-id="7d9a4-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7d9a4-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="7d9a4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7d9a4-150">System.String</span></span>

### <span data-ttu-id="7d9a4-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d9a4-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7d9a4-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d9a4-152">OUTPUTS</span></span>

### <span data-ttu-id="7d9a4-153">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7d9a4-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="7d9a4-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d9a4-154">NOTES</span></span>

## <span data-ttu-id="7d9a4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d9a4-155">RELATED LINKS</span></span>
