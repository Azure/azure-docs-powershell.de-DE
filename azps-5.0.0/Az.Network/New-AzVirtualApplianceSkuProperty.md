---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301432"
---
# <span data-ttu-id="22b8b-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="22b8b-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="22b8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="22b8b-103">Definieren Sie eine Network Virtual Appliance-SKU für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="22b8b-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="22b8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b8b-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="22b8b-106">Der Befehl New-AzVirtualApplianceSkuProperties definiert eine SKU für die virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="22b8b-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="22b8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="22b8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22b8b-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="22b8b-109">Erstellen Sie ein virtuelles Appliance-SKU-Eigenschaftenobjekt, das mit New-AzNetworkVirtualAppliance Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22b8b-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="22b8b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b8b-110">PARAMETERS</span></span>

### <span data-ttu-id="22b8b-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="22b8b-111">-BundledScaleUnit</span></span>
<span data-ttu-id="22b8b-112">Die gebündelte Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="22b8b-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b8b-113">-DefaultProfile</span></span>
<span data-ttu-id="22b8b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22b8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b8b-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="22b8b-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="22b8b-116">Die Marktplatz Version.</span><span class="sxs-lookup"><span data-stu-id="22b8b-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b8b-117">-Lieferantenname</span><span class="sxs-lookup"><span data-stu-id="22b8b-117">-VendorName</span></span>
<span data-ttu-id="22b8b-118">Der Name des Kreditors.</span><span class="sxs-lookup"><span data-stu-id="22b8b-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b8b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b8b-119">CommonParameters</span></span>
<span data-ttu-id="22b8b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b8b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b8b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22b8b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b8b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22b8b-122">INPUTS</span></span>

### <span data-ttu-id="22b8b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="22b8b-123">None</span></span>

## <span data-ttu-id="22b8b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22b8b-124">OUTPUTS</span></span>

### <span data-ttu-id="22b8b-125">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="22b8b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="22b8b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="22b8b-126">NOTES</span></span>

## <span data-ttu-id="22b8b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22b8b-127">RELATED LINKS</span></span>
