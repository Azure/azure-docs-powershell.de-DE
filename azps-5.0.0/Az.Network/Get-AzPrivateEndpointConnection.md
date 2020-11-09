---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302020"
---
# <span data-ttu-id="20a63-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20a63-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="20a63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20a63-102">SYNOPSIS</span></span>
<span data-ttu-id="20a63-103">Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="20a63-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="20a63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20a63-104">SYNTAX</span></span>

### <span data-ttu-id="20a63-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="20a63-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a63-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="20a63-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a63-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="20a63-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="20a63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a63-108">DESCRIPTION</span></span>
<span data-ttu-id="20a63-109">Das Cmdlet " **Get-AzPrivateEndpointConnection** " Ruft eine private Endpunkt Verbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="20a63-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="20a63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20a63-110">EXAMPLES</span></span>

### <span data-ttu-id="20a63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20a63-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="20a63-112">In diesem Beispiel wird eine Liste aller privaten Endpunkt Verbindungen zurückgegeben, die zu SQL Server mit dem Namen MySQL gehören.</span><span class="sxs-lookup"><span data-stu-id="20a63-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="20a63-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20a63-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="20a63-114">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 gehört zum privaten Link Dienst mit dem Namen MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20a63-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="20a63-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a63-115">PARAMETERS</span></span>

### <span data-ttu-id="20a63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a63-116">-DefaultProfile</span></span>
<span data-ttu-id="20a63-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20a63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a63-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a63-118">-Description</span></span>
<span data-ttu-id="20a63-119">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="20a63-119">The reason of action.</span></span>

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

### <span data-ttu-id="20a63-120">-Name</span><span class="sxs-lookup"><span data-stu-id="20a63-120">-Name</span></span>
<span data-ttu-id="20a63-121">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="20a63-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20a63-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="20a63-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="20a63-123">Die Azure Resource Manager-ID der privaten Link Ressource, zu der eine private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="20a63-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="20a63-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="20a63-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="20a63-125">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="20a63-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20a63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a63-126">-ResourceGroupName</span></span>
<span data-ttu-id="20a63-127">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="20a63-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20a63-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20a63-128">-ResourceId</span></span>
<span data-ttu-id="20a63-129">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="20a63-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20a63-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20a63-130">-ServiceName</span></span>
<span data-ttu-id="20a63-131">Der Name des Diensts, zu dem die private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="20a63-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="20a63-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a63-132">CommonParameters</span></span>
<span data-ttu-id="20a63-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a63-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a63-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a63-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a63-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20a63-135">INPUTS</span></span>

### <span data-ttu-id="20a63-136">System. String</span><span class="sxs-lookup"><span data-stu-id="20a63-136">System.String</span></span>

## <span data-ttu-id="20a63-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20a63-137">OUTPUTS</span></span>

### <span data-ttu-id="20a63-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20a63-138">System.Boolean</span></span>

## <span data-ttu-id="20a63-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="20a63-139">NOTES</span></span>

## <span data-ttu-id="20a63-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20a63-140">RELATED LINKS</span></span>

[<span data-ttu-id="20a63-141">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20a63-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20a63-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20a63-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20a63-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20a63-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20a63-144">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20a63-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
