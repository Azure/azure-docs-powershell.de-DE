---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920368"
---
# <span data-ttu-id="f8f75-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="f8f75-101">Get-AzSignalR</span></span>

## <span data-ttu-id="f8f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f75-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f75-103">Holen Sie sich einen bestimmten SignalR-Dienst oder alle SignalR-Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8f75-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="f8f75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8f75-104">SYNTAX</span></span>

### <span data-ttu-id="f8f75-105">ListSignalRServiceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f75-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f75-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f75-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f75-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f75-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f75-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8f75-108">DESCRIPTION</span></span>
<span data-ttu-id="f8f75-109">Holen Sie sich einen bestimmten SignalR-Dienst oder alle SignalR-Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8f75-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="f8f75-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8f75-110">EXAMPLES</span></span>

### <span data-ttu-id="f8f75-111">Alle SignalR-Dienste im Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="f8f75-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="f8f75-112">Alle SignalR-Dienste in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="f8f75-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f8f75-113">Einen bestimmten SignalR-Dienst erhalten</span><span class="sxs-lookup"><span data-stu-id="f8f75-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f8f75-114">Einen bestimmten SignalR-Dienst aus der Standardressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="f8f75-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="f8f75-115">Die Standardressourcengruppe kann von \` Set-AzDefault -ResourceGroupName myResourceGroup festgelegt \` werden.</span><span class="sxs-lookup"><span data-stu-id="f8f75-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="f8f75-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f8f75-116">PARAMETERS</span></span>

### <span data-ttu-id="f8f75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f75-117">-DefaultProfile</span></span>
<span data-ttu-id="f8f75-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8f75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f75-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f8f75-119">-Name</span></span>
<span data-ttu-id="f8f75-120">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f8f75-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f75-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8f75-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8f75-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f75-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f75-123">-ResourceId</span></span>
<span data-ttu-id="f8f75-124">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f8f75-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f75-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f75-125">CommonParameters</span></span>
<span data-ttu-id="f8f75-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f75-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f75-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8f75-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f75-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f75-128">INPUTS</span></span>

### <span data-ttu-id="f8f75-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f8f75-129">System.String</span></span>
## <span data-ttu-id="f8f75-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f75-130">OUTPUTS</span></span>

### <span data-ttu-id="f8f75-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f8f75-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="f8f75-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f8f75-132">NOTES</span></span>

## <span data-ttu-id="f8f75-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f8f75-133">RELATED LINKS</span></span>
