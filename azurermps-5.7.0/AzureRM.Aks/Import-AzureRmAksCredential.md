---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: 9a95f6a6b299114c52e011c3a1abdc6fa8651c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477073"
---
# <span data-ttu-id="f24aa-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="f24aa-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="f24aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f24aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f24aa-103">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="f24aa-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f24aa-104">SYNTAX</span></span>

### <span data-ttu-id="f24aa-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f24aa-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f24aa-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f24aa-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f24aa-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f24aa-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f24aa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f24aa-108">DESCRIPTION</span></span>
<span data-ttu-id="f24aa-109">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="f24aa-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="f24aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f24aa-110">EXAMPLES</span></span>

### <span data-ttu-id="f24aa-111">Importieren und Zusammenführen der Kubectl-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f24aa-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f24aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f24aa-112">PARAMETERS</span></span>

### <span data-ttu-id="f24aa-113">– Administrator</span><span class="sxs-lookup"><span data-stu-id="f24aa-113">-Admin</span></span>
<span data-ttu-id="f24aa-114">Rufen Sie die "clusterAdmin' kubectl config" anstelle des standardmäßigen "clusterUser" ab.</span><span class="sxs-lookup"><span data-stu-id="f24aa-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="f24aa-115">-ConfigPath</span></span>
<span data-ttu-id="f24aa-116">Eine kubectl-Konfigurationsdatei zum Erstellen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f24aa-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="f24aa-117">Verwenden Sie "-", um stattdessen YAML auf stdout zu drucken.</span><span class="sxs-lookup"><span data-stu-id="f24aa-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="f24aa-118">Standard:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="f24aa-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24aa-119">-DefaultProfile</span></span>
<span data-ttu-id="f24aa-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f24aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f24aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f24aa-121">-Force</span></span>
<span data-ttu-id="f24aa-122">Importieren der Kubernetes-Konfiguration, auch wenn dies die Standardeinstellung ist</span><span class="sxs-lookup"><span data-stu-id="f24aa-122">Import Kubernetes config even if it is the default</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f24aa-123">-Id</span></span>
<span data-ttu-id="f24aa-124">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="f24aa-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f24aa-125">-InputObject</span></span>
<span data-ttu-id="f24aa-126">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f24aa-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f24aa-127">-Name</span></span>
<span data-ttu-id="f24aa-128">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="f24aa-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f24aa-129">-PassThru</span></span>
<span data-ttu-id="f24aa-130">Gibt "true" zurück, wenn der Import erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="f24aa-130">Returns true if import is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f24aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="f24aa-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f24aa-132">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24aa-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f24aa-133">-Confirm</span></span>
<span data-ttu-id="f24aa-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f24aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24aa-135">-WhatIf</span></span>
<span data-ttu-id="f24aa-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f24aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24aa-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f24aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24aa-138">CommonParameters</span></span>
<span data-ttu-id="f24aa-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f24aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24aa-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f24aa-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24aa-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f24aa-141">INPUTS</span></span>

### <span data-ttu-id="f24aa-142">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f24aa-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="f24aa-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f24aa-143">System.String</span></span>

## <span data-ttu-id="f24aa-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f24aa-144">OUTPUTS</span></span>

### <span data-ttu-id="f24aa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f24aa-145">System.String</span></span>

## <span data-ttu-id="f24aa-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f24aa-146">NOTES</span></span>

## <span data-ttu-id="f24aa-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f24aa-147">RELATED LINKS</span></span>
