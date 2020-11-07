---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821763"
---
# <span data-ttu-id="31a03-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31a03-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="31a03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31a03-102">SYNOPSIS</span></span>
<span data-ttu-id="31a03-103">Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="31a03-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="31a03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a03-104">SYNTAX</span></span>

### <span data-ttu-id="31a03-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="31a03-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31a03-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="31a03-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31a03-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31a03-107">DESCRIPTION</span></span>
<span data-ttu-id="31a03-108">Das Cmdlet " **Get-AzPrivateEndpointConnection** " Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="31a03-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="31a03-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31a03-109">EXAMPLES</span></span>

### <span data-ttu-id="31a03-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="31a03-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="31a03-111">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="31a03-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="31a03-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="31a03-112">PARAMETERS</span></span>

### <span data-ttu-id="31a03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a03-113">-DefaultProfile</span></span>
<span data-ttu-id="31a03-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31a03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a03-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31a03-115">-Description</span></span>
<span data-ttu-id="31a03-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="31a03-116">The reason of action.</span></span>

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

### <span data-ttu-id="31a03-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31a03-117">-Name</span></span>
<span data-ttu-id="31a03-118">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="31a03-118">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a03-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a03-119">-ResourceGroupName</span></span>
<span data-ttu-id="31a03-120">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="31a03-120">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a03-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="31a03-121">-ResourceId</span></span>
<span data-ttu-id="31a03-122">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="31a03-122">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a03-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="31a03-123">-ServiceName</span></span>
<span data-ttu-id="31a03-124">Der Name des privaten Link Diensts mit der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="31a03-124">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a03-125">CommonParameters</span></span>
<span data-ttu-id="31a03-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a03-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31a03-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a03-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31a03-128">INPUTS</span></span>

### <span data-ttu-id="31a03-129">System. String</span><span class="sxs-lookup"><span data-stu-id="31a03-129">System.String</span></span>

## <span data-ttu-id="31a03-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31a03-130">OUTPUTS</span></span>

### <span data-ttu-id="31a03-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31a03-131">System.Boolean</span></span>

## <span data-ttu-id="31a03-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="31a03-132">NOTES</span></span>

## <span data-ttu-id="31a03-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31a03-133">RELATED LINKS</span></span>

[<span data-ttu-id="31a03-134">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31a03-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
