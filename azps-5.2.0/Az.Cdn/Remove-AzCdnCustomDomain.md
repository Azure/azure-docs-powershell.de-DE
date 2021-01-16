---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307544"
---
# <span data-ttu-id="6b1a1-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="6b1a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1a1-103">Entfernt eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-103">Removes a custom domain.</span></span>

## <span data-ttu-id="6b1a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b1a1-104">SYNTAX</span></span>

### <span data-ttu-id="6b1a1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b1a1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1a1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b1a1-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1a1-108">Das **Cmdlet "Remove-AzCdnCustomDomain"** entfernt die benutzerdefinierte Domäne von einem Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6b1a1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b1a1-109">EXAMPLES</span></span>

## <span data-ttu-id="6b1a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b1a1-110">PARAMETERS</span></span>

### <span data-ttu-id="6b1a1-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-111">-CdnCustomDomain</span></span>
<span data-ttu-id="6b1a1-112">Gibt die benutzerdefinierte Domäne an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1a1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6b1a1-113">-CustomDomainName</span></span>
<span data-ttu-id="6b1a1-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b1a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1a1-115">-DefaultProfile</span></span>
<span data-ttu-id="6b1a1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6b1a1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b1a1-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b1a1-117">-EndpointName</span></span>
<span data-ttu-id="6b1a1-118">Gibt den Namen des Endpunkts an, von dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b1a1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b1a1-119">-PassThru</span></span>
<span data-ttu-id="6b1a1-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b1a1-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1a1-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6b1a1-122">-ProfileName</span></span>
<span data-ttu-id="6b1a1-123">Gibt den Namen des Profils an, aus dem dieses Cmdlet eine benutzerdefinierte Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b1a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b1a1-125">Gibt den Namen der Ressourcengruppe an, aus der mit diesem Cmdlet eine benutzerdefinierte Domäne entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b1a1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b1a1-126">-Confirm</span></span>
<span data-ttu-id="6b1a1-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1a1-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6b1a1-128">-WhatIf</span></span>
<span data-ttu-id="6b1a1-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1a1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1a1-131">CommonParameters</span></span>
<span data-ttu-id="6b1a1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1a1-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b1a1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1a1-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b1a1-134">INPUTS</span></span>

### <span data-ttu-id="6b1a1-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="6b1a1-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b1a1-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b1a1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b1a1-137">OUTPUTS</span></span>

### <span data-ttu-id="6b1a1-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b1a1-138">System.Boolean</span></span>

## <span data-ttu-id="6b1a1-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b1a1-139">NOTES</span></span>

## <span data-ttu-id="6b1a1-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b1a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="6b1a1-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="6b1a1-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="6b1a1-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b1a1-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


