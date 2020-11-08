---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165762"
---
# <span data-ttu-id="062e6-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="062e6-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="062e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="062e6-102">SYNOPSIS</span></span>
<span data-ttu-id="062e6-103">Ruft die private DNS-Zonengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="062e6-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="062e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="062e6-104">SYNTAX</span></span>

### <span data-ttu-id="062e6-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="062e6-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="062e6-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="062e6-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="062e6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="062e6-107">DESCRIPTION</span></span>
<span data-ttu-id="062e6-108">Das Cmdlet " **Get-AzPrivateDnsZoneGroup** " ruft mindestens eine private DNS-Zonengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="062e6-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="062e6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="062e6-109">EXAMPLES</span></span>

### <span data-ttu-id="062e6-110">Beispiel 1: Abrufen der privaten DNS-Zonengruppe</span><span class="sxs-lookup"><span data-stu-id="062e6-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="062e6-111">Im obigen Beispiel wird eine private DNS-Zonengruppe mit dem Namen dnsgroup1 in der Ressourcengruppe RG abgerufen.</span><span class="sxs-lookup"><span data-stu-id="062e6-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="062e6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="062e6-112">PARAMETERS</span></span>

### <span data-ttu-id="062e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062e6-113">-DefaultProfile</span></span>
<span data-ttu-id="062e6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="062e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="062e6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="062e6-115">-Name</span></span>
<span data-ttu-id="062e6-116">Der Name der privaten DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="062e6-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="062e6-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="062e6-117">-PrivateEndpointName</span></span>
<span data-ttu-id="062e6-118">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="062e6-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="062e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="062e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="062e6-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="062e6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="062e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062e6-121">CommonParameters</span></span>
<span data-ttu-id="062e6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062e6-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="062e6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062e6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="062e6-124">INPUTS</span></span>

### <span data-ttu-id="062e6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="062e6-125">System.String</span></span>

## <span data-ttu-id="062e6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="062e6-126">OUTPUTS</span></span>

### <span data-ttu-id="062e6-127">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="062e6-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="062e6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="062e6-128">NOTES</span></span>

## <span data-ttu-id="062e6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="062e6-129">RELATED LINKS</span></span>
