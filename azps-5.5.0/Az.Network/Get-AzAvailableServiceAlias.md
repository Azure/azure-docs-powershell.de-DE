---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161129"
---
# <span data-ttu-id="bc871-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="bc871-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="bc871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc871-102">SYNOPSIS</span></span>
<span data-ttu-id="bc871-103">Holen Sie sich verfügbare Dienstaliase in der Region.</span><span class="sxs-lookup"><span data-stu-id="bc871-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="bc871-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc871-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc871-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc871-105">DESCRIPTION</span></span>
<span data-ttu-id="bc871-106">Mit **dem Cmdlet "Get-AzAvailableServiceAlias"** können Sie alle verfügbaren Dienstaliase für ein Subnetz am angegebenen Standort abrufen.</span><span class="sxs-lookup"><span data-stu-id="bc871-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="bc871-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc871-107">EXAMPLES</span></span>

### <span data-ttu-id="bc871-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc871-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="bc871-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc871-109">PARAMETERS</span></span>

### <span data-ttu-id="bc871-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc871-110">-DefaultProfile</span></span>
<span data-ttu-id="bc871-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc871-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc871-112">-Location</span><span class="sxs-lookup"><span data-stu-id="bc871-112">-Location</span></span>
<span data-ttu-id="bc871-113">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="bc871-113">The location.</span></span>

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

### <span data-ttu-id="bc871-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc871-114">CommonParameters</span></span>
<span data-ttu-id="bc871-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc871-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc871-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc871-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc871-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc871-117">INPUTS</span></span>

### <span data-ttu-id="bc871-118">System.String</span><span class="sxs-lookup"><span data-stu-id="bc871-118">System.String</span></span>

## <span data-ttu-id="bc871-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc871-119">OUTPUTS</span></span>

### <span data-ttu-id="bc871-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="bc871-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="bc871-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc871-121">NOTES</span></span>

## <span data-ttu-id="bc871-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc871-122">RELATED LINKS</span></span>
