---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663502"
---
# <span data-ttu-id="792a0-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="792a0-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="792a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="792a0-102">SYNOPSIS</span></span>
<span data-ttu-id="792a0-103">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="792a0-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="792a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="792a0-104">SYNTAX</span></span>

### <span data-ttu-id="792a0-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="792a0-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792a0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a0-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792a0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a0-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792a0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="792a0-108">DESCRIPTION</span></span>
<span data-ttu-id="792a0-109">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="792a0-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="792a0-110">Der SSH-Tunnel wird in einem PowerShell-Auftrag mit dem Namen Kubectl-Tunnel eingerichtet und kann durch Ausführen gefunden werden `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="792a0-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="792a0-111">Der Tunnel sollte über [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="792a0-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="792a0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="792a0-112">EXAMPLES</span></span>

### <span data-ttu-id="792a0-113">Starten eines SSH-Tunnels und Öffnen eines Browsers im Kubernetes-Dashboard</span><span class="sxs-lookup"><span data-stu-id="792a0-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="792a0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="792a0-114">PARAMETERS</span></span>

### <span data-ttu-id="792a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792a0-115">-DefaultProfile</span></span>
<span data-ttu-id="792a0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="792a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792a0-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="792a0-117">-DisableBrowser</span></span>
<span data-ttu-id="792a0-118">Öffnen Sie einen Browser nach establising des kubectl-Portierungs-Forwards nicht.</span><span class="sxs-lookup"><span data-stu-id="792a0-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="792a0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="792a0-119">-Id</span></span>
<span data-ttu-id="792a0-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="792a0-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="792a0-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="792a0-121">-InputObject</span></span>
<span data-ttu-id="792a0-122">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="792a0-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792a0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="792a0-123">-Name</span></span>
<span data-ttu-id="792a0-124">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="792a0-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="792a0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="792a0-125">-PassThru</span></span>
<span data-ttu-id="792a0-126">Das Cmdlet gibt KubeTunnelJob zurück, wenn es übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="792a0-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="792a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="792a0-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="792a0-128">Resource group name</span></span>

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

### <span data-ttu-id="792a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792a0-129">CommonParameters</span></span>
<span data-ttu-id="792a0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792a0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792a0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="792a0-132">INPUTS</span></span>

### <span data-ttu-id="792a0-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="792a0-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="792a0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="792a0-134">System.String</span></span>

## <span data-ttu-id="792a0-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="792a0-135">OUTPUTS</span></span>

### <span data-ttu-id="792a0-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="792a0-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="792a0-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="792a0-137">NOTES</span></span>

## <span data-ttu-id="792a0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="792a0-138">RELATED LINKS</span></span>
