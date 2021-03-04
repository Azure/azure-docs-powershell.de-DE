---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938448"
---
# <span data-ttu-id="01b10-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="01b10-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="01b10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b10-102">SYNOPSIS</span></span>
<span data-ttu-id="01b10-103">Ruft eine Liste der Sicherheitstopologien für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="01b10-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="01b10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01b10-104">SYNTAX</span></span>

### <span data-ttu-id="01b10-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="01b10-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b10-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="01b10-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b10-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b10-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01b10-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01b10-108">DESCRIPTION</span></span>
<span data-ttu-id="01b10-109">Sicherheitstopologien werden automatisch vom Azure Security Center erkannt. Verwenden Sie dieses Cmdlet zum Anzeigen von Sicherheitstopologien.</span><span class="sxs-lookup"><span data-stu-id="01b10-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="01b10-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01b10-110">EXAMPLES</span></span>

### <span data-ttu-id="01b10-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01b10-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="01b10-112">Anzeigen aller Sicherheitstopologien in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="01b10-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="01b10-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01b10-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="01b10-114">Erhalten einer bestimmten Sicherheitstopologie</span><span class="sxs-lookup"><span data-stu-id="01b10-114">Get a specific security topologies</span></span>

## <span data-ttu-id="01b10-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01b10-115">PARAMETERS</span></span>

### <span data-ttu-id="01b10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b10-116">-DefaultProfile</span></span>
<span data-ttu-id="01b10-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01b10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b10-118">-Location</span><span class="sxs-lookup"><span data-stu-id="01b10-118">-Location</span></span>
<span data-ttu-id="01b10-119">Ort.</span><span class="sxs-lookup"><span data-stu-id="01b10-119">Location.</span></span>

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

### <span data-ttu-id="01b10-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01b10-120">-Name</span></span>
<span data-ttu-id="01b10-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="01b10-121">Resource name.</span></span>

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

### <span data-ttu-id="01b10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b10-122">-ResourceGroupName</span></span>
<span data-ttu-id="01b10-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01b10-123">Resource group name.</span></span>

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

### <span data-ttu-id="01b10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b10-124">-ResourceId</span></span>
<span data-ttu-id="01b10-125">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="01b10-125">Resource ID.</span></span>

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

### <span data-ttu-id="01b10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b10-126">CommonParameters</span></span>
<span data-ttu-id="01b10-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b10-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01b10-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b10-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01b10-129">INPUTS</span></span>

### <span data-ttu-id="01b10-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01b10-130">System.String</span></span>

## <span data-ttu-id="01b10-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01b10-131">OUTPUTS</span></span>

### <span data-ttu-id="01b10-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="01b10-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="01b10-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01b10-133">NOTES</span></span>

## <span data-ttu-id="01b10-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01b10-134">RELATED LINKS</span></span>
