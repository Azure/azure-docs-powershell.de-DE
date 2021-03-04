---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 99498979df259723a192bd0e2fd74ef436ae0ee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919635"
---
# <span data-ttu-id="fa80e-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fa80e-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="fa80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa80e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa80e-103">Azure SecurityPartnerProvider erhalten</span><span class="sxs-lookup"><span data-stu-id="fa80e-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="fa80e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa80e-104">SYNTAX</span></span>

### <span data-ttu-id="fa80e-105">SecurityPartnerProviderNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa80e-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa80e-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa80e-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa80e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa80e-107">DESCRIPTION</span></span>
<span data-ttu-id="fa80e-108">Das **Get-AzSecurityPartnerProvider-Cmdlet** erhält einen Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fa80e-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="fa80e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa80e-109">EXAMPLES</span></span>

### <span data-ttu-id="fa80e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa80e-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="fa80e-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fa80e-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="fa80e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa80e-112">PARAMETERS</span></span>

### <span data-ttu-id="fa80e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa80e-113">-DefaultProfile</span></span>
<span data-ttu-id="fa80e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa80e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa80e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fa80e-115">-Name</span></span>
<span data-ttu-id="fa80e-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fa80e-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa80e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa80e-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa80e-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fa80e-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa80e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa80e-119">-ResourceId</span></span>
<span data-ttu-id="fa80e-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fa80e-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa80e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa80e-121">CommonParameters</span></span>
<span data-ttu-id="fa80e-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa80e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa80e-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa80e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa80e-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa80e-124">INPUTS</span></span>

### <span data-ttu-id="fa80e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fa80e-125">System.String</span></span>

## <span data-ttu-id="fa80e-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa80e-126">OUTPUTS</span></span>

### <span data-ttu-id="fa80e-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fa80e-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="fa80e-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa80e-128">NOTES</span></span>

## <span data-ttu-id="fa80e-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa80e-129">RELATED LINKS</span></span>
