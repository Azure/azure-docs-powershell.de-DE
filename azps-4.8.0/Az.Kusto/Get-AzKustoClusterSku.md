---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010172"
---
# <span data-ttu-id="1f372-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="1f372-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="1f372-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f372-102">SYNOPSIS</span></span>
<span data-ttu-id="1f372-103">Listet die berechtigten SKUs für den Kusto-Ressourcenanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="1f372-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="1f372-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f372-104">SYNTAX</span></span>

### <span data-ttu-id="1f372-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f372-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f372-106">List1</span><span class="sxs-lookup"><span data-stu-id="1f372-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f372-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f372-107">DESCRIPTION</span></span>
<span data-ttu-id="1f372-108">Listet die berechtigten SKUs für den Kusto-Ressourcenanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="1f372-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="1f372-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f372-109">EXAMPLES</span></span>

### <span data-ttu-id="1f372-110">Beispiel 1: Listet die anrechenbaren SKUs auf</span><span class="sxs-lookup"><span data-stu-id="1f372-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="1f372-111">Der obige Befehl listet die anrechenbaren SKUs auf.</span><span class="sxs-lookup"><span data-stu-id="1f372-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="1f372-112">Beispiel 2: Listet geeignete SKUs für bestimmte Cluster auf</span><span class="sxs-lookup"><span data-stu-id="1f372-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="1f372-113">Der obige Befehl listet die berechtigten SKUs für bestimmte Cluster auf</span><span class="sxs-lookup"><span data-stu-id="1f372-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="1f372-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f372-114">PARAMETERS</span></span>

### <span data-ttu-id="1f372-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1f372-115">-ClusterName</span></span>
<span data-ttu-id="1f372-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="1f372-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f372-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f372-117">-DefaultProfile</span></span>
<span data-ttu-id="1f372-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f372-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f372-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f372-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f372-120">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="1f372-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f372-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1f372-121">-SubscriptionId</span></span>
<span data-ttu-id="1f372-122">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f372-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f372-123">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1f372-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f372-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f372-124">CommonParameters</span></span>
<span data-ttu-id="1f372-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f372-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f372-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f372-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f372-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f372-127">INPUTS</span></span>

## <span data-ttu-id="1f372-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f372-128">OUTPUTS</span></span>

### <span data-ttu-id="1f372-129">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="1f372-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="1f372-130">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="1f372-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="1f372-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f372-131">NOTES</span></span>

<span data-ttu-id="1f372-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="1f372-132">ALIASES</span></span>

## <span data-ttu-id="1f372-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f372-133">RELATED LINKS</span></span>

