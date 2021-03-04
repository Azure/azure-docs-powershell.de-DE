---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 251692538dbd9c5db28718c5833c9a3d096d9503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936811"
---
# <span data-ttu-id="c3dbb-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="c3dbb-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="c3dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dbb-103">Ruft die RegistryStatistics für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="c3dbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3dbb-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3dbb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="c3dbb-106">Ruft die RegistryStatistics für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="c3dbb-107">Dies enthält Informationen zur Anzahl der insgesamt aktivierten und deaktivierten Geräte in einem IotHub.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="c3dbb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3dbb-108">EXAMPLES</span></span>

### <span data-ttu-id="c3dbb-109">Beispiel 1 : "Registrierungsstatistik"</span><span class="sxs-lookup"><span data-stu-id="c3dbb-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c3dbb-110">Ruft die RegistryStatistics für den IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c3dbb-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3dbb-111">PARAMETERS</span></span>

### <span data-ttu-id="c3dbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dbb-112">-DefaultProfile</span></span>
<span data-ttu-id="c3dbb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c3dbb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3dbb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c3dbb-114">-Name</span></span>
<span data-ttu-id="c3dbb-115">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-115">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3dbb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3dbb-116">-ResourceGroupName</span></span>
<span data-ttu-id="c3dbb-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c3dbb-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3dbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dbb-118">CommonParameters</span></span>
<span data-ttu-id="c3dbb-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3dbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dbb-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3dbb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dbb-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3dbb-121">INPUTS</span></span>

### <span data-ttu-id="c3dbb-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c3dbb-122">System.String</span></span>

## <span data-ttu-id="c3dbb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3dbb-123">OUTPUTS</span></span>

### <span data-ttu-id="c3dbb-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="c3dbb-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="c3dbb-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3dbb-125">NOTES</span></span>

## <span data-ttu-id="c3dbb-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3dbb-126">RELATED LINKS</span></span>
