---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472483"
---
# <span data-ttu-id="0d82b-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="0d82b-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="0d82b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d82b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d82b-103">Ruft alle gültigen SKU ab, zu die dieser IotHub überwechseln kann.</span><span class="sxs-lookup"><span data-stu-id="0d82b-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="0d82b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d82b-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d82b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d82b-105">DESCRIPTION</span></span>
<span data-ttu-id="0d82b-106">Ruft alle gültigen SKU ab, zu der dieser IotHub übergangen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d82b-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="0d82b-107">Ein IotHub kann nicht zwischen kostenlosen und kostenpflichtigen SKU wechseln und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="0d82b-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="0d82b-108">Sie müssen dieOthub löschen und neu erstellen, wenn Sie dies erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d82b-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="0d82b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d82b-109">EXAMPLES</span></span>

### <span data-ttu-id="0d82b-110">Beispiel 1: Gültige SKU erhalten</span><span class="sxs-lookup"><span data-stu-id="0d82b-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0d82b-111">Ruft eine Liste allerKUS für IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="0d82b-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0d82b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d82b-112">PARAMETERS</span></span>

### <span data-ttu-id="0d82b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d82b-113">-DefaultProfile</span></span>
<span data-ttu-id="0d82b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0d82b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d82b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0d82b-115">-Name</span></span>
<span data-ttu-id="0d82b-116">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="0d82b-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="0d82b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d82b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d82b-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="0d82b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0d82b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d82b-119">CommonParameters</span></span>
<span data-ttu-id="0d82b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d82b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d82b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d82b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d82b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d82b-122">INPUTS</span></span>

### <span data-ttu-id="0d82b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0d82b-123">System.String</span></span>

## <span data-ttu-id="0d82b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d82b-124">OUTPUTS</span></span>

### <span data-ttu-id="0d82b-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="0d82b-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="0d82b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d82b-126">NOTES</span></span>

## <span data-ttu-id="0d82b-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d82b-127">RELATED LINKS</span></span>
