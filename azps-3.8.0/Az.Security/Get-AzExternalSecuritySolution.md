---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 2d018bd704d776b506035f365fc5045a51202d13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845800"
---
# <span data-ttu-id="a76fa-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a76fa-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="a76fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a76fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a76fa-103">Abrufen einer externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="a76fa-103">Get external security solution</span></span> 

## <span data-ttu-id="a76fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a76fa-104">SYNTAX</span></span>

### <span data-ttu-id="a76fa-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="a76fa-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a76fa-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a76fa-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a76fa-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a76fa-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a76fa-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a76fa-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a76fa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a76fa-109">DESCRIPTION</span></span>
<span data-ttu-id="a76fa-110">Abrufen einer externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="a76fa-110">Get external security solution</span></span>

## <span data-ttu-id="a76fa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a76fa-111">EXAMPLES</span></span>

### <span data-ttu-id="a76fa-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a76fa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="a76fa-113">Abrufen aller externen Sicherheitslösungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="a76fa-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="a76fa-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a76fa-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="a76fa-115">Abrufen einer bestimmten externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="a76fa-115">Get a specific external security solution</span></span>

## <span data-ttu-id="a76fa-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a76fa-116">PARAMETERS</span></span>

### <span data-ttu-id="a76fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76fa-117">-DefaultProfile</span></span>
<span data-ttu-id="a76fa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a76fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a76fa-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="a76fa-119">-Location</span></span>
<span data-ttu-id="a76fa-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="a76fa-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a76fa-121">-Name</span></span>
<span data-ttu-id="a76fa-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a76fa-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="a76fa-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a76fa-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fa-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a76fa-125">-ResourceId</span></span>
<span data-ttu-id="a76fa-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a76fa-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76fa-127">CommonParameters</span></span>
<span data-ttu-id="a76fa-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76fa-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76fa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76fa-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a76fa-130">INPUTS</span></span>

### <span data-ttu-id="a76fa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a76fa-131">System.String</span></span>

## <span data-ttu-id="a76fa-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a76fa-132">OUTPUTS</span></span>

### <span data-ttu-id="a76fa-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a76fa-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="a76fa-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a76fa-134">NOTES</span></span>

## <span data-ttu-id="a76fa-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a76fa-135">RELATED LINKS</span></span>
