---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174735"
---
# <span data-ttu-id="2f2a2-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="2f2a2-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="2f2a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2a2-103">Deaktivieren von HTTPS für eine benutzerdefinierte Domäne</span><span class="sxs-lookup"><span data-stu-id="2f2a2-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="2f2a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2a2-104">SYNTAX</span></span>

### <span data-ttu-id="2f2a2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f2a2-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f2a2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f2a2-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2a2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f2a2-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f2a2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f2a2-108">DESCRIPTION</span></span>
<span data-ttu-id="2f2a2-109">Das **AzFrontDoorCustomDomainHttps deaktiviert** HTTPS für eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="2f2a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f2a2-110">EXAMPLES</span></span>

### <span data-ttu-id="2f2a2-111">Beispiel 1: Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit FrontDoorName und ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="2f2a2-112">Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-Custom-XYZ" mit FrontDoorName als "frontdoor1" und ResourceGroupName als "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="2f2a2-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="2f2a2-113">Beispiel 2: Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit dem PSFrontendEndpoint-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="2f2a2-114">Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit dem PSFrontendEndpoint-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="2f2a2-115">Beispiel 3: Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit der Resourcen-Funktion.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="2f2a2-116">Deaktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-Custom-XYZ" mit der Option "$ResourceId".</span><span class="sxs-lookup"><span data-stu-id="2f2a2-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="2f2a2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f2a2-117">PARAMETERS</span></span>

### <span data-ttu-id="2f2a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2a2-118">-DefaultProfile</span></span>
<span data-ttu-id="2f2a2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f2a2-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2f2a2-120">-FrontDoorName</span></span>
<span data-ttu-id="2f2a2-121">Der Name der Haustür.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="2f2a2-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f2a2-122">-FrontendEndpointName</span></span>
<span data-ttu-id="2f2a2-123">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="2f2a2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f2a2-124">-InputObject</span></span>
<span data-ttu-id="2f2a2-125">Das zu aktualisierbare Frontend-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f2a2-127">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="2f2a2-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2f2a2-128">-ResourceId</span></span>
<span data-ttu-id="2f2a2-129">Ressourcen-ID des Front-Door-Endpunkts zum Deaktivieren von HTTPS</span><span class="sxs-lookup"><span data-stu-id="2f2a2-129">Resource Id of the Front Door endpoint to disable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f2a2-130">-Confirm</span></span>
<span data-ttu-id="2f2a2-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f2a2-132">-WhatIf</span></span>
<span data-ttu-id="2f2a2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f2a2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2a2-135">CommonParameters</span></span>
<span data-ttu-id="2f2a2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2a2-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f2a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2a2-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f2a2-138">INPUTS</span></span>

### <span data-ttu-id="2f2a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2a2-139">System.String</span></span>

## <span data-ttu-id="2f2a2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f2a2-140">OUTPUTS</span></span>

### <span data-ttu-id="2f2a2-141">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f2a2-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="2f2a2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f2a2-142">NOTES</span></span>

## <span data-ttu-id="2f2a2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f2a2-143">RELATED LINKS</span></span>
