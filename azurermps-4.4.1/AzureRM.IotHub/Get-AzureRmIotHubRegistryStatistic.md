---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663571"
---
# <span data-ttu-id="11a8c-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="11a8c-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="11a8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="11a8c-103">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="11a8c-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a8c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="11a8c-106">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="11a8c-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="11a8c-107">Damit erhalten Sie Informationen über die Anzahl der insgesamt aktivierten und deaktivierten Geräte in einem IotHub.</span><span class="sxs-lookup"><span data-stu-id="11a8c-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="11a8c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11a8c-108">EXAMPLES</span></span>

### <span data-ttu-id="11a8c-109">Beispiel 1 Abrufen des RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="11a8c-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="11a8c-110">Ruft die RegistryStatictics für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="11a8c-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="11a8c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="11a8c-111">PARAMETERS</span></span>

### <span data-ttu-id="11a8c-112">-Name</span><span class="sxs-lookup"><span data-stu-id="11a8c-112">-Name</span></span>
<span data-ttu-id="11a8c-113">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="11a8c-113">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="11a8c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a8c-114">-ResourceGroupName</span></span>
<span data-ttu-id="11a8c-115">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="11a8c-115">Resource Group Name</span></span>

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

### <span data-ttu-id="11a8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a8c-116">-DefaultProfile</span></span>
<span data-ttu-id="11a8c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11a8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a8c-118">CommonParameters</span></span>
<span data-ttu-id="11a8c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a8c-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a8c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a8c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11a8c-121">INPUTS</span></span>

### <span data-ttu-id="11a8c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="11a8c-122">System.String</span></span>

## <span data-ttu-id="11a8c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11a8c-123">OUTPUTS</span></span>

### <span data-ttu-id="11a8c-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="11a8c-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="11a8c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="11a8c-125">NOTES</span></span>

## <span data-ttu-id="11a8c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11a8c-126">RELATED LINKS</span></span>

