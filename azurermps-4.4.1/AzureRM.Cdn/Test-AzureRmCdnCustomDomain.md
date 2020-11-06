---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497850"
---
# <span data-ttu-id="7e846-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7e846-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="7e846-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e846-102">SYNOPSIS</span></span>
<span data-ttu-id="7e846-103">Überprüft, ob einem Endpunkt eine benutzerdefinierte Domäne hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e846-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e846-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e846-104">SYNTAX</span></span>

### <span data-ttu-id="7e846-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e846-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e846-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="7e846-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e846-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e846-107">DESCRIPTION</span></span>
<span data-ttu-id="7e846-108">Das Cmdlet **Test-AzureRmCdnCustomDomain** überprüft, ob eine benutzerdefinierte Domäne einem Endpunkt hinzugefügt werden kann, indem die CNAME-Zuordnung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="7e846-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="7e846-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e846-109">EXAMPLES</span></span>

## <span data-ttu-id="7e846-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e846-110">PARAMETERS</span></span>

### <span data-ttu-id="7e846-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e846-111">-CdnEndpoint</span></span>
<span data-ttu-id="7e846-112">Gibt den Endpunkt an, dem Sie die benutzerdefinierte Domäne hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e846-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="7e846-113">-CustomDomainHostName</span></span>
<span data-ttu-id="7e846-114">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="7e846-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="7e846-115">-EndpointName</span></span>
<span data-ttu-id="7e846-116">Gibt den Namen des Endpunkts an, dem Sie die benutzerdefinierte Domäne hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e846-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="7e846-117">-ProfileName</span></span>
<span data-ttu-id="7e846-118">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="7e846-118">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e846-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e846-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7e846-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e846-121">-DefaultProfile</span></span>
<span data-ttu-id="7e846-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e846-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e846-123">CommonParameters</span></span>
<span data-ttu-id="7e846-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e846-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e846-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e846-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e846-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e846-126">INPUTS</span></span>

### <span data-ttu-id="7e846-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e846-127">PSEndpoint</span></span>
<span data-ttu-id="7e846-128">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e846-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7e846-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e846-129">OUTPUTS</span></span>

### <span data-ttu-id="7e846-130">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="7e846-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="7e846-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e846-131">NOTES</span></span>

## <span data-ttu-id="7e846-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e846-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e846-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7e846-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7e846-134">Neu – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7e846-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7e846-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7e846-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


