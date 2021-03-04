---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 09bd7f919b953c4df09293a75c2c893df4a01b96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919728"
---
# <span data-ttu-id="5e29d-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e29d-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="5e29d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e29d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e29d-103">Einen privaten Endpunkt erhalten</span><span class="sxs-lookup"><span data-stu-id="5e29d-103">Get a private endpoint</span></span>

## <span data-ttu-id="5e29d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e29d-104">SYNTAX</span></span>

### <span data-ttu-id="5e29d-105">NoExpand (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e29d-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e29d-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="5e29d-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e29d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e29d-107">DESCRIPTION</span></span>
<span data-ttu-id="5e29d-108">Das **Get-AzPrivateEndpoint-Cmdlet** ruft einen oder mehrere private Endpunkte ab.</span><span class="sxs-lookup"><span data-stu-id="5e29d-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="5e29d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e29d-109">EXAMPLES</span></span>

### <span data-ttu-id="5e29d-110">Beispiel 1: Abrufen eines privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="5e29d-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="5e29d-111">Dieser Befehl ruft den privaten Endpunkt "MyPrivateEndpoint1" in der Ressourcengruppe TestResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5e29d-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="5e29d-112">Beispiel 2: Auflisten aller privaten Endpunkte in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e29d-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="5e29d-113">Dieser Befehl ruft alle privaten Endpunkte in der Ressourcengruppe TestResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5e29d-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="5e29d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e29d-114">PARAMETERS</span></span>

### <span data-ttu-id="5e29d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e29d-115">-DefaultProfile</span></span>
<span data-ttu-id="5e29d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e29d-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5e29d-117">-ExpandResource</span></span>
<span data-ttu-id="5e29d-118">Der Ressourcenbezug, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e29d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5e29d-119">-Name</span></span>
<span data-ttu-id="5e29d-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5e29d-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e29d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e29d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e29d-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e29d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e29d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e29d-123">CommonParameters</span></span>
<span data-ttu-id="5e29d-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e29d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e29d-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e29d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e29d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e29d-126">INPUTS</span></span>

### <span data-ttu-id="5e29d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5e29d-127">System.String</span></span>

## <span data-ttu-id="5e29d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e29d-128">OUTPUTS</span></span>

### <span data-ttu-id="5e29d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e29d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5e29d-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e29d-130">NOTES</span></span>

## <span data-ttu-id="5e29d-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e29d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e29d-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e29d-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="5e29d-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e29d-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)