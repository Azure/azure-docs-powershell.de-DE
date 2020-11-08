---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: c915f2e95c8912a071fd949a6c231a1eff79b97b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175472"
---
# <span data-ttu-id="1786a-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="1786a-101">Add-AzDelegation</span></span>

## <span data-ttu-id="1786a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1786a-102">SYNOPSIS</span></span>
<span data-ttu-id="1786a-103">Fügt eine Delegierung zu einem Subnetz hinzu.</span><span class="sxs-lookup"><span data-stu-id="1786a-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="1786a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1786a-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1786a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1786a-105">DESCRIPTION</span></span>
<span data-ttu-id="1786a-106">Mit dem Cmdlet **Add-AzDelegation** wird eine Dienst Delegierung zu einem Azure-Subnetz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1786a-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="1786a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1786a-107">EXAMPLES</span></span>

### <span data-ttu-id="1786a-108">Beispiel 1: Hinzufügen einer Delegierung</span><span class="sxs-lookup"><span data-stu-id="1786a-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="1786a-109">Der erste Befehl ruft das virtuelle Netzwerk ab, in dem sich das Subnetz befindet.</span><span class="sxs-lookup"><span data-stu-id="1786a-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="1786a-110">Der zweite Befehl isoliert das gewünschte Subnetz, das Sie delegieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1786a-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="1786a-111">Der dritte Befehl fügt dem Subnetz eine Delegierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1786a-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="1786a-112">Dieses besondere Beispiel wäre hilfreich, wenn Sie SQL zum Erstellen von Schnittstellen Endpunkten in diesem Subnetz aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1786a-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="1786a-113">Mit dem letzten Befehl wird das aktualisierte Subnetz an den Server gesendet, um tatsächlich Ihr Subnetz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1786a-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="1786a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1786a-114">PARAMETERS</span></span>

### <span data-ttu-id="1786a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1786a-115">-DefaultProfile</span></span>
<span data-ttu-id="1786a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1786a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1786a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1786a-117">-Name</span></span>
<span data-ttu-id="1786a-118">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="1786a-118">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1786a-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1786a-119">-ServiceName</span></span>
<span data-ttu-id="1786a-120">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="1786a-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1786a-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="1786a-121">-Subnet</span></span>
<span data-ttu-id="1786a-122">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="1786a-122">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1786a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1786a-123">CommonParameters</span></span>
<span data-ttu-id="1786a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1786a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1786a-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1786a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1786a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1786a-126">INPUTS</span></span>

### <span data-ttu-id="1786a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1786a-127">System.String</span></span>

### <span data-ttu-id="1786a-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1786a-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="1786a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1786a-129">OUTPUTS</span></span>

### <span data-ttu-id="1786a-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1786a-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="1786a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1786a-131">NOTES</span></span>

## <span data-ttu-id="1786a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1786a-132">RELATED LINKS</span></span>

<span data-ttu-id="1786a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Satz-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="1786a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>