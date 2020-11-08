---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177740"
---
# <span data-ttu-id="67f4d-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="67f4d-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="67f4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="67f4d-103">Ruft eine Liste der Sicherheits Topologien für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="67f4d-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="67f4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67f4d-104">SYNTAX</span></span>

### <span data-ttu-id="67f4d-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="67f4d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f4d-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="67f4d-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f4d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f4d-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f4d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67f4d-108">DESCRIPTION</span></span>
<span data-ttu-id="67f4d-109">Sicherheits Topologien werden vom Azure Security Center automatisch erkannt, mithilfe dieses Cmdlets können Sie Sicherheits Topologien anzeigen.</span><span class="sxs-lookup"><span data-stu-id="67f4d-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="67f4d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67f4d-110">EXAMPLES</span></span>

### <span data-ttu-id="67f4d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67f4d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="67f4d-112">Anzeigen aller Sicherheits Topologien in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="67f4d-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="67f4d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="67f4d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="67f4d-114">Abrufen spezifischer Sicherheits Topologien</span><span class="sxs-lookup"><span data-stu-id="67f4d-114">Get a specific security topologies</span></span>

## <span data-ttu-id="67f4d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="67f4d-115">PARAMETERS</span></span>

### <span data-ttu-id="67f4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f4d-116">-DefaultProfile</span></span>
<span data-ttu-id="67f4d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67f4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f4d-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="67f4d-118">-Location</span></span>
<span data-ttu-id="67f4d-119">Lage.</span><span class="sxs-lookup"><span data-stu-id="67f4d-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f4d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67f4d-120">-Name</span></span>
<span data-ttu-id="67f4d-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="67f4d-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="67f4d-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67f4d-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f4d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67f4d-124">-ResourceId</span></span>
<span data-ttu-id="67f4d-125">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="67f4d-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f4d-126">CommonParameters</span></span>
<span data-ttu-id="67f4d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f4d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f4d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f4d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67f4d-129">INPUTS</span></span>

### <span data-ttu-id="67f4d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67f4d-130">System.String</span></span>

## <span data-ttu-id="67f4d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67f4d-131">OUTPUTS</span></span>

### <span data-ttu-id="67f4d-132">Microsoft. Azure. Commands. Security. Models. Topology. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="67f4d-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="67f4d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="67f4d-133">NOTES</span></span>

## <span data-ttu-id="67f4d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67f4d-134">RELATED LINKS</span></span>
