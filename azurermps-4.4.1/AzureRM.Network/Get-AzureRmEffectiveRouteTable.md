---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497822"
---
# <span data-ttu-id="0fbb1-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0fbb1-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="0fbb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbb1-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbb1-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbb1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbb1-106">Das Cmdlet " **Get-AzureRmEffectiveRouteTable** " gibt die effektive Routingtabelle zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="0fbb1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fbb1-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbb1-108">Beispiel 1: Abrufen der Tabelle "effektive Route" auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="0fbb1-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0fbb1-109">Dieser Befehl ruft die effektive Routingtabelle ab, die der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe "myresourcegroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="0fbb1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbb1-110">PARAMETERS</span></span>

### <span data-ttu-id="0fbb1-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0fbb1-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="0fbb1-112">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="0fbb1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbb1-113">-ResourceGroupName</span></span>
<span data-ttu-id="0fbb1-114">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-114">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fbb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbb1-115">-DefaultProfile</span></span>
<span data-ttu-id="0fbb1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbb1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbb1-117">CommonParameters</span></span>
<span data-ttu-id="0fbb1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbb1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbb1-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbb1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbb1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fbb1-120">INPUTS</span></span>

## <span data-ttu-id="0fbb1-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fbb1-121">OUTPUTS</span></span>

### <span data-ttu-id="0fbb1-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="0fbb1-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="0fbb1-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fbb1-123">NOTES</span></span>

## <span data-ttu-id="0fbb1-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fbb1-124">RELATED LINKS</span></span>

[<span data-ttu-id="0fbb1-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0fbb1-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


