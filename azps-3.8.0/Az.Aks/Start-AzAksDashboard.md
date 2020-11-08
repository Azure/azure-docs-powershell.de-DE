---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995915"
---
# <span data-ttu-id="96f8d-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="96f8d-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="96f8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="96f8d-103">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="96f8d-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="96f8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96f8d-104">SYNTAX</span></span>

### <span data-ttu-id="96f8d-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="96f8d-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96f8d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f8d-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96f8d-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f8d-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96f8d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96f8d-108">DESCRIPTION</span></span>
<span data-ttu-id="96f8d-109">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="96f8d-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="96f8d-110">Der SSH-Tunnel wird in einem PowerShell-Auftrag mit dem Namen Kubectl-Tunnel eingerichtet und kann durch Ausführen gefunden werden `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="96f8d-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="96f8d-111">Der Tunnel sollte über [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="96f8d-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="96f8d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96f8d-112">EXAMPLES</span></span>

### <span data-ttu-id="96f8d-113">Starten eines SSH-Tunnels und Öffnen eines Browsers im Kubernetes-Dashboard</span><span class="sxs-lookup"><span data-stu-id="96f8d-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="96f8d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f8d-114">PARAMETERS</span></span>

### <span data-ttu-id="96f8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f8d-115">-DefaultProfile</span></span>
<span data-ttu-id="96f8d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96f8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f8d-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="96f8d-117">-DisableBrowser</span></span>
<span data-ttu-id="96f8d-118">Öffnen Sie keinen Browser, nachdem Sie den kubectl-Port weitergeleitet haben.</span><span class="sxs-lookup"><span data-stu-id="96f8d-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="96f8d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="96f8d-119">-Id</span></span>
<span data-ttu-id="96f8d-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="96f8d-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="96f8d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96f8d-121">-InputObject</span></span>
<span data-ttu-id="96f8d-122">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="96f8d-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f8d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="96f8d-123">-Name</span></span>
<span data-ttu-id="96f8d-124">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="96f8d-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="96f8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96f8d-125">-PassThru</span></span>
<span data-ttu-id="96f8d-126">Das Cmdlet gibt KubeTunnelJob zurück, wenn es übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="96f8d-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="96f8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="96f8d-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="96f8d-128">Resource group name</span></span>

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

### <span data-ttu-id="96f8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f8d-129">CommonParameters</span></span>
<span data-ttu-id="96f8d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f8d-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f8d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f8d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96f8d-132">INPUTS</span></span>

### <span data-ttu-id="96f8d-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="96f8d-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="96f8d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96f8d-134">System.String</span></span>

## <span data-ttu-id="96f8d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96f8d-135">OUTPUTS</span></span>

### <span data-ttu-id="96f8d-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="96f8d-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="96f8d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="96f8d-137">NOTES</span></span>

## <span data-ttu-id="96f8d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96f8d-138">RELATED LINKS</span></span>
