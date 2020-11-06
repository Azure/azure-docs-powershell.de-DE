---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500114"
---
# <span data-ttu-id="24a19-101">Get-AzureRmExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="24a19-101">Get-AzureRmExternalSecuritySolution</span></span>

## <span data-ttu-id="24a19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24a19-102">SYNOPSIS</span></span>
<span data-ttu-id="24a19-103">Abrufen einer externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="24a19-103">Get external security solution</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24a19-104">SYNTAX</span></span>

### <span data-ttu-id="24a19-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="24a19-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a19-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="24a19-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a19-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="24a19-107">SubscriptionLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24a19-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a19-108">ResourceId</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24a19-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24a19-109">DESCRIPTION</span></span>
<span data-ttu-id="24a19-110">Abrufen einer externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="24a19-110">Get external security solution</span></span>

## <span data-ttu-id="24a19-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24a19-111">EXAMPLES</span></span>

### <span data-ttu-id="24a19-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24a19-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
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

<span data-ttu-id="24a19-113">Abrufen aller externen Sicherheitslösungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="24a19-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="24a19-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="24a19-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="24a19-115">Abrufen einer bestimmten externen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="24a19-115">Get a specific external security solution</span></span>

## <span data-ttu-id="24a19-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="24a19-116">PARAMETERS</span></span>

### <span data-ttu-id="24a19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a19-117">-DefaultProfile</span></span>
<span data-ttu-id="24a19-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24a19-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a19-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="24a19-119">-Location</span></span>
<span data-ttu-id="24a19-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="24a19-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a19-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24a19-121">-Name</span></span>
<span data-ttu-id="24a19-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="24a19-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a19-123">-ResourceGroupName</span></span>
<span data-ttu-id="24a19-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24a19-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a19-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="24a19-125">-ResourceId</span></span>
<span data-ttu-id="24a19-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="24a19-126">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a19-127">CommonParameters</span></span>
<span data-ttu-id="24a19-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a19-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a19-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24a19-130">INPUTS</span></span>

### <span data-ttu-id="24a19-131">System. String</span><span class="sxs-lookup"><span data-stu-id="24a19-131">System.String</span></span>

## <span data-ttu-id="24a19-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24a19-132">OUTPUTS</span></span>

### <span data-ttu-id="24a19-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="24a19-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="24a19-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="24a19-134">NOTES</span></span>

## <span data-ttu-id="24a19-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24a19-135">RELATED LINKS</span></span>
