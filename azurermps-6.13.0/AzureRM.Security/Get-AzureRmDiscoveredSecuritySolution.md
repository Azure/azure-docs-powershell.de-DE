---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482069"
---
# <span data-ttu-id="b07d4-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b07d4-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="b07d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b07d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b07d4-103">Ruft Sicherheitslösungen ab, die vom Azure Security Center erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="b07d4-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b07d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b07d4-104">SYNTAX</span></span>

### <span data-ttu-id="b07d4-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="b07d4-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07d4-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b07d4-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07d4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b07d4-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b07d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b07d4-108">DESCRIPTION</span></span>
<span data-ttu-id="b07d4-109">Sicherheitslösungen werden automatisch vom Azure Security Center erkannt, verwenden Sie dieses Cmdlet, um die gefundenen Sicherheitslösungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b07d4-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="b07d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b07d4-110">EXAMPLES</span></span>

### <span data-ttu-id="b07d4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b07d4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="b07d4-112">Abrufen aller gefundenen Sicherheitslösungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="b07d4-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="b07d4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b07d4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="b07d4-114">Abrufen einer bestimmten gefundenen Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="b07d4-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="b07d4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07d4-115">PARAMETERS</span></span>

### <span data-ttu-id="b07d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07d4-116">-DefaultProfile</span></span>
<span data-ttu-id="b07d4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b07d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07d4-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="b07d4-118">-Location</span></span>
<span data-ttu-id="b07d4-119">Lage.</span><span class="sxs-lookup"><span data-stu-id="b07d4-119">Location.</span></span>

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

### <span data-ttu-id="b07d4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b07d4-120">-Name</span></span>
<span data-ttu-id="b07d4-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b07d4-121">Resource name.</span></span>

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

### <span data-ttu-id="b07d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b07d4-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b07d4-123">Resource group name.</span></span>

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

### <span data-ttu-id="b07d4-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b07d4-124">-ResourceId</span></span>
<span data-ttu-id="b07d4-125">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b07d4-125">Resource ID.</span></span>

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

### <span data-ttu-id="b07d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07d4-126">CommonParameters</span></span>
<span data-ttu-id="b07d4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07d4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07d4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b07d4-129">INPUTS</span></span>

### <span data-ttu-id="b07d4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b07d4-130">System.String</span></span>

## <span data-ttu-id="b07d4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b07d4-131">OUTPUTS</span></span>

### <span data-ttu-id="b07d4-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b07d4-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="b07d4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b07d4-133">NOTES</span></span>

## <span data-ttu-id="b07d4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b07d4-134">RELATED LINKS</span></span>
