---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303892"
---
# <span data-ttu-id="eedc0-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="eedc0-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="eedc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eedc0-102">SYNOPSIS</span></span>
<span data-ttu-id="eedc0-103">Deaktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="eedc0-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="eedc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eedc0-104">SYNTAX</span></span>

### <span data-ttu-id="eedc0-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eedc0-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eedc0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eedc0-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eedc0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eedc0-107">DESCRIPTION</span></span>
<span data-ttu-id="eedc0-108">Deaktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="eedc0-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="eedc0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eedc0-109">EXAMPLES</span></span>

### <span data-ttu-id="eedc0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eedc0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="eedc0-111">Deaktivieren Sie die Addons `HttpApplicationRouting` ,, `Monitoring` `AzurePolicy` `VirtualNode` und `KubeDashboard` für AKS.</span><span class="sxs-lookup"><span data-stu-id="eedc0-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="eedc0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eedc0-112">PARAMETERS</span></span>

### <span data-ttu-id="eedc0-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="eedc0-113">-ClusterName</span></span>
<span data-ttu-id="eedc0-114">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="eedc0-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedc0-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="eedc0-115">-ClusterObject</span></span>
<span data-ttu-id="eedc0-116">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="eedc0-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="eedc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedc0-117">-DefaultProfile</span></span>
<span data-ttu-id="eedc0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eedc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eedc0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eedc0-119">-Name</span></span>
<span data-ttu-id="eedc0-120">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="eedc0-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedc0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eedc0-121">-ResourceGroupName</span></span>
<span data-ttu-id="eedc0-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eedc0-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedc0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eedc0-123">-Confirm</span></span>
<span data-ttu-id="eedc0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eedc0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eedc0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eedc0-125">-WhatIf</span></span>
<span data-ttu-id="eedc0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eedc0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eedc0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eedc0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eedc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedc0-128">CommonParameters</span></span>
<span data-ttu-id="eedc0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eedc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedc0-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eedc0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedc0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eedc0-131">INPUTS</span></span>

### <span data-ttu-id="eedc0-132">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="eedc0-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="eedc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eedc0-133">System.String</span></span>

## <span data-ttu-id="eedc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eedc0-134">OUTPUTS</span></span>

### <span data-ttu-id="eedc0-135">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="eedc0-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="eedc0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="eedc0-136">NOTES</span></span>

## <span data-ttu-id="eedc0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eedc0-137">RELATED LINKS</span></span>
