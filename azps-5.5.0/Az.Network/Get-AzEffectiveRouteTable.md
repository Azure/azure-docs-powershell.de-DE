---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159196"
---
# <span data-ttu-id="fcacf-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fcacf-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="fcacf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcacf-102">SYNOPSIS</span></span>
<span data-ttu-id="fcacf-103">Ruft die effektive Routentabelle einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="fcacf-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="fcacf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcacf-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcacf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcacf-105">DESCRIPTION</span></span>
<span data-ttu-id="fcacf-106">Das **Cmdlet "Get-AzEffectiveRouteTable"** gibt die effektive Routentabelle zurück, die auf eine Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcacf-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="fcacf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcacf-107">EXAMPLES</span></span>

### <span data-ttu-id="fcacf-108">Beispiel 1: Erstellen der Tabelle für effektive Routen auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="fcacf-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fcacf-109">Dieser Befehl ruft die effektive Routentabelle ab, die der Netzwerkschnittstelle "MyNetworkInterface" in der Ressourcengruppe namens "MyResourceGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fcacf-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fcacf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcacf-110">PARAMETERS</span></span>

### <span data-ttu-id="fcacf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcacf-111">-AsJob</span></span>
<span data-ttu-id="fcacf-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fcacf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcacf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcacf-113">-DefaultProfile</span></span>
<span data-ttu-id="fcacf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcacf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcacf-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fcacf-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="fcacf-116">Der Name einer Netzwerkschnittstelle wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="fcacf-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="fcacf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcacf-117">-ResourceGroupName</span></span>
<span data-ttu-id="fcacf-118">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="fcacf-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="fcacf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcacf-119">CommonParameters</span></span>
<span data-ttu-id="fcacf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcacf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcacf-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcacf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcacf-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcacf-122">INPUTS</span></span>

### <span data-ttu-id="fcacf-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fcacf-123">System.String</span></span>

## <span data-ttu-id="fcacf-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcacf-124">OUTPUTS</span></span>

### <span data-ttu-id="fcacf-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="fcacf-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="fcacf-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcacf-126">NOTES</span></span>

## <span data-ttu-id="fcacf-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcacf-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcacf-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fcacf-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


