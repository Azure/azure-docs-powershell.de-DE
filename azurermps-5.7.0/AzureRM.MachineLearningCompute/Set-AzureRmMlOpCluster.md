---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664907"
---
# <span data-ttu-id="5037a-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5037a-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="5037a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5037a-102">SYNOPSIS</span></span>
<span data-ttu-id="5037a-103">Legt die Eigenschaften eines Vorgangs Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="5037a-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5037a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5037a-104">SYNTAX</span></span>

### <span data-ttu-id="5037a-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5037a-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5037a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5037a-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5037a-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="5037a-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5037a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5037a-108">DESCRIPTION</span></span>
<span data-ttu-id="5037a-109">Legt alle Eigenschaften eines Vorgangs Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="5037a-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="5037a-110">Da bei Verwendung eines Clusterobjekts alle Eigenschaften festgelegt werden, muss ein vollständig gültiges Eingabeobjekt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5037a-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="5037a-111">Schreibgeschützte Eigenschaften werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5037a-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="5037a-112">Nur einige Eigenschaften sind derzeit aktualisierbar, wie in den Parametersätzen zu sehen ist.</span><span class="sxs-lookup"><span data-stu-id="5037a-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="5037a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5037a-113">EXAMPLES</span></span>

### <span data-ttu-id="5037a-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5037a-114">Example 1</span></span>
<span data-ttu-id="5037a-115">Aktualisieren eines Clusters mit einzelnen Parametern</span><span class="sxs-lookup"><span data-stu-id="5037a-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="5037a-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5037a-116">Example 2</span></span>
<span data-ttu-id="5037a-117">Aktualisieren eines Clusters mit einem Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5037a-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="5037a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5037a-118">PARAMETERS</span></span>

### <span data-ttu-id="5037a-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="5037a-119">-AgentCount</span></span>
<span data-ttu-id="5037a-120">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="5037a-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5037a-121">-DefaultProfile</span></span>
<span data-ttu-id="5037a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5037a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5037a-123">-InputObject</span></span>
<span data-ttu-id="5037a-124">Die Clustereigenschaften für die Operation.</span><span class="sxs-lookup"><span data-stu-id="5037a-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5037a-125">-Name</span></span>
<span data-ttu-id="5037a-126">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="5037a-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5037a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5037a-128">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="5037a-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5037a-129">-ResourceId</span></span>
<span data-ttu-id="5037a-130">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="5037a-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5037a-131">-SslCertificate</span></span>
<span data-ttu-id="5037a-132">Die SSL-Zertifikatsdaten im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="5037a-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="5037a-133">-SslCName</span></span>
<span data-ttu-id="5037a-134">Der CNAME für das SSL-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="5037a-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="5037a-135">-SslKey</span></span>
<span data-ttu-id="5037a-136">Die SSL-Schlüsseldaten im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="5037a-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="5037a-137">-SslStatus</span></span>
<span data-ttu-id="5037a-138">SSL-Status</span><span class="sxs-lookup"><span data-stu-id="5037a-138">SSL status.</span></span>
<span data-ttu-id="5037a-139">Mögliche Werte sind "aktiviert" und "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="5037a-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5037a-140">-Confirm</span></span>
<span data-ttu-id="5037a-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5037a-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5037a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5037a-142">-WhatIf</span></span>
<span data-ttu-id="5037a-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5037a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5037a-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5037a-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5037a-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5037a-145">INPUTS</span></span>

### <span data-ttu-id="5037a-146">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5037a-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="5037a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5037a-147">System.String</span></span>
### <span data-ttu-id="5037a-148">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5037a-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="5037a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5037a-149">OUTPUTS</span></span>

### <span data-ttu-id="5037a-150">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5037a-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="5037a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="5037a-151">NOTES</span></span>

## <span data-ttu-id="5037a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5037a-152">RELATED LINKS</span></span>

