---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 711d9848188cbdbaaeac9313680fd9fd70cb1f34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479714"
---
# <span data-ttu-id="da69a-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="da69a-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="da69a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da69a-102">SYNOPSIS</span></span>
<span data-ttu-id="da69a-103">Ruft Routentabellen ab.</span><span class="sxs-lookup"><span data-stu-id="da69a-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da69a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da69a-104">SYNTAX</span></span>

### <span data-ttu-id="da69a-105">Erweitern</span><span class="sxs-lookup"><span data-stu-id="da69a-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da69a-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="da69a-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da69a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da69a-107">DESCRIPTION</span></span>
<span data-ttu-id="da69a-108">Das Cmdlet " **Get-AzureRmRouteTable** " ruft Azure Route-Tabellen ab.</span><span class="sxs-lookup"><span data-stu-id="da69a-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="da69a-109">Sie können eine einzelne Routentabelle abrufen oder alle Arbeitsplan Tabellen in einer Ressourcengruppe oder in Ihrem Abonnement abrufen.</span><span class="sxs-lookup"><span data-stu-id="da69a-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="da69a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da69a-110">EXAMPLES</span></span>

### <span data-ttu-id="da69a-111">Beispiel 1: Abrufen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="da69a-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="da69a-112">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="da69a-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="da69a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="da69a-113">PARAMETERS</span></span>

### <span data-ttu-id="da69a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da69a-114">-DefaultProfile</span></span>
<span data-ttu-id="da69a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da69a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da69a-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="da69a-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da69a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da69a-117">-Name</span></span>
<span data-ttu-id="da69a-118">Gibt den Namen der Arbeitsplan Tabelle an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="da69a-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da69a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da69a-119">-ResourceGroupName</span></span>
<span data-ttu-id="da69a-120">Gibt den Namen der Ressourcengruppe an, die die Arbeitsplan Tabellen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="da69a-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da69a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da69a-121">CommonParameters</span></span>
<span data-ttu-id="da69a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da69a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da69a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da69a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da69a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da69a-124">INPUTS</span></span>

### <span data-ttu-id="da69a-125">Keine</span><span class="sxs-lookup"><span data-stu-id="da69a-125">None</span></span>
<span data-ttu-id="da69a-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="da69a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da69a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da69a-127">OUTPUTS</span></span>

### <span data-ttu-id="da69a-128">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="da69a-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="da69a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="da69a-129">NOTES</span></span>

## <span data-ttu-id="da69a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da69a-130">RELATED LINKS</span></span>

[<span data-ttu-id="da69a-131">Neu – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="da69a-131">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="da69a-132">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="da69a-132">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="da69a-133">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="da69a-133">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


