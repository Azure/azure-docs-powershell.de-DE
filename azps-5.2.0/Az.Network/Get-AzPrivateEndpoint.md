---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364088"
---
# <span data-ttu-id="ff07a-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff07a-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ff07a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff07a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff07a-103">Erhalten eines privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="ff07a-103">Get a private endpoint</span></span>

## <span data-ttu-id="ff07a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff07a-104">SYNTAX</span></span>

### <span data-ttu-id="ff07a-105">NoExpand (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff07a-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff07a-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="ff07a-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff07a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff07a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff07a-108">Das **Get-AzPrivateEndpoint-Cmdlet** ruft einen oder mehrere private Endpunkte ab.</span><span class="sxs-lookup"><span data-stu-id="ff07a-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="ff07a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff07a-109">EXAMPLES</span></span>

### <span data-ttu-id="ff07a-110">Beispiel 1: Abrufen eines privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="ff07a-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="ff07a-111">Dieser Befehl ruft den privaten Endpunkt "MyPrivateEndpoint1" in der Ressourcengruppe "TestResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="ff07a-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="ff07a-112">Beispiel 2: Auflisten aller privaten Endpunkte in "ResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="ff07a-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="ff07a-113">Dieser Befehl ruft alle privaten Endpunkte in der Ressourcengruppe "TestResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="ff07a-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ff07a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff07a-114">PARAMETERS</span></span>

### <span data-ttu-id="ff07a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff07a-115">-DefaultProfile</span></span>
<span data-ttu-id="ff07a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff07a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff07a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ff07a-117">-ExpandResource</span></span>
<span data-ttu-id="ff07a-118">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff07a-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ff07a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ff07a-119">-Name</span></span>
<span data-ttu-id="ff07a-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ff07a-120">The resource name.</span></span>

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

### <span data-ttu-id="ff07a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff07a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff07a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ff07a-122">The resource group name.</span></span>

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

### <span data-ttu-id="ff07a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff07a-123">CommonParameters</span></span>
<span data-ttu-id="ff07a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff07a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff07a-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff07a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff07a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff07a-126">INPUTS</span></span>

### <span data-ttu-id="ff07a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ff07a-127">System.String</span></span>

## <span data-ttu-id="ff07a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff07a-128">OUTPUTS</span></span>

### <span data-ttu-id="ff07a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff07a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ff07a-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ff07a-130">NOTES</span></span>

## <span data-ttu-id="ff07a-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ff07a-131">RELATED LINKS</span></span>

[<span data-ttu-id="ff07a-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff07a-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="ff07a-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff07a-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)