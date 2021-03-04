---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: f9428c2249cf69d366a6770d448e82618d98896f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919731"
---
# <span data-ttu-id="2c8b8-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2c8b8-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2c8b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8b8-103">Ruft private DNS-Zonengruppe ab</span><span class="sxs-lookup"><span data-stu-id="2c8b8-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="2c8b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c8b8-104">SYNTAX</span></span>

### <span data-ttu-id="2c8b8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c8b8-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8b8-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="2c8b8-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c8b8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c8b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2c8b8-108">Das **Get-AzPrivateDnsZoneGroup-Cmdlet** ruft eine oder mehrere private DNS-Zonengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="2c8b8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c8b8-109">EXAMPLES</span></span>

### <span data-ttu-id="2c8b8-110">Beispiel 1: Abrufen einer privaten DNS-Zonengruppe</span><span class="sxs-lookup"><span data-stu-id="2c8b8-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="2c8b8-111">Im obigen Beispiel wird eine private DNS-Zonengruppe namens dnsgroup1 in der Ressourcengruppe rg ab.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="2c8b8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2c8b8-112">PARAMETERS</span></span>

### <span data-ttu-id="2c8b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8b8-113">-DefaultProfile</span></span>
<span data-ttu-id="2c8b8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8b8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2c8b8-115">-Name</span></span>
<span data-ttu-id="2c8b8-116">Der Name der gruppe für private DNS-Zonen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8b8-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="2c8b8-117">-PrivateEndpointName</span></span>
<span data-ttu-id="2c8b8-118">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c8b8-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8b8-121">CommonParameters</span></span>
<span data-ttu-id="2c8b8-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8b8-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8b8-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c8b8-124">INPUTS</span></span>

### <span data-ttu-id="2c8b8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2c8b8-125">System.String</span></span>

## <span data-ttu-id="2c8b8-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c8b8-126">OUTPUTS</span></span>

### <span data-ttu-id="2c8b8-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2c8b8-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2c8b8-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2c8b8-128">NOTES</span></span>

## <span data-ttu-id="2c8b8-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2c8b8-129">RELATED LINKS</span></span>
