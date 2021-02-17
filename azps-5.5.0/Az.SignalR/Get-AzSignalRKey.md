---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156273"
---
# <span data-ttu-id="4a72d-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="4a72d-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="4a72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a72d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a72d-103">Holen Sie sich die Zugriffstasten eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="4a72d-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="4a72d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a72d-104">SYNTAX</span></span>

### <span data-ttu-id="4a72d-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a72d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a72d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a72d-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a72d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a72d-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a72d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a72d-108">DESCRIPTION</span></span>
<span data-ttu-id="4a72d-109">Holen Sie sich die Zugriffstasten eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="4a72d-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="4a72d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a72d-110">EXAMPLES</span></span>

### <span data-ttu-id="4a72d-111">Erhalten von Zugriffstasten für einen bestimmten SignalR-Dienst</span><span class="sxs-lookup"><span data-stu-id="4a72d-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="4a72d-112">Zugreifen auf Tasten von einem SignalR-Dienstobjekt in Pipe</span><span class="sxs-lookup"><span data-stu-id="4a72d-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="4a72d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a72d-113">PARAMETERS</span></span>

### <span data-ttu-id="4a72d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a72d-114">-DefaultProfile</span></span>
<span data-ttu-id="4a72d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a72d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a72d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a72d-116">-InputObject</span></span>
<span data-ttu-id="4a72d-117">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="4a72d-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4a72d-118">-Name</span></span>
<span data-ttu-id="4a72d-119">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="4a72d-119">SignalR service name.</span></span>

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

### <span data-ttu-id="4a72d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a72d-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a72d-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4a72d-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a72d-122">-ResourceId</span></span>
<span data-ttu-id="4a72d-123">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="4a72d-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="4a72d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a72d-124">CommonParameters</span></span>
<span data-ttu-id="4a72d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a72d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a72d-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a72d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a72d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a72d-127">INPUTS</span></span>

### <span data-ttu-id="4a72d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4a72d-128">System.String</span></span>
### <span data-ttu-id="4a72d-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4a72d-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="4a72d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a72d-130">OUTPUTS</span></span>

### <span data-ttu-id="4a72d-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="4a72d-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="4a72d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a72d-132">NOTES</span></span>

## <span data-ttu-id="4a72d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a72d-133">RELATED LINKS</span></span>
