---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848816"
---
# <span data-ttu-id="8a76e-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8a76e-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="8a76e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a76e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a76e-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="8a76e-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a76e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a76e-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a76e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a76e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a76e-106">Das Cmdlet " **Get-AzureRmEffectiveRouteTable** " gibt die effektive Routingtabelle zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a76e-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="8a76e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a76e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a76e-108">Beispiel 1: Abrufen der Tabelle "effektive Route" auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="8a76e-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8a76e-109">Dieser Befehl ruft die effektive Routingtabelle ab, die der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe "myresourcegroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8a76e-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8a76e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a76e-110">PARAMETERS</span></span>

### <span data-ttu-id="8a76e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a76e-111">-AsJob</span></span>
<span data-ttu-id="8a76e-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8a76e-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a76e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a76e-113">-DefaultProfile</span></span>
<span data-ttu-id="8a76e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a76e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a76e-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8a76e-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="8a76e-116">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a76e-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="8a76e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a76e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a76e-118">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="8a76e-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a76e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a76e-119">CommonParameters</span></span>
<span data-ttu-id="8a76e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a76e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a76e-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a76e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a76e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a76e-122">INPUTS</span></span>

## <span data-ttu-id="8a76e-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a76e-123">OUTPUTS</span></span>

### <span data-ttu-id="8a76e-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="8a76e-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="8a76e-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a76e-125">NOTES</span></span>

## <span data-ttu-id="8a76e-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a76e-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a76e-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8a76e-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


