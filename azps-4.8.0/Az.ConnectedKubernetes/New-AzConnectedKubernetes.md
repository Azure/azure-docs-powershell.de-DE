---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009983"
---
# <span data-ttu-id="0d817-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="0d817-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="0d817-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d817-102">SYNOPSIS</span></span>
<span data-ttu-id="0d817-103">API zum Registrieren eines neuen K8s-Clusters und damit zum Erstellen einer nachverfolgten Ressource in Arm</span><span class="sxs-lookup"><span data-stu-id="0d817-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="0d817-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d817-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d817-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d817-105">DESCRIPTION</span></span>
<span data-ttu-id="0d817-106">API zum Registrieren eines neuen K8s-Clusters und damit zum Erstellen einer nachverfolgten Ressource in Arm</span><span class="sxs-lookup"><span data-stu-id="0d817-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="0d817-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d817-107">EXAMPLES</span></span>

### <span data-ttu-id="0d817-108">Beispiel 1: Erstellen eines verbundenen kubernetes</span><span class="sxs-lookup"><span data-stu-id="0d817-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="0d817-109">Dieser Befehl erstellt eine verbundene kubernetes.</span><span class="sxs-lookup"><span data-stu-id="0d817-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="0d817-110">Beispiel 1: Erstellen einer verbundenen kubernetes mit Parametern kubeConfig und kubencontext</span><span class="sxs-lookup"><span data-stu-id="0d817-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="0d817-111">Dieser Befehl erstellt eine verbundene kubernetes mit Parametern kubeConfig und kubencontext.</span><span class="sxs-lookup"><span data-stu-id="0d817-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="0d817-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d817-112">PARAMETERS</span></span>

### <span data-ttu-id="0d817-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0d817-113">-ClusterName</span></span>
<span data-ttu-id="0d817-114">Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0d817-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d817-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d817-115">-DefaultProfile</span></span>
<span data-ttu-id="0d817-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d817-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d817-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="0d817-117">-KubeConfig</span></span>
<span data-ttu-id="0d817-118">Pfad zur Datei "Kuben-Konfiguration"</span><span class="sxs-lookup"><span data-stu-id="0d817-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="0d817-119">-Kubencontext</span><span class="sxs-lookup"><span data-stu-id="0d817-119">-KubeContext</span></span>
<span data-ttu-id="0d817-120">Kubconfig-Kontext vom aktuellen Computer</span><span class="sxs-lookup"><span data-stu-id="0d817-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="0d817-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="0d817-121">-Location</span></span>
<span data-ttu-id="0d817-122">Speicherort des Clusters</span><span class="sxs-lookup"><span data-stu-id="0d817-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d817-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d817-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d817-124">Der Name der Ressourcengruppe, in der der kubernetes-Cluster registriert ist.</span><span class="sxs-lookup"><span data-stu-id="0d817-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d817-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0d817-125">-SubscriptionId</span></span>
<span data-ttu-id="0d817-126">Die ID des Abonnements, für das der kubernetes-Cluster registriert ist.</span><span class="sxs-lookup"><span data-stu-id="0d817-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d817-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d817-127">-Confirm</span></span>
<span data-ttu-id="0d817-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d817-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d817-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d817-129">-WhatIf</span></span>
<span data-ttu-id="0d817-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d817-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d817-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d817-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d817-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d817-132">CommonParameters</span></span>
<span data-ttu-id="0d817-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d817-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d817-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d817-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d817-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d817-135">INPUTS</span></span>

## <span data-ttu-id="0d817-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d817-136">OUTPUTS</span></span>

### <span data-ttu-id="0d817-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="0d817-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="0d817-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d817-138">NOTES</span></span>

<span data-ttu-id="0d817-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="0d817-139">ALIASES</span></span>

## <span data-ttu-id="0d817-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d817-140">RELATED LINKS</span></span>

