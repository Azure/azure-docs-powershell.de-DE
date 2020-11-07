---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a9a9c8705307b7c9ec3e71a9278c29637c4afc3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660705"
---
# <span data-ttu-id="dd7c4-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd7c4-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="dd7c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7c4-103">Ruft Routentabellen ab.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-103">Gets route tables.</span></span>

## <span data-ttu-id="dd7c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd7c4-104">SYNTAX</span></span>

### <span data-ttu-id="dd7c4-105">NOEXPAND (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd7c4-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd7c4-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="dd7c4-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd7c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd7c4-107">DESCRIPTION</span></span>
<span data-ttu-id="dd7c4-108">Das Cmdlet " **Get-AzRouteTable** " ruft Azure Route-Tabellen ab.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="dd7c4-109">Sie können eine einzelne Routentabelle abrufen oder alle Arbeitsplan Tabellen in einer Ressourcengruppe oder in Ihrem Abonnement abrufen.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="dd7c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd7c4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd7c4-111">Beispiel 1: Abrufen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="dd7c4-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="dd7c4-112">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="dd7c4-113">Beispiel 2: Auflisten von Routentabellen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="dd7c4-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="dd7c4-114">Dieser Befehl ruft alle Arbeitsplan Tabellen ab, deren Name mit "Routingtabelle" beginnt.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="dd7c4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd7c4-115">PARAMETERS</span></span>

### <span data-ttu-id="dd7c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7c4-116">-DefaultProfile</span></span>
<span data-ttu-id="dd7c4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd7c4-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dd7c4-118">-ExpandResource</span></span>
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

### <span data-ttu-id="dd7c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dd7c4-119">-Name</span></span>
<span data-ttu-id="dd7c4-120">Gibt den Namen der Arbeitsplan Tabelle an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd7c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd7c4-122">Gibt den Namen der Ressourcengruppe an, die die Arbeitsplan Tabellen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd7c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7c4-123">CommonParameters</span></span>
<span data-ttu-id="dd7c4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7c4-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd7c4-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7c4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd7c4-126">INPUTS</span></span>

### <span data-ttu-id="dd7c4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dd7c4-127">System.String</span></span>

## <span data-ttu-id="dd7c4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd7c4-128">OUTPUTS</span></span>

### <span data-ttu-id="dd7c4-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd7c4-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="dd7c4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd7c4-130">NOTES</span></span>

## <span data-ttu-id="dd7c4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd7c4-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd7c4-132">Neu – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd7c4-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="dd7c4-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd7c4-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="dd7c4-134">Satz-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd7c4-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


