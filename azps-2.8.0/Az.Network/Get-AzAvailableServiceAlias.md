---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 7ea7bec01bacba43732f8e1eb544b109dfae11b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821887"
---
# <span data-ttu-id="16a5d-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="16a5d-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="16a5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="16a5d-103">Rufen Sie die verfügbaren Dienst Aliase in der Region ab.</span><span class="sxs-lookup"><span data-stu-id="16a5d-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="16a5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a5d-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16a5d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="16a5d-106">Mit dem Cmdlet **Get-AzAvailableServiceAlias** können Sie alle verfügbaren Dienst Aliase für ein Subnetz am angegebenen Speicherort abrufen.</span><span class="sxs-lookup"><span data-stu-id="16a5d-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="16a5d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="16a5d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16a5d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="16a5d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a5d-109">PARAMETERS</span></span>

### <span data-ttu-id="16a5d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a5d-110">-DefaultProfile</span></span>
<span data-ttu-id="16a5d-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16a5d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a5d-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="16a5d-112">-Location</span></span>
<span data-ttu-id="16a5d-113">Die Position.</span><span class="sxs-lookup"><span data-stu-id="16a5d-113">The location.</span></span>

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

### <span data-ttu-id="16a5d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a5d-114">CommonParameters</span></span>
<span data-ttu-id="16a5d-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a5d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a5d-116">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16a5d-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a5d-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16a5d-117">INPUTS</span></span>

### <span data-ttu-id="16a5d-118">System. String</span><span class="sxs-lookup"><span data-stu-id="16a5d-118">System.String</span></span>

## <span data-ttu-id="16a5d-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16a5d-119">OUTPUTS</span></span>

### <span data-ttu-id="16a5d-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="16a5d-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="16a5d-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="16a5d-121">NOTES</span></span>

## <span data-ttu-id="16a5d-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16a5d-122">RELATED LINKS</span></span>
