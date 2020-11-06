---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502037"
---
# <span data-ttu-id="5cda6-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5cda6-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="5cda6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cda6-102">SYNOPSIS</span></span>
<span data-ttu-id="5cda6-103">Fügt eine Delegierung zu einem Subnetz hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cda6-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cda6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cda6-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cda6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cda6-105">DESCRIPTION</span></span>
<span data-ttu-id="5cda6-106">Mit dem Cmdlet **Add-AzureRmDelegation** wird eine Dienst Delegierung zu einem Azure-Subnetz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5cda6-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="5cda6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cda6-107">EXAMPLES</span></span>

### <span data-ttu-id="5cda6-108">1: Hinzufügen einer Delegierung</span><span class="sxs-lookup"><span data-stu-id="5cda6-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="5cda6-109">Der erste Befehl ruft das virtuelle Netzwerk ab, in dem sich das Subnetz befindet.</span><span class="sxs-lookup"><span data-stu-id="5cda6-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="5cda6-110">Der zweite Befehl isoliert das gewünschte Subnetz, das Sie delegieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5cda6-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="5cda6-111">Der dritte Befehl fügt dem Subnetz eine Delegierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cda6-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="5cda6-112">Dieses besondere Beispiel wäre hilfreich, wenn Sie SQL zum Erstellen von Schnittstellen Endpunkten in diesem Subnetz aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5cda6-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="5cda6-113">Mit dem letzten Befehl wird das aktualisierte Subnetz an den Server gesendet, um tatsächlich Ihr Subnetz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5cda6-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="5cda6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cda6-114">PARAMETERS</span></span>

### <span data-ttu-id="5cda6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cda6-115">-DefaultProfile</span></span>
<span data-ttu-id="5cda6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cda6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cda6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5cda6-117">-Name</span></span>
<span data-ttu-id="5cda6-118">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="5cda6-118">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cda6-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5cda6-119">-ServiceName</span></span>
<span data-ttu-id="5cda6-120">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="5cda6-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cda6-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5cda6-121">-Subnet</span></span>
<span data-ttu-id="5cda6-122">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="5cda6-122">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cda6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cda6-123">CommonParameters</span></span>
<span data-ttu-id="5cda6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cda6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5cda6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cda6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cda6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cda6-126">INPUTS</span></span>

### <span data-ttu-id="5cda6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5cda6-127">System.String</span></span>

### <span data-ttu-id="5cda6-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5cda6-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5cda6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cda6-129">OUTPUTS</span></span>

### <span data-ttu-id="5cda6-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5cda6-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5cda6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cda6-131">NOTES</span></span>

## <span data-ttu-id="5cda6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cda6-132">RELATED LINKS</span></span>
<span data-ttu-id="5cda6-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Satz-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5cda6-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
