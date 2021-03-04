---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926571"
---
# <span data-ttu-id="fbe63-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fbe63-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="fbe63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe63-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe63-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="fbe63-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="fbe63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbe63-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe63-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbe63-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe63-106">Das **Get-AzEffectiveRouteTable-Cmdlet** gibt die effektive Routentabelle zurück, die auf eine Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbe63-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="fbe63-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbe63-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe63-108">Beispiel 1: Erhalten der effektiven Routentabelle auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="fbe63-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fbe63-109">Dieser Befehl ruft die effektive Routentabelle ab, die der Netzwerkschnittstelle "MyNetworkInterface" in der Ressourcengruppe "MyResourceGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fbe63-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fbe63-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fbe63-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe63-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbe63-111">-AsJob</span></span>
<span data-ttu-id="fbe63-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fbe63-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbe63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe63-113">-DefaultProfile</span></span>
<span data-ttu-id="fbe63-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbe63-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe63-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fbe63-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="fbe63-116">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="fbe63-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="fbe63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe63-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbe63-118">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="fbe63-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="fbe63-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe63-119">CommonParameters</span></span>
<span data-ttu-id="fbe63-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe63-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe63-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbe63-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe63-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbe63-122">INPUTS</span></span>

### <span data-ttu-id="fbe63-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe63-123">System.String</span></span>

## <span data-ttu-id="fbe63-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbe63-124">OUTPUTS</span></span>

### <span data-ttu-id="fbe63-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="fbe63-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="fbe63-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fbe63-126">NOTES</span></span>

## <span data-ttu-id="fbe63-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fbe63-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbe63-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fbe63-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


