---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167444"
---
# <span data-ttu-id="7bba5-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="7bba5-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="7bba5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bba5-102">SYNOPSIS</span></span>
<span data-ttu-id="7bba5-103">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="7bba5-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="7bba5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bba5-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bba5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bba5-105">DESCRIPTION</span></span>
<span data-ttu-id="7bba5-106">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="7bba5-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="7bba5-107">Damit erhalten Sie Informationen über die Anzahl der insgesamt aktivierten und deaktivierten Geräte in einem IotHub.</span><span class="sxs-lookup"><span data-stu-id="7bba5-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="7bba5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bba5-108">EXAMPLES</span></span>

### <span data-ttu-id="7bba5-109">Beispiel 1 Abrufen des RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="7bba5-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7bba5-110">Ruft die RegistryStatistics für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="7bba5-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7bba5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bba5-111">PARAMETERS</span></span>

### <span data-ttu-id="7bba5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bba5-112">-DefaultProfile</span></span>
<span data-ttu-id="7bba5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7bba5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bba5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7bba5-114">-Name</span></span>
<span data-ttu-id="7bba5-115">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="7bba5-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7bba5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bba5-116">-ResourceGroupName</span></span>
<span data-ttu-id="7bba5-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7bba5-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7bba5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bba5-118">CommonParameters</span></span>
<span data-ttu-id="7bba5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bba5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bba5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bba5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bba5-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bba5-121">INPUTS</span></span>

### <span data-ttu-id="7bba5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7bba5-122">System.String</span></span>

## <span data-ttu-id="7bba5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bba5-123">OUTPUTS</span></span>

### <span data-ttu-id="7bba5-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="7bba5-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="7bba5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bba5-125">NOTES</span></span>

## <span data-ttu-id="7bba5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bba5-126">RELATED LINKS</span></span>
