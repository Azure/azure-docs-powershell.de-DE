---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165754"
---
# <span data-ttu-id="7556d-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7556d-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7556d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7556d-102">SYNOPSIS</span></span>
<span data-ttu-id="7556d-103">Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="7556d-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="7556d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7556d-104">SYNTAX</span></span>

### <span data-ttu-id="7556d-105">ByPrivateLinkResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="7556d-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7556d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7556d-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7556d-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="7556d-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7556d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7556d-108">DESCRIPTION</span></span>
<span data-ttu-id="7556d-109">Das Cmdlet " **Get-AzPrivateEndpointConnection** " Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="7556d-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="7556d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7556d-110">EXAMPLES</span></span>

### <span data-ttu-id="7556d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7556d-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="7556d-112">In diesem Beispiel wird eine Liste aller privaten Endpunkt Verbindungen zurückgegeben, die zu SQL Server mit dem Namen MySQL gehören.</span><span class="sxs-lookup"><span data-stu-id="7556d-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="7556d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7556d-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="7556d-114">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 gehört zum privaten Link Dienst mit dem Namen MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7556d-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="7556d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7556d-115">PARAMETERS</span></span>

### <span data-ttu-id="7556d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7556d-116">-DefaultProfile</span></span>
<span data-ttu-id="7556d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7556d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7556d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7556d-118">-Name</span></span>
<span data-ttu-id="7556d-119">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7556d-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7556d-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7556d-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7556d-121">Die Azure Resource Manager-ID der privaten Link Ressource, zu der eine private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="7556d-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7556d-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7556d-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7556d-123">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="7556d-123">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7556d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7556d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7556d-125">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7556d-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7556d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7556d-126">-ResourceId</span></span>
<span data-ttu-id="7556d-127">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7556d-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7556d-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7556d-128">-ServiceName</span></span>
<span data-ttu-id="7556d-129">Der Name des Diensts, zu dem die private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="7556d-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="7556d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7556d-130">CommonParameters</span></span>
<span data-ttu-id="7556d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7556d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7556d-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7556d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7556d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7556d-133">INPUTS</span></span>

### <span data-ttu-id="7556d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7556d-134">System.String</span></span>

## <span data-ttu-id="7556d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7556d-135">OUTPUTS</span></span>

### <span data-ttu-id="7556d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7556d-136">System.Boolean</span></span>

## <span data-ttu-id="7556d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="7556d-137">NOTES</span></span>

## <span data-ttu-id="7556d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7556d-138">RELATED LINKS</span></span>

[<span data-ttu-id="7556d-139">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7556d-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7556d-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7556d-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7556d-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7556d-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7556d-142">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7556d-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
