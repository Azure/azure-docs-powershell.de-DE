---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174336"
---
# <span data-ttu-id="3dec7-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3dec7-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="3dec7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3dec7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dec7-103">Abrufen eines Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3dec7-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="3dec7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dec7-104">SYNTAX</span></span>

### <span data-ttu-id="3dec7-105">VirtualRouterSubscriptionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3dec7-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dec7-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dec7-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dec7-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dec7-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dec7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dec7-108">DESCRIPTION</span></span>
<span data-ttu-id="3dec7-109">Das Cmdlet " **Get-AzVirtualRouter** " Ruft ein Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3dec7-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="3dec7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dec7-110">EXAMPLES</span></span>

### <span data-ttu-id="3dec7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dec7-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="3dec7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3dec7-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="3dec7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dec7-113">PARAMETERS</span></span>

### <span data-ttu-id="3dec7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dec7-114">-DefaultProfile</span></span>
<span data-ttu-id="3dec7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3dec7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dec7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dec7-116">-ResourceGroupName</span></span>
<span data-ttu-id="3dec7-117">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3dec7-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dec7-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3dec7-118">-ResourceId</span></span>
<span data-ttu-id="3dec7-119">Die Quelle des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3dec7-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dec7-120">-Routername</span><span class="sxs-lookup"><span data-stu-id="3dec7-120">-RouterName</span></span>
<span data-ttu-id="3dec7-121">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3dec7-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dec7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dec7-122">CommonParameters</span></span>
<span data-ttu-id="3dec7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dec7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dec7-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dec7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dec7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3dec7-125">INPUTS</span></span>

### <span data-ttu-id="3dec7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3dec7-126">System.String</span></span>

## <span data-ttu-id="3dec7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3dec7-127">OUTPUTS</span></span>

### <span data-ttu-id="3dec7-128">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3dec7-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3dec7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3dec7-129">NOTES</span></span>

## <span data-ttu-id="3dec7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3dec7-130">RELATED LINKS</span></span>
