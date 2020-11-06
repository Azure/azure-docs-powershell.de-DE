---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 8095e2ebd1d9e55e8f5bc847f4a72277363e197a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503546"
---
# <span data-ttu-id="c8815-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8815-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="c8815-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8815-102">SYNOPSIS</span></span>
<span data-ttu-id="c8815-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="c8815-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8815-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8815-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8815-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8815-105">DESCRIPTION</span></span>
<span data-ttu-id="c8815-106">Das Cmdlet " **Get-AzureRmEffectiveRouteTable** " gibt die effektive Routingtabelle zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8815-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="c8815-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8815-107">EXAMPLES</span></span>

### <span data-ttu-id="c8815-108">Beispiel 1: Abrufen der Tabelle "effektive Route" auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8815-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c8815-109">Dieser Befehl ruft die effektive Routingtabelle ab, die der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe "myresourcegroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c8815-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="c8815-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8815-110">PARAMETERS</span></span>

### <span data-ttu-id="c8815-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8815-111">-AsJob</span></span>
<span data-ttu-id="c8815-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8815-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8815-113">-DefaultProfile</span></span>
<span data-ttu-id="c8815-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8815-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8815-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c8815-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="c8815-116">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8815-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="c8815-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8815-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8815-118">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="c8815-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="c8815-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8815-119">CommonParameters</span></span>
<span data-ttu-id="c8815-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8815-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8815-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8815-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8815-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8815-122">INPUTS</span></span>

### <span data-ttu-id="c8815-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c8815-123">System.String</span></span>

## <span data-ttu-id="c8815-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8815-124">OUTPUTS</span></span>

### <span data-ttu-id="c8815-125">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="c8815-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="c8815-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8815-126">NOTES</span></span>

## <span data-ttu-id="c8815-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8815-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8815-128">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c8815-128">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


