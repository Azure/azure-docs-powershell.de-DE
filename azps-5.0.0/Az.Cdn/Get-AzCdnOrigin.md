---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179743"
---
# <span data-ttu-id="b88c5-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b88c5-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="b88c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b88c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b88c5-103">Ruft einen CDN-Ursprungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="b88c5-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="b88c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b88c5-104">SYNTAX</span></span>

### <span data-ttu-id="b88c5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b88c5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88c5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b88c5-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b88c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b88c5-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b88c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b88c5-108">DESCRIPTION</span></span>
<span data-ttu-id="b88c5-109">Das Cmdlet " **Get-AzCdnOrigin** " Ruft einen Azure Content Delivery Network (CDN)-Ursprungsserver und dessen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="b88c5-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="b88c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b88c5-110">EXAMPLES</span></span>

## <span data-ttu-id="b88c5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b88c5-111">PARAMETERS</span></span>

### <span data-ttu-id="b88c5-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b88c5-112">-CdnEndpoint</span></span>
<span data-ttu-id="b88c5-113">Gibt das CDN-Endpunkt Objekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="b88c5-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88c5-114">-DefaultProfile</span></span>
<span data-ttu-id="b88c5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b88c5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b88c5-116">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="b88c5-116">-EndpointName</span></span>
<span data-ttu-id="b88c5-117">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="b88c5-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b88c5-118">-OriginName</span></span>
<span data-ttu-id="b88c5-119">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b88c5-119">Specifies the name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b88c5-120">-ProfileName</span></span>
<span data-ttu-id="b88c5-121">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="b88c5-121">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="b88c5-123">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="b88c5-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b88c5-124">-ResourceId</span></span>
<span data-ttu-id="b88c5-125">Die Ressourcen-ID des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="b88c5-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88c5-126">CommonParameters</span></span>
<span data-ttu-id="b88c5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88c5-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b88c5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88c5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b88c5-129">INPUTS</span></span>

### <span data-ttu-id="b88c5-130">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b88c5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b88c5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b88c5-131">OUTPUTS</span></span>

### <span data-ttu-id="b88c5-132">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b88c5-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b88c5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b88c5-133">NOTES</span></span>

## <span data-ttu-id="b88c5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b88c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="b88c5-135">Satz-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b88c5-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


