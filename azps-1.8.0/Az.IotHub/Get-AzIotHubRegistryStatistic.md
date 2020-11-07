---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: bb4ab11406a644d34bdb5b45ea3b3fba47376826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819760"
---
# <span data-ttu-id="6db25-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="6db25-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="6db25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6db25-102">SYNOPSIS</span></span>
<span data-ttu-id="6db25-103">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="6db25-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="6db25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6db25-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6db25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6db25-105">DESCRIPTION</span></span>
<span data-ttu-id="6db25-106">Ruft die RegistryStatistics für eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="6db25-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="6db25-107">Damit erhalten Sie Informationen über die Anzahl der insgesamt aktivierten und deaktivierten Geräte in einem IotHub.</span><span class="sxs-lookup"><span data-stu-id="6db25-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="6db25-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6db25-108">EXAMPLES</span></span>

### <span data-ttu-id="6db25-109">Beispiel 1 Abrufen des RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="6db25-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6db25-110">Ruft die RegistryStatictics für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="6db25-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6db25-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6db25-111">PARAMETERS</span></span>

### <span data-ttu-id="6db25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db25-112">-DefaultProfile</span></span>
<span data-ttu-id="6db25-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6db25-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6db25-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6db25-114">-Name</span></span>
<span data-ttu-id="6db25-115">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="6db25-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="6db25-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db25-116">-ResourceGroupName</span></span>
<span data-ttu-id="6db25-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6db25-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6db25-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db25-118">CommonParameters</span></span>
<span data-ttu-id="6db25-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db25-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db25-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db25-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db25-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6db25-121">INPUTS</span></span>

### <span data-ttu-id="6db25-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6db25-122">System.String</span></span>

## <span data-ttu-id="6db25-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6db25-123">OUTPUTS</span></span>

### <span data-ttu-id="6db25-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="6db25-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="6db25-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6db25-125">NOTES</span></span>

## <span data-ttu-id="6db25-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6db25-126">RELATED LINKS</span></span>
