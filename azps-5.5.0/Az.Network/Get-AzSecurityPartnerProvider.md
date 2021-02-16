---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160969"
---
# <span data-ttu-id="9d909-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9d909-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="9d909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d909-102">SYNOPSIS</span></span>
<span data-ttu-id="9d909-103">Azure SecurityPartnerProvider erhalten</span><span class="sxs-lookup"><span data-stu-id="9d909-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="9d909-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d909-104">SYNTAX</span></span>

### <span data-ttu-id="9d909-105">SecurityPartnerProviderNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d909-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d909-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d909-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d909-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d909-107">DESCRIPTION</span></span>
<span data-ttu-id="9d909-108">Das **Cmdlet "Get-AzSecurityPartnerProvider"** erhält einen Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9d909-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="9d909-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d909-109">EXAMPLES</span></span>

### <span data-ttu-id="9d909-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d909-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="9d909-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d909-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="9d909-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d909-112">PARAMETERS</span></span>

### <span data-ttu-id="9d909-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d909-113">-DefaultProfile</span></span>
<span data-ttu-id="9d909-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d909-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d909-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9d909-115">-Name</span></span>
<span data-ttu-id="9d909-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9d909-116">The resource name.</span></span>

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

### <span data-ttu-id="9d909-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d909-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d909-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d909-118">The resource group name.</span></span>

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

### <span data-ttu-id="9d909-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d909-119">-ResourceId</span></span>
<span data-ttu-id="9d909-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9d909-120">The resource Id.</span></span>

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

### <span data-ttu-id="9d909-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d909-121">CommonParameters</span></span>
<span data-ttu-id="9d909-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d909-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d909-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d909-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d909-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d909-124">INPUTS</span></span>

### <span data-ttu-id="9d909-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9d909-125">System.String</span></span>

## <span data-ttu-id="9d909-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d909-126">OUTPUTS</span></span>

### <span data-ttu-id="9d909-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9d909-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="9d909-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d909-128">NOTES</span></span>

## <span data-ttu-id="9d909-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d909-129">RELATED LINKS</span></span>
