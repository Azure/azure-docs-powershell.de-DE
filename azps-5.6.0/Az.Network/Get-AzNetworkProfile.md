---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: f2f18ac77f923247f2bef0e78802a2f05cf302d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919883"
---
# <span data-ttu-id="569f7-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="569f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="569f7-102">SYNOPSIS</span></span>
<span data-ttu-id="569f7-103">Ruft eine vorhandene Netzwerkprofilressource der obersten Ebene ab</span><span class="sxs-lookup"><span data-stu-id="569f7-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="569f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="569f7-104">SYNTAX</span></span>

### <span data-ttu-id="569f7-105">GetByResourceNameNoExpandParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="569f7-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="569f7-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="569f7-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="569f7-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="569f7-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="569f7-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="569f7-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="569f7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="569f7-109">DESCRIPTION</span></span>
<span data-ttu-id="569f7-110">Das **Get-AzNetworkProfile-Cmdlet** ruft eine vorhandene Netzwerkprofilressource der obersten Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="569f7-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="569f7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="569f7-111">EXAMPLES</span></span>

### <span data-ttu-id="569f7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="569f7-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="569f7-113">Dadurch wird das Netzwerkprofil np1 in der Ressourcengruppe rg1 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="569f7-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="569f7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="569f7-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="569f7-115">Dadurch werden die Netzwerkprofile abgerufen, die mit "np" beginnen.</span><span class="sxs-lookup"><span data-stu-id="569f7-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="569f7-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="569f7-116">PARAMETERS</span></span>

### <span data-ttu-id="569f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-117">-DefaultProfile</span></span>
<span data-ttu-id="569f7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="569f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569f7-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="569f7-119">-ExpandResource</span></span>
<span data-ttu-id="569f7-120">Der Ressourcenbezug, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="569f7-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569f7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="569f7-121">-Name</span></span>
<span data-ttu-id="569f7-122">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="569f7-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="569f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="569f7-124">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="569f7-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="569f7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="569f7-125">-ResourceId</span></span>
<span data-ttu-id="569f7-126">Die Azure-Ressourcen-Manager-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="569f7-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569f7-127">CommonParameters</span></span>
<span data-ttu-id="569f7-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569f7-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="569f7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569f7-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="569f7-130">INPUTS</span></span>

### <span data-ttu-id="569f7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="569f7-131">System.String</span></span>

## <span data-ttu-id="569f7-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="569f7-132">OUTPUTS</span></span>

### <span data-ttu-id="569f7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="569f7-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="569f7-134">NOTES</span></span>

## <span data-ttu-id="569f7-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="569f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="569f7-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="569f7-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="569f7-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="569f7-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
