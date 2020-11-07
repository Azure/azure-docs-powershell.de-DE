---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841679"
---
# <span data-ttu-id="36b73-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b73-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="36b73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36b73-102">SYNOPSIS</span></span>
<span data-ttu-id="36b73-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="36b73-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="36b73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36b73-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b73-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36b73-105">DESCRIPTION</span></span>
<span data-ttu-id="36b73-106">Das Cmdlet " **Get-AzEffectiveRouteTable** " gibt die effektive Routingtabelle zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="36b73-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="36b73-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36b73-107">EXAMPLES</span></span>

### <span data-ttu-id="36b73-108">Beispiel 1: Abrufen der Tabelle "effektive Route" auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="36b73-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="36b73-109">Dieser Befehl ruft die effektive Routingtabelle ab, die der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe "myresourcegroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36b73-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="36b73-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36b73-110">PARAMETERS</span></span>

### <span data-ttu-id="36b73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36b73-111">-AsJob</span></span>
<span data-ttu-id="36b73-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="36b73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36b73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b73-113">-DefaultProfile</span></span>
<span data-ttu-id="36b73-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36b73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b73-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="36b73-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="36b73-116">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="36b73-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="36b73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b73-117">-ResourceGroupName</span></span>
<span data-ttu-id="36b73-118">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="36b73-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="36b73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b73-119">CommonParameters</span></span>
<span data-ttu-id="36b73-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b73-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b73-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b73-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36b73-122">INPUTS</span></span>

## <span data-ttu-id="36b73-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36b73-123">OUTPUTS</span></span>

### <span data-ttu-id="36b73-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="36b73-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="36b73-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="36b73-125">NOTES</span></span>

## <span data-ttu-id="36b73-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36b73-126">RELATED LINKS</span></span>

[<span data-ttu-id="36b73-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36b73-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


