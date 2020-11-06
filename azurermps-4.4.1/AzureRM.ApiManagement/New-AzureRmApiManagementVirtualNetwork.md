---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477445"
---
# <span data-ttu-id="a4338-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4338-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a4338-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4338-102">SYNOPSIS</span></span>
<span data-ttu-id="a4338-103">Erstellt eine Instanz von PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a4338-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4338-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4338-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4338-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4338-105">DESCRIPTION</span></span>
<span data-ttu-id="a4338-106">Das Cmdlet **New-AzureRmApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="a4338-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="a4338-107">Dieser Befehl wird mit dem Cmdlet " **Satz-AzureRMApiManagementVirtualNetworks** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4338-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="a4338-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4338-108">EXAMPLES</span></span>

### <span data-ttu-id="a4338-109">Beispiel 1: Erstellen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="a4338-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="a4338-110">In diesem Beispiel wird ein virtuelles Netzwerk erstellt und anschließend das Cmdlet " **setAzureRmApiManagementVirtualNetworks** " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a4338-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="a4338-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4338-111">PARAMETERS</span></span>

### <span data-ttu-id="a4338-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="a4338-112">-Location</span></span>
<span data-ttu-id="a4338-113">Gibt den Speicherort des virtuellen Netzwerks an, in dem dieses Cmdlet die Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4338-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="a4338-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a4338-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4338-115">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="a4338-115">North Central US</span></span>
- <span data-ttu-id="a4338-116">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="a4338-116">South Central US</span></span>
- <span data-ttu-id="a4338-117">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="a4338-117">Central US</span></span>
- <span data-ttu-id="a4338-118">West Europa</span><span class="sxs-lookup"><span data-stu-id="a4338-118">West Europe</span></span>
- <span data-ttu-id="a4338-119">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="a4338-119">North Europe</span></span>
- <span data-ttu-id="a4338-120">West-US</span><span class="sxs-lookup"><span data-stu-id="a4338-120">West US</span></span>
- <span data-ttu-id="a4338-121">East US</span><span class="sxs-lookup"><span data-stu-id="a4338-121">East US</span></span>
- <span data-ttu-id="a4338-122">East US 2</span><span class="sxs-lookup"><span data-stu-id="a4338-122">East US 2</span></span>
- <span data-ttu-id="a4338-123">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="a4338-123">Japan East</span></span>
- <span data-ttu-id="a4338-124">Japan West</span><span class="sxs-lookup"><span data-stu-id="a4338-124">Japan West</span></span>
- <span data-ttu-id="a4338-125">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="a4338-125">Brazil South</span></span>
- <span data-ttu-id="a4338-126">Südostasien</span><span class="sxs-lookup"><span data-stu-id="a4338-126">Southeast Asia</span></span>
- <span data-ttu-id="a4338-127">Ostasien</span><span class="sxs-lookup"><span data-stu-id="a4338-127">East Asia</span></span>
- <span data-ttu-id="a4338-128">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="a4338-128">Australia East</span></span>
- <span data-ttu-id="a4338-129">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="a4338-129">Australia Southeast</span></span>

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

### <span data-ttu-id="a4338-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="a4338-130">-SubnetResourceId</span></span>
<span data-ttu-id="a4338-131">Gibt die Subnetz-Ressourcen-ID des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a4338-131">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="a4338-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4338-132">-DefaultProfile</span></span>
<span data-ttu-id="a4338-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4338-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4338-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4338-134">CommonParameters</span></span>
<span data-ttu-id="a4338-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4338-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4338-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4338-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4338-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4338-137">INPUTS</span></span>

## <span data-ttu-id="a4338-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4338-138">OUTPUTS</span></span>

### <span data-ttu-id="a4338-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4338-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a4338-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4338-140">NOTES</span></span>

## <span data-ttu-id="a4338-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4338-141">RELATED LINKS</span></span>

