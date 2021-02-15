---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152873"
---
# <span data-ttu-id="7c95a-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="7c95a-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="7c95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c95a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c95a-103">Ruft die Registrierungsstatistik für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="7c95a-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="7c95a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c95a-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c95a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c95a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c95a-106">Ruft die Registrierungsstatistik für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="7c95a-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="7c95a-107">Hier finden Sie Informationen zur Gesamtzahl der aktivierten und deaktivierten Geräte in einem IotHub.</span><span class="sxs-lookup"><span data-stu-id="7c95a-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="7c95a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c95a-108">EXAMPLES</span></span>

### <span data-ttu-id="7c95a-109">Beispiel 1: "RegistryStatistics"</span><span class="sxs-lookup"><span data-stu-id="7c95a-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7c95a-110">Ruft die Registrierungsstatistik für IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="7c95a-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7c95a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c95a-111">PARAMETERS</span></span>

### <span data-ttu-id="7c95a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c95a-112">-DefaultProfile</span></span>
<span data-ttu-id="7c95a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7c95a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c95a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7c95a-114">-Name</span></span>
<span data-ttu-id="7c95a-115">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="7c95a-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7c95a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c95a-116">-ResourceGroupName</span></span>
<span data-ttu-id="7c95a-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7c95a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7c95a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c95a-118">CommonParameters</span></span>
<span data-ttu-id="7c95a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c95a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c95a-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c95a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c95a-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c95a-121">INPUTS</span></span>

### <span data-ttu-id="7c95a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="7c95a-122">System.String</span></span>

## <span data-ttu-id="7c95a-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c95a-123">OUTPUTS</span></span>

### <span data-ttu-id="7c95a-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="7c95a-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="7c95a-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c95a-125">NOTES</span></span>

## <span data-ttu-id="7c95a-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c95a-126">RELATED LINKS</span></span>
