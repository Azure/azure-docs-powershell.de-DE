---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 616695e60d945e545cfbb8c1b2fb7ba81ae9caa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157633"
---
# <span data-ttu-id="06604-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="06604-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="06604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06604-102">SYNOPSIS</span></span>
<span data-ttu-id="06604-103">Deaktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="06604-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="06604-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06604-104">SYNTAX</span></span>

### <span data-ttu-id="06604-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="06604-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06604-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06604-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06604-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06604-107">DESCRIPTION</span></span>
<span data-ttu-id="06604-108">Deaktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="06604-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="06604-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06604-109">EXAMPLES</span></span>

### <span data-ttu-id="06604-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06604-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="06604-111">Deaktivieren Sie die `HttpApplicationRouting` Add-Ons `Monitoring` , und `AzurePolicy` für `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="06604-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="06604-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06604-112">PARAMETERS</span></span>

### <span data-ttu-id="06604-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="06604-113">-ClusterName</span></span>
<span data-ttu-id="06604-114">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="06604-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="06604-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="06604-115">-ClusterObject</span></span>
<span data-ttu-id="06604-116">Ein PSAkiernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="06604-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="06604-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06604-117">-DefaultProfile</span></span>
<span data-ttu-id="06604-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06604-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06604-119">-Name</span><span class="sxs-lookup"><span data-stu-id="06604-119">-Name</span></span>
<span data-ttu-id="06604-120">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="06604-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="06604-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06604-121">-ResourceGroupName</span></span>
<span data-ttu-id="06604-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="06604-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="06604-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06604-123">-Confirm</span></span>
<span data-ttu-id="06604-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06604-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06604-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="06604-125">-WhatIf</span></span>
<span data-ttu-id="06604-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06604-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06604-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06604-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06604-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06604-128">CommonParameters</span></span>
<span data-ttu-id="06604-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06604-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06604-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06604-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06604-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06604-131">INPUTS</span></span>

### <span data-ttu-id="06604-132">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="06604-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="06604-133">System.String</span><span class="sxs-lookup"><span data-stu-id="06604-133">System.String</span></span>

## <span data-ttu-id="06604-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06604-134">OUTPUTS</span></span>

### <span data-ttu-id="06604-135">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="06604-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="06604-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06604-136">NOTES</span></span>

## <span data-ttu-id="06604-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06604-137">RELATED LINKS</span></span>
