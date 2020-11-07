---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d5fca22bf289c42681d9af18a9eaff28587f1922
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824867"
---
# <span data-ttu-id="86dec-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="86dec-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="86dec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86dec-102">SYNOPSIS</span></span>
<span data-ttu-id="86dec-103">Ruft Sicherheitslösungen ab, die vom Azure Security Center erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="86dec-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="86dec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86dec-104">SYNTAX</span></span>

### <span data-ttu-id="86dec-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="86dec-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86dec-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="86dec-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86dec-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="86dec-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86dec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86dec-108">DESCRIPTION</span></span>
<span data-ttu-id="86dec-109">Sicherheitslösungen werden automatisch vom Azure Security Center erkannt, verwenden Sie dieses Cmdlet, um die gefundenen Sicherheitslösungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="86dec-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="86dec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86dec-110">EXAMPLES</span></span>

### <span data-ttu-id="86dec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86dec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="86dec-112">Abrufen aller gefundenen Sicherheitslösungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="86dec-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="86dec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="86dec-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="86dec-114">Abrufen einer bestimmten gefundenen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="86dec-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="86dec-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="86dec-115">PARAMETERS</span></span>

### <span data-ttu-id="86dec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86dec-116">-DefaultProfile</span></span>
<span data-ttu-id="86dec-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86dec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86dec-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="86dec-118">-Location</span></span>
<span data-ttu-id="86dec-119">Lage.</span><span class="sxs-lookup"><span data-stu-id="86dec-119">Location.</span></span>

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

### <span data-ttu-id="86dec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="86dec-120">-Name</span></span>
<span data-ttu-id="86dec-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="86dec-121">Resource name.</span></span>

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

### <span data-ttu-id="86dec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86dec-122">-ResourceGroupName</span></span>
<span data-ttu-id="86dec-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86dec-123">Resource group name.</span></span>

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

### <span data-ttu-id="86dec-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="86dec-124">-ResourceId</span></span>
<span data-ttu-id="86dec-125">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="86dec-125">Resource ID.</span></span>

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

### <span data-ttu-id="86dec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86dec-126">CommonParameters</span></span>
<span data-ttu-id="86dec-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86dec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86dec-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86dec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86dec-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86dec-129">INPUTS</span></span>

### <span data-ttu-id="86dec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="86dec-130">System.String</span></span>

## <span data-ttu-id="86dec-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86dec-131">OUTPUTS</span></span>

### <span data-ttu-id="86dec-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="86dec-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="86dec-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="86dec-133">NOTES</span></span>

## <span data-ttu-id="86dec-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86dec-134">RELATED LINKS</span></span>
