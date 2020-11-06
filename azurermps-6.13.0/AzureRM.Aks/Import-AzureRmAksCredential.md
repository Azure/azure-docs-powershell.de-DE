---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: b65ac736be5ee5f2f0592bcb2fdc84c873361f9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500317"
---
# <span data-ttu-id="7ceb0-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="7ceb0-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="7ceb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ceb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ceb0-103">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="7ceb0-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ceb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ceb0-104">SYNTAX</span></span>

### <span data-ttu-id="7ceb0-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ceb0-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ceb0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ceb0-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ceb0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ceb0-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ceb0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ceb0-108">DESCRIPTION</span></span>
<span data-ttu-id="7ceb0-109">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="7ceb0-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="7ceb0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ceb0-110">EXAMPLES</span></span>

### <span data-ttu-id="7ceb0-111">Importieren und Zusammenführen der Kubectl-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7ceb0-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="7ceb0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ceb0-112">PARAMETERS</span></span>

### <span data-ttu-id="7ceb0-113">– Administrator</span><span class="sxs-lookup"><span data-stu-id="7ceb0-113">-Admin</span></span>
<span data-ttu-id="7ceb0-114">Rufen Sie die "clusterAdmin' kubectl config" anstelle des standardmäßigen "clusterUser" ab.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="7ceb0-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="7ceb0-115">-ConfigPath</span></span>
<span data-ttu-id="7ceb0-116">Eine kubectl-Konfigurationsdatei zum Erstellen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="7ceb0-117">Verwenden Sie "-", um stattdessen YAML auf stdout zu drucken.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="7ceb0-118">Standard:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ceb0-119">-DefaultProfile</span></span>
<span data-ttu-id="7ceb0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7ceb0-121">-Force</span></span>
<span data-ttu-id="7ceb0-122">Importieren der Kubernetes-Konfiguration, auch wenn dies die Standardeinstellung ist</span><span class="sxs-lookup"><span data-stu-id="7ceb0-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="7ceb0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="7ceb0-123">-Id</span></span>
<span data-ttu-id="7ceb0-124">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="7ceb0-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ceb0-125">-InputObject</span></span>
<span data-ttu-id="7ceb0-126">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7ceb0-127">-Name</span></span>
<span data-ttu-id="7ceb0-128">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="7ceb0-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ceb0-129">-PassThru</span></span>
<span data-ttu-id="7ceb0-130">Gibt "true" zurück, wenn der Import erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="7ceb0-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="7ceb0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ceb0-131">-ResourceGroupName</span></span>
<span data-ttu-id="7ceb0-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7ceb0-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ceb0-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ceb0-133">-Confirm</span></span>
<span data-ttu-id="7ceb0-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ceb0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ceb0-135">-WhatIf</span></span>
<span data-ttu-id="7ceb0-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ceb0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ceb0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ceb0-138">CommonParameters</span></span>
<span data-ttu-id="7ceb0-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ceb0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ceb0-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ceb0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ceb0-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ceb0-141">INPUTS</span></span>

### <span data-ttu-id="7ceb0-142">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7ceb0-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="7ceb0-143">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ceb0-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7ceb0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7ceb0-144">System.String</span></span>

## <span data-ttu-id="7ceb0-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ceb0-145">OUTPUTS</span></span>

### <span data-ttu-id="7ceb0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7ceb0-146">System.String</span></span>

## <span data-ttu-id="7ceb0-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ceb0-147">NOTES</span></span>

## <span data-ttu-id="7ceb0-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ceb0-148">RELATED LINKS</span></span>
